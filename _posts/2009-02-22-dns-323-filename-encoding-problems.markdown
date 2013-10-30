---
layout: post
status: publish
published: true
title: DNS-323 filename encoding problems
author: Per Liedman
author_login: per
author_email: per@liedman.net
author_url: http://per.liedman.net
wordpress_id: 133
wordpress_url: http://per.liedman.net/?p=133
date: 2009-02-22 13:53:43.000000000 +01:00
categories: []
tags: []
comments:
- id: 27765
  author: Silas Reyes
  author_email: Barratt526@gmail.com
  author_url: http://www.reddit.com/r/reddit.com/comments/g66x5/australians_analyze_the_pakistanis/
  date: !binary |-
    MjAxMS0wNC0yMyAxNjoyODowNiArMDIwMA==
  date_gmt: !binary |-
    MjAxMS0wNC0yMyAxNToyODowNiArMDIwMA==
  content: ! 'Your blog (DNS-323 filename encoding problems :  epepep) does not show
    up appropriately on my android - you may want to try and fix that :) Silas Reyes'
- id: 105094
  author: David Ayre
  author_email: dave@ayre.ca
  author_url: ''
  date: !binary |-
    MjAxMy0wMS0wMyAwMDo1NjowNCArMDEwMA==
  date_gmt: !binary |-
    MjAxMy0wMS0wMiAyMzo1NjowNCArMDEwMA==
  content: Very helpful thank you !   I'm retiring a DNS-323 and had this conversion
    problem after a previous firmware upgrade with many music filenames.   Your one
    liner saved me a lot of time.
---
This entry will be in english, since it's more likely to be helpful to others googling for solutions to the same problem.

A colleague of mine has used a <a href="http://www.dlink.com/products/?pid=509">D-Link DNS-323</a> as his RAID/backup solution at home. Apparently it's been working great for ages, until he recently updated its firmware, which also caused all files and directories containing non-ASCII characters (mostly å, ä and ö for us swedes) to be completely inaccessible; the windows sharing (Samba/SMB) wouldn't show the directories at all, and although they showed up in FTP, you couldn't really access them. Downgrading the firmware did not help.

The fun thing about the DNS-323, and the reason the colleague asked me for help, is that it runs Linux internally. Although it looks like a USB disk with a web interface, it actually has a full-featured operating system underneath. Well, <i>close to</i> full featured.

Googling for solutions, I found another swede, Martin Bergek, who had at least <a href="http://www.bergek.com/2008/11/12/filename-encoding-problems-on-dlink-dns-323/">similar problems</a> (by chance, I also happen to know who Martin is). It seems that older firmwares used <a href="http://en.wikipedia.org/wiki/Code_page_850">CP850</a> for filename encoding, while newer versions use <a href="http://en.wikipedia.org/wiki/UTF-8">UTF-8</a>. Probably some upgrade didn't go as planned, leaving the filenames in CP850, while interpreting them as UTF-8. Decoding swedish CP850 characters as UTF-8 results in invalid multibyte characters, causing the programs to refuse to handle files and directories containing them.

Now for the fun part. There seems to be quite a <a href="http://wiki.dns323.info/">community developing hacks for the DNS-323</a>. Using the so called <a href="http://wiki.dns323.info/howto:fun_plug">fun_plug</a>, you can very easily enable an SSH server, and get access to lots of useful commands. In my case, SSH access in combination with the <a href="http://en.wikipedia.org/wiki/Rsync">rsync</a> command turned out to be the key.

My solution was to get a backup disk large enough to copy all the material from the DNS-323 (actually, my colleague had already thought of this and provided me with a disk for this purpose). Once all the files where copied from the DNS-323, it could be wiped and the files copied back, but this time with the correct filename encoding.

As mentioned above, most of the problem results from applications interpreting the characters as invalid UTF-8 codes, refusing to work with them altogether. Even basic stuff, like doing recursive file lists with rsync, fails if a directory contains the invalid characters, probably since the runtime's string library can't work with the resulting strings. Shell commands like cd handle the directories, though, even if the characters are displayed as garbage.

Fortunately, rsync includes a command line parameter called <code>--iconv</code>, which lets you override which encoding is used when interpreting the filenames. This way, you can interpret the names correctly, and they can be converted into proper UTF-8. The trick is that you have to do this on the DNS-323 side, otherwise the conversion will be done on the backup unit's side, still causing errors attempting to do recursive file lists. (In case you connect the USB disk directly to the DNS-323, you won't have to think about this - in my case, the backup disk was connected to my Ubuntu desktop.)

So, to sum things up, this was the killer command line that made it possible to copy all the files out of the DNS-323:

<code>rsync -azv --iconv=cp850,utf8 /mnt/HD_a2/ per@asta:/media/usbdrive/dns323</code>

(Obviously, you'll have to replace the paths to whatever directories you're using on the DNS-323 as well as for the backup disk.)

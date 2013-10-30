---
layout: post
status: publish
published: true
title: Using Ubuntu One from a headless Oneiric Ocelot server
author: Per Liedman
author_login: per
author_email: per@liedman.net
author_url: http://per.liedman.net
wordpress_id: 248
wordpress_url: http://per.liedman.net/?p=248
date: 2011-12-28 12:08:41.000000000 +01:00
categories:
- '1'
tags: []
comments:
- id: 57084
  author: ! 'Using Ubuntu One for backup on a headless server : epepep'
  author_email: ''
  author_url: http://per.liedman.net/2011/01/22/using-ubuntu-one-for-backup-on-a-headless-server/
  date: !binary |-
    MjAxMS0xMi0yOCAxMjoxMToyOCArMDEwMA==
  date_gmt: !binary |-
    MjAxMS0xMi0yOCAxMToxMToyOCArMDEwMA==
  content: ! '[...] Update 2011-12-28: I wrote a follow up post on how to fix some
    of the issues with the instructions below, especially with regard to Ubuntu 11.10
    Oneiric Ocelot: Using Ubuntu One from a headless Oneiric Ocelot server [...]'
- id: 57174
  author: Roland
  author_email: rasos@alton.at
  author_url: http://www.osAlliance.com
  date: !binary |-
    MjAxMS0xMi0zMCAyMToxOTo1NSArMDEwMA==
  date_gmt: !binary |-
    MjAxMS0xMi0zMCAyMDoxOTo1NSArMDEwMA==
  content: ! "Hi Per,\r\nyour blog has been listed as an answer to my question on
    http://askubuntu.com/questions/89325/can-i-run-u1-on-an-ubuntu-server\r\nI was
    very happy someone has a solution and I followed your instructions (using a 10.04
    lucid server). Unfortunately, it seems that a module is missing. Any idea, how
    to obtain that? \r\n-Roland\r\nTraceback (most recent call last):\r\n  File \"/usr/local/bin/u1sync\",
    line 28, in \r\n    from u1sync.main import main\r\n  File \"/usr/local/lib/python2.6/dist-packages/u1sync/main.py\",
    line 39, in \r\n    import ubuntuone.storageprotocol.dircontent_pb2 as dircontent_pb2\r\nImportError:
    No module named ubuntuone.storageprotocol.dircontent_pb2"
- id: 58382
  author: SB
  author_email: stefan.bommer@gmx.net
  author_url: ''
  date: !binary |-
    MjAxMi0wMS0xMCAwMDoxMTowNyArMDEwMA==
  date_gmt: !binary |-
    MjAxMi0wMS0wOSAyMzoxMTowNyArMDEwMA==
  content: ! "same problem here, but on an oneiric headless server.\r\n\r\n\"Traceback
    (most recent call last):\r\n  File \"/usr/local/bin/u1sync\", line 28, in \r\n
    \   from u1sync.main import main\r\n  File \"/usr/local/lib/python2.7/dist-packages/u1sync/main.py\",
    line 39, in \r\n    import ubuntuone.storageprotocol.dircontent_pb2 as dircontent_pb2\r\nImportError:
    No module named ubuntuone.storageprotocol.dircontent_pb2\""
- id: 62952
  author: Jim
  author_email: jim@datalude.com
  author_url: ''
  date: !binary |-
    MjAxMi0wMy0wOCAwOTo0NToyMiArMDEwMA==
  date_gmt: !binary |-
    MjAxMi0wMy0wOCAwODo0NToyMiArMDEwMA==
  content: ! "apt-get install python-ubuntuone-storageprotocol got rid of that for
    me. I also needed python-twisted. \r\n\r\nBut now it seems I need to install 30Mbs
    of crap to get python-ubuntuone-client on there ... hmmm"
- id: 63129
  author: Jim
  author_email: jim@datalude.com
  author_url: ''
  date: !binary |-
    MjAxMi0wMy0xMCAwNzoxMzoyOSArMDEwMA==
  date_gmt: !binary |-
    MjAxMi0wMy0xMCAwNjoxMzoyOSArMDEwMA==
  content: ! "I think your server must have had Gnome installed, despite being screenless.
    \r\nUltimately ended up installing python-ubuntuone-client. Then gnome-ubuntuone-client,
    which demanded another 30 Mb of nonsense (spelling libraries, blah blah). And
    then u1sdtool still wouldn't start. \r\nEventually I hit on a plan: I'd need to
    use the gui config tool, forwarding the X connection to my local desktop. \r\nRight
    so I connected to the server with ssh -X user@remoteserver.com and then looked
    for the gui. Apparently its called ubuntuone-control-panel-gtk. But the package
    has a different name so ...\r\nsudo apt-get install ubuntuone-control-panel-gui\r\nand
    then\r\nubuntuone-control-panel-gtk\r\nAfter about 30 seconds the gui appears
    on my local machine and I can set up the UbutuOne connection! \r\n\r\nOnly trouble
    is that now, when I log out, the machine doesn't sync."
- id: 64225
  author: Roman
  author_email: rtg@rtg.in.ua
  author_url: http://rtg.in.ua/
  date: !binary |-
    MjAxMi0wMy0yMiAxMzoxOTo1OCArMDEwMA==
  date_gmt: !binary |-
    MjAxMi0wMy0yMiAxMjoxOTo1OCArMDEwMA==
  content: Right now I back up the data using Ubuntu One REST API, documented here
    - http://rtg.in.ua/blog/2012/03/upload-to-ubuntu-one-using-curl/
- id: 121935
  author: Phen 375
  author_email: ctxufylaxt@rxazel.com
  author_url: http://phen375123.com/
  date: !binary |-
    MjAxMy0wNC0xMCAwNTowMTo1OCArMDIwMA==
  date_gmt: !binary |-
    MjAxMy0wNC0xMCAwNDowMTo1OCArMDIwMA==
  content: krlssqfs, <a href="http://phen375123.com/" rel="nofollow">Powered by vlbook
    is phen375 safe</a>, lZkHVyf, [url=http://phen375123.com/]Phen 375[/url], CRHjmwX,
    http://phen375123.com/ Buy phen 375, XvaQXPr.
- id: 121936
  author: Etoro Review
  author_email: ayxbqddnjx@xjzgbq.com
  author_url: http://portugal-forex.com/etoro-review/
  date: !binary |-
    MjAxMy0wNC0xMCAwNTowNzoyMCArMDIwMA==
  date_gmt: !binary |-
    MjAxMy0wNC0xMCAwNDowNzoyMCArMDIwMA==
  content: qjyjqqfs, <a href="http://fioricetknowledgebase.com/" rel="nofollow">Fioricet</a>,
    OvwmtFi, [url=http://fioricetknowledgebase.com/]Fioricet pregnancy[/url], UZkRXeK,
    http://fioricetknowledgebase.com/ Fioricet, bSxGXaR, <a href="http://aboutvolumepills.com/"
    rel="nofollow">Volume Pills</a>, gEYfkme, [url=http://aboutvolumepills.com/]Volume
    pills[/url], SycmJKp, http://aboutvolumepills.com/ Volume Pills, lrsfjuQ, <a href="http://portugal-forex.com/etoro-review/"
    rel="nofollow">Etoro promotional code</a>, rpuQSiv, [url=http://portugal-forex.com/etoro-review/]Etoro
    Promotion Code[/url], NLnDrwX, http://portugal-forex.com/etoro-review/ Etoro Webtrader,
    BKlOlZd, <a href="http://bulimotbg.com/" rel="nofollow">Phen375</a>, oKNxvLD,
    [url=http://bulimotbg.com/]Phen375 reviews[/url], aWWsHAM, http://bulimotbg.com/
    Phen375 reviews, FxGODWI, <a href="http://www.vardenafilguide.com/" rel="nofollow">Woodward
    edu wafootball wp includes images vardenafil</a>, vhArNez, [url=http://www.vardenafilguide.com/]Zenegra
    sildenafil vs vardenafil[/url], GGHqejc, http://www.vardenafilguide.com/ Vardenafil
    products online, eDPUvXl, <a href="http://dinkstyle.com/hostmonster/" rel="nofollow">Host
    Monster</a>, KNQcOAO, [url=http://dinkstyle.com/hostmonster/]Hostmonster[/url],
    rcZQLJL, http://dinkstyle.com/hostmonster/ Monster garage host jesse james, yGmnkGK.
---
I discovered my backup has been broken since august. Yikes. I don't know the whole story why it started failing, but apparently it became permanently broken after updating to Ubuntu 11.10, Oneiric Ocelot. I use Ubuntu One for my backup, since I'm a cheap bastard. The way I set it up is described here: <a href="http://per.liedman.net/2011/01/22/using-ubuntu-one-for-backup-on-a-headless-server/">Using Ubuntu One for backup on a headless server</a>. Unfortunately, the package <i>ubuntuone-client-tools</i> has been removed in Oneiric Ocelot, which was pretty much a disaster for my backup. Since my old blog post still appears to be the number one Google result for backing up to Ubuntu One from the command line, I sort of feel obliged to tell you how to set it up in Oneiric Ocelot as well.

<h2>Setting up <i>u1sync</i> in Ubuntu 11.10, Oneiric Ocelot</h2>
Maybe I'm just dumb or something, but I was sort of shocked of how hard it was to find any information at all about what had happened to the <i>u1sync</i> utility or why the package <i>ubuntuone-client-tools</i> had been removed. At last, I found that <a href="https://launchpad.net/u1sync">u1sync is now hosted on Launchpad</a> - it doesn't appear to be part of any package, there doesn't appear to be any documentation, there isn't even a downloadable file. You can get the latest code (no tags or branches or anything fancy here) using <a href="http://bazaar.canonical.com/en/">Bazaar</a>, the VCS that isn't popular anywhere. Sorry to be sarcastic, but it's pretty much the caricature of an open source project. On the bright side: the code is there, someone has made this utility and is sort of maintaining it - I love you for doing this!

So, to get u1sync on your machine:
<ol>
  <li>Install Bazaar:
    <code>sudo apt-get install bzr</code>
  </li>
  <li>Download the latest code to your working directory:
    <code>bzr branch lp:u1sync</code>
  </li>
  <li>Install the code:
<code>    cd u1sync
    sudo python setup.py install
</code>  </li>
</ol>

...and we are more or less back to where we left off in my previous blog post. One minor issue: if you used the u1sync utility from the old package, you might get the error message:
<code> ImportError: No module named u1sync.genericmerge</code>
when running u1sync. In this case, you have an old file called <code>.ubuntuone-sync/local-index</code> in your synced folder - open the file and find the text <code>ubuntuone.u1sync.genericmerge</code> - remove the first part, so that only <code>u1sync.genericmerge</code> is left. (Yes, yikes! I spent a good part of a day swearing over this.)

<h2>Getting an authorization token for Ubuntu One using command line</h2>
A lot of the comments on my earlier blog post revolved around the fact that I reused the oauth token from my desktop machine when doing the backup from my server. That was an imperfect solution which resulted in file conflicts and other issues. On the other hand, not even Stuart Langridge, Technical architect for Ubuntu One, could post correct instructions on getting a new token from the command line :)

After digging in to this a bit more, writing some code of my own to do it, I finally found that of course someone else already did it. <a href="http://people.canonical.com/~roman.yepishev/">Roman Yepishev</a> wrote a small <a href="http://people.canonical.com/~roman.yepishev/us/ubuntuone-sso-login.py">script to create a new oauth token for Ubuntu One</a> - it's pretty self instructive if you use it. It dumps the new token to stdout, and you stick it into the u1sync commandline. Exactly what I wanted.

Hope this was helpful in getting Ubuntu One from the command line set up for you!

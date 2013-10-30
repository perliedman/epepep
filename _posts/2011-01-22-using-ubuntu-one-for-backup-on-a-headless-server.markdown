---
layout: post
status: publish
published: true
title: Using Ubuntu One for backup on a headless server
author: Per Liedman
author_login: per
author_email: per@liedman.net
author_url: http://per.liedman.net
wordpress_id: 224
wordpress_url: http://per.liedman.net/?p=224
date: 2011-01-22 14:26:10.000000000 +01:00
categories:
- '1'
tags: []
comments:
- id: 13408
  author: ! 'Tweets that mention Using Ubuntu One for backup on a headless server
    : epepep -- Topsy.com'
  author_email: ''
  author_url: http://topsy.com/per.liedman.net/2011/01/22/using-ubuntu-one-for-backup-on-a-headless-server/?utm_source=pingback&amp;utm_campaign=L2
  date: !binary |-
    MjAxMS0wMS0yMiAxNTowNzo1MSArMDEwMA==
  date_gmt: !binary |-
    MjAxMS0wMS0yMiAxNDowNzo1MSArMDEwMA==
  content: ! '[...] This post was mentioned on Twitter by Stuart Langridge and Per
    Liedman, Christopher. Christopher said: Great will try this RT @liedman Finally
    got around to document how to use Ubuntu One from a headless server: http://goo.gl/FC4sW
    (ping @sil) [...]'
- id: 13412
  author: sil
  author_email: stuart.langridge@canonical.com
  author_url: http://one.ubuntu.com
  date: !binary |-
    MjAxMS0wMS0yMiAxNjozNjoxNCArMDEwMA==
  date_gmt: !binary |-
    MjAxMS0wMS0yMiAxNTozNjoxNCArMDEwMA==
  content: ! "This is very cool. I should re-iterate that u1sync isn't supported by
    us, so it's best-effort only :-)\r\n\r\nBetter way of getting the oauth token:\r\n\r\n1.
    Request a new token at Ubuntu SSO\r\n\r\nwget --user=stuart.langridge@canonical.com-O
    token-details --ask-password \"https://login.ubuntu.com/api/1.0/authentications?ws.op=authenticate&amp;token_name=Ubuntu%20One%20@%20$(hostname)\"\r\n\r\nChange
    --user to be your Ubuntu One username, and enter your Ubuntu One password when
    prompted. You will now have a file named \"token-details\" which contains your
    OAuth token.\r\n\r\n2. Tell Ubuntu One that that token's OK\r\n\r\nwget -O token-approval
    'https://one.ubuntu.com/oauth/sso-finished-so-get-tokens/stuart.langridge%40canonical.com'\r\n\r\n(there
    seems to be a slight problem with this step right now, but it should work :))\r\n\r\nAfter
    that, you ought to be able to use the token information in token-details with
    u1sync."
- id: 24436
  author: smurf
  author_email: smurf@liedman.net
  author_url: ''
  date: !binary |-
    MjAxMS0wNC0wMSAxNDozNDozMyArMDIwMA==
  date_gmt: !binary |-
    MjAxMS0wNC0wMSAxMzozNDozMyArMDIwMA==
  content: ! '@sil: don''t you have to supply any data from the token in the headers?'
- id: 29162
  author: wolf
  author_email: wolf@blazingangles.com
  author_url: http://blog.blazingangles.net/wen
  date: !binary |-
    MjAxMS0wNS0wMSAwODo0NzowNCArMDIwMA==
  date_gmt: !binary |-
    MjAxMS0wNS0wMSAwNzo0NzowNCArMDIwMA==
  content: ! '@sil: the slight problem seems to have lasted since January, because
    it still doesn''t work. Isn''t there some other problem, like not supplying the
    token information like "smurf" suggests?'
- id: 29519
  author: gavin
  author_email: gavinjfleming@gmail.com
  author_url: ''
  date: !binary |-
    MjAxMS0wNS0wNCAxMjozMjoxNiArMDIwMA==
  date_gmt: !binary |-
    MjAxMS0wNS0wNCAxMTozMjoxNiArMDIwMA==
  content: ! 'Same here. Step 1 works fine, Step 2 gives this: â€˜https://one.ubuntu.com/oauth/sso-finished-so-get-tokens/my%40email.comâ€™:
    Scheme missing.'
- id: 40928
  author: Torsten Bronger
  author_email: bronger@physik.rwth-aachen.de
  author_url: ''
  date: !binary |-
    MjAxMS0wOC0xMSAwMDo1OTo1NSArMDIwMA==
  date_gmt: !binary |-
    MjAxMS0wOC0xMCAyMzo1OTo1NSArMDIwMA==
  content: Thanks for the starting point, but in this form the page is only partly
    helpful. sil's alternative way is indeed broken -- just browse to the send link
    with an ordinary browser.  And, "ubuntuone-client-tools" doesn't seem to be in
    the repositories anymore.
- id: 40929
  author: Torsten Bronger
  author_email: bronger@physik.rwth-aachen.de
  author_url: ''
  date: !binary |-
    MjAxMS0wOC0xMSAwMTowMToxNSArMDIwMA==
  date_gmt: !binary |-
    MjAxMS0wOC0xMSAwMDowMToxNSArMDIwMA==
  content: s/send/second/
- id: 56317
  author: Nick Yeoman
  author_email: c@nickyeoman.com
  author_url: http://www.nickyeoman.com
  date: !binary |-
    MjAxMS0xMi0xOCAxODo0NzoxNyArMDEwMA==
  date_gmt: !binary |-
    MjAxMS0xMi0xOCAxNzo0NzoxNyArMDEwMA==
  content: ! "Exactly what I was looking for!\r\n\r\nGreat article!"
- id: 56642
  author: Steven Gordon
  author_email: steve.per@sandilands.info
  author_url: http://sandilands.info/sgordon/
  date: !binary |-
    MjAxMS0xMi0yMyAwNzoxMTowNyArMDEwMA==
  date_gmt: !binary |-
    MjAxMS0xMi0yMyAwNjoxMTowNyArMDEwMA==
  content: Per's instructions worked fine for me on Ubuntu 10.04 server and 11.04
    desktop. Note however the string that contains the token and token secret in the
    password was formatted differently. I had a string like 'consumer_secret=aaaaa&amp;token=bbbbb&amp;consumer_key=ccccc&amp;name=ddddd&amp;token_secret=eeeee'
    where I used the values 'bbbbb' and 'eeeee'
- id: 57083
  author: ! 'Using Ubuntu One from a headless Oneiric Ocelot server : epepep'
  author_email: ''
  author_url: http://per.liedman.net/2011/12/28/using-ubuntu-one-from-a-headless-oneiric-ocelot/
  date: !binary |-
    MjAxMS0xMi0yOCAxMjowODo0NCArMDEwMA==
  date_gmt: !binary |-
    MjAxMS0xMi0yOCAxMTowODo0NCArMDEwMA==
  content: ! '[...] Ubuntu One for my backup, since I&#8217;m a cheap bastard. The
    way I set it up is described here: Using Ubuntu One for backup on a headless server.
    Unfortunately, the package ubuntuone-client-tools has been removed in Oneiric
    Ocelot, which was [...]'
- id: 57086
  author: Per Liedman
  author_email: per@liedman.net
  author_url: http://per.liedman.net
  date: !binary |-
    MjAxMS0xMi0yOCAxMjoxMzowNyArMDEwMA==
  date_gmt: !binary |-
    MjAxMS0xMi0yOCAxMToxMzowNyArMDEwMA==
  content: ! "I wrote a follow up post with instructions regarding later Ubuntu versions
    (in particular 11.10 Oneiric Ocelot): http://per.liedman.net/2011/12/28/using-ubuntu-one-from-a-headless-oneiric-ocelot/\r\n\r\nThis
    post also documents how to get a new oauth token for your headless server."
- id: 113622
  author: http://enbase.net/db/User:Kimipnzai
  author_email: zella.rooney@gmail.com
  author_url: http://enbase.net/db/User:Kimipnzai
  date: !binary |-
    MjAxMy0wMy0wNSAwMTo1MzowMCArMDEwMA==
  date_gmt: !binary |-
    MjAxMy0wMy0wNSAwMDo1MzowMCArMDEwMA==
  content: Thanks to my father who informed me about this webpage, this website is
    actually awesome.
- id: 127135
  author: Cosmetic Dentistry- Warwick Archives Â« Dentists in Orange County NY Dentists
    in Orange County NY
  author_email: nola.levi@zoho.com
  author_url: http://ocnydentistreviews.com/category/cosmeticwarwick/
  date: !binary |-
    MjAxMy0wNS0wNSAwNzo0NzoyMyArMDIwMA==
  date_gmt: !binary |-
    MjAxMy0wNS0wNSAwNjo0NzoyMyArMDIwMA==
  content: ! "You really make it appear so easy along with \r\nyour presentation but
    I find this matter to be actually something \r\nwhich I think I'd by no means
    understand. It sort of feels too complicated and extremely large for me. I'm looking
    ahead on your subsequent \r\npublish, I'll try to get the grasp of it!"
- id: 134845
  author: california casualty auto and home insurance
  author_email: renatearcher@mailworks.org
  author_url: http://www.calautoinsurance.net/
  date: !binary |-
    MjAxMy0wNi0wNiAwNzo0Mjo0MCArMDIwMA==
  date_gmt: !binary |-
    MjAxMy0wNi0wNiAwNjo0Mjo0MCArMDIwMA==
  content: It's an awesome paragraph in support of all the online people; they will
    obtain benefit from it I am sure.
- id: 140474
  author: top eleven hack token
  author_email: heather_gower@gmx.de
  author_url: http://www.youtube.com/watch?v=ubOOjC1qX8U
  date: !binary |-
    MjAxMy0wNy0wNCAwODoyNDo0MiArMDIwMA==
  date_gmt: !binary |-
    MjAxMy0wNy0wNCAwNzoyNDo0MiArMDIwMA==
  content: ! "Thank you for sharing your info. I really appreciate your efforts and
    \r\nI am waiting for your further write ups thank you once again."
- id: 146806
  author: mspy discount coupon
  author_email: manuel.maxwell@gmail.com
  author_url: http://discount202.com/category/mspy-coupon-code/
  date: !binary |-
    MjAxMy0wNy0yOSAwMjowNDoxOSArMDIwMA==
  date_gmt: !binary |-
    MjAxMy0wNy0yOSAwMTowNDoxOSArMDIwMA==
  content: ! "certainly like your website but you have to take a look \r\nat the spelling
    on quite a few of your posts.\r\nA number of them are rife with spelling problems
    and I in finding it very troublesome \r\nto tell the truth then again I'll surely
    come back again."
- id: 152869
  author: wedding flowers
  author_email: milan_linkous@gmail.com
  author_url: http://www.weddingflowersofamerica.com/
  date: !binary |-
    MjAxMy0wOC0yMyAxMzoyODozNiArMDIwMA==
  date_gmt: !binary |-
    MjAxMy0wOC0yMyAxMjoyODozNiArMDIwMA==
  content: Thanks , I've just been searching for info about this topic for a long
    time and yours is the best I have found out so far. But, what about the conclusion?
    Are you positive about the source?
- id: 165398
  author: khandala photos
  author_email: adrianna-pinkney@yahoo.com
  author_url: http://habitatnys.org/index.php/member/264675
  date: !binary |-
    MjAxMy0xMC0yNSAyMDo1NTo1MyArMDIwMA==
  date_gmt: !binary |-
    MjAxMy0xMC0yNSAxOTo1NTo1MyArMDIwMA==
  content: ! "There can also be the Powai Lake, Mahakali Caves, Gateway of India,
    Juhu beach, etc.\r\nTo load you off, here are some in the most happening pictorial
    destinations around Pune.\r\nOnce you uncover the hill station of Bhandardara,
    it's certain you will be drawn by its tranquility \r\nagain and again."
---
<em>Update 2011-12-28:</em> I wrote a follow up post on how to fix some of the issues with the instructions below, especially with regard to Ubuntu 11.10 Oneiric Ocelot: <a href="http://per.liedman.net/2011/12/28/using-ubuntu-one-from-a-headless-oneiric-ocelot/">Using Ubuntu One from a headless Oneiric Ocelot server</a>

Ok, let me start by stating that I know, and you should also know, that Ubuntu One and the other cloud storage services like DropBox are not for serious backups. So if you're reading this post to learn something about backing up your enterprisy data, you have <em>come to the wrong place</em>. But if you're like me, and have a server in your closet as a hobby, and just want some sort of backup that's also off site, you have come to the right place.

The problem at hand: I have a server in my closet at home, and I store some stuff on it that I would be very sorry if I lost. (I also store a lot more on it that I don't care the least about.) So, I want to back that stuff up. It's primarily a couple of MySQL databases and some version control repositories.

Ubuntu comes with a cloud storage service called <a href="https://one.ubuntu.com/">Ubuntu One</a>. Ubuntu One gives you a free account with two gigabytes of storage, and you can pay a small subscription fee to get significantly more storage if you need it. While there are <a href="http://peterthorin.wordpress.com/2010/01/28/backup-solutions/">lots of other similar solutions</a>, Ubuntu One seems like a nice choice if you're into Ubuntu, since its neatly integrated into the Gnome desktop.

The bad news is that for a headless (no screen) machine, like my server, Ubuntu One is currently a bit harder to set up. I really need the backups to work even if I don't start a remote session and type my password, and so on. A backup that requires manual intervention is about as bad as no backup at all, in my opinion.

I was sort of frustrated when I found this out, and <a href="http://twitter.com/#!/liedman/status/23337089936392192">Twittered angrily</a> about the lack of command line interface. A couple of days later, I got a very friendly reply from Stuart Langridge (<a href="http://twitter.com/#!/sil">@sil</a>), who happens to be technical architect for Ubuntu One. Wow. Not only a response to my rant, but a short conversation ended up with enough clues for me to solve the problem at hand.

So, to save you from having to finding out the details yourself, here is how you could go about making Ubuntu One work as a backup for your headless server:

<h3>Install ubuntuone-client-tools</h3>
The program you need is called <code>u1sync</code>, and is distributed in a package called <code>ubuntuone-client-tools</code>. Install it:

<code>sudo apt-get install ubuntuone-client-tools</code>

<h3>Get an authentication token</h3>
The tricky part about getting Ubuntu One working standalone is really authentication. Normally, Ubuntu One authenticates using information stored in your Gnome keyring. On the server, you might not even have the keyring deamon installed, and even if it is, the backup must work even if you haven't entered your keyring password, and so on. Fortunately, <code>u1sync</code> can authenticate without the keyring, but you will have to provide an <a href="http://en.wikipedia.org/wiki/OAuth">OAuth</a> token manually. Getting that token feels sort of like a hack, but this is how I do it:
<ol>
	<li>Go to a desktop machine where you have Ubuntu One set up with the account you want to use</li>
	<li>Go to <strong>System</strong> menu -> <strong>Preferences</strong> -> <strong>Passwords and Encryption Keys</strong></li>
	<li>Under the tab <strong>Passwords</strong>, you will find an entry called <strong>UbuntuOne token for https://ubuntuone.com</strong> - double click it.</li>
	<li>In the dialog, open the password label and mark the <strong>Show password</strong> checkbox. It should now look something like this:

<img src="http://per.liedman.net/wp-content/uploads/2011/01/ubuntuone-oauth-token-dialog.png" alt="" title="Ubuntu One OAuth token dialog" width="361" height="332" class="aligncenter size-full wp-image-230" />
</li>
	<li>Copy the text from the password field into a text editor of your choice. It will look like this:
<code>oauth_token_secret=xxxx&oauth_token=yyyy</code>, but with <code>xxxx</code> and <code>yyyy</code> replaced with much more gibberish. It's those to parts of the strings you're after.</li>
	<li>In your backup script on your server (you have one of those already, right? Mine is based around <a href="http://sourceforge.net/projects/automysqlbackup/">AutoMySQLBackup</a> and lots of <code>tar</code> commands), insert this line somewhere at the end:<br/><code>u1sync --oauth=yyyy:xxxx [your backup folder]</code><br/>Note the order of things: u1sync needs to oauth token (key) first, and the secret as a seconds argument; at least for me, they were stored in the other way around in the keyring string.</lI>

And that's about it! The <code>u1sync</code> command will automatically synchronize the directory contents against your account every time the script is run. It will also output a lot of information about what it's doing, so if you're running the backup script from <code>cron</code> (you should), you might want to redirect the output to a log or <code>/dev/null</code>, or you will get lots of long mails.

Also note, that if you for some reason unauthorize the machine you got the OAuth token from, you will also unauthorize the backup server. Unauthorizing a machine really means revoking the OAuth token, and since the machines share the same token, both will now be unauthorized.

Finally, if you find out or already know a simpler way to get the OAuth token, I really interested in hearing about it. And yay for Ubuntu (One) and Stuart Langridge, thanks to them I now have an easy and free backup solution for at least the most critical stuff.

---
layout: post
status: publish
published: true
title: What plane?
author: Per Liedman
author_login: per
author_email: per@liedman.net
author_url: http://per.liedman.net
wordpress_id: 168
wordpress_url: http://per.liedman.net/?p=168
date: 2010-07-26 15:49:06.000000000 +02:00
categories:
- What plane
tags: []
comments:
- id: 3173
  author: ! 'More planes : epepep'
  author_email: ''
  author_url: http://per.liedman.net/2010/08/10/more-planes/
  date: !binary |-
    MjAxMC0wOC0xMCAwODo1MDo1OSArMDIwMA==
  date_gmt: !binary |-
    MjAxMC0wOC0xMCAwNzo1MDo1OSArMDIwMA==
  content: ! '[...] quick update. Since I got an Android phone (an HTC Desire, yay!),
    I&#8217;ve tested my What Plane application on a real device. I&#8217;ve fixed
    some minor issues, so that it actually sort of works [...]'
- id: 3333
  author: ! 'Flightradar24 for Android : epepep'
  author_email: ''
  author_url: http://per.liedman.net/2010/09/25/flightradar24-for-android/
  date: !binary |-
    MjAxMC0wOS0yNSAxMDozMDozMyArMDIwMA==
  date_gmt: !binary |-
    MjAxMC0wOS0yNSAwOTozMDozMyArMDIwMA==
  content: ! '[...] their own Android application. I figured they would do that, and
    that it would pretty much make What Plane? obsolete. To my surprise, the app they
    actually released is surprisingly thin, and at least for me [...]'
- id: 33553
  author: Henrik ClaesÃ©n
  author_email: henrik.claesen@gmail.com
  author_url: ''
  date: !binary |-
    MjAxMS0wNi0wNyAxMjo0NzoyNyArMDIwMA==
  date_gmt: !binary |-
    MjAxMS0wNi0wNyAxMTo0NzoyNyArMDIwMA==
  content: Nice application! But if you view details the details is hided as soon
    as the information is updated. And the application always updates?! And for the
    GUI freaks a nice application would be nice ;). This was found on a Samsung Galaxy
    S2, using Android version 2.3.3
- id: 33554
  author: Henrik ClaesÃ©n
  author_email: henrik.claesen@gmail.com
  author_url: ''
  date: !binary |-
    MjAxMS0wNi0wNyAxMjo1MDowOCArMDIwMA==
  date_gmt: !binary |-
    MjAxMS0wNi0wNyAxMTo1MDowOCArMDIwMA==
  content: hmmm...a tiny word fell out of the comment above. It meant a application
    icon would be nice....
- id: 33859
  author: Per Liedman
  author_email: per@liedman.net
  author_url: http://per.liedman.net
  date: !binary |-
    MjAxMS0wNi0wOSAxODo0NjoxOSArMDIwMA==
  date_gmt: !binary |-
    MjAxMS0wNi0wOSAxNzo0NjoxOSArMDIwMA==
  content: ! "Henrik: thanks for the feedback. Funny thing is, just the other day,
    I actually made an icon for the app. So the next version, which I hope to release
    in a couple of days, you will get an icon and a couple of bug fixes.\r\n\r\nI
    agree that the automatic update (which occurs once per minute) shouldn't close
    the aircraft you've expanded in the list. Perhaps I will find the energy to fix
    that as well."
- id: 53722
  author: Tim Bennett
  author_email: flashman@gmail.com
  author_url: http://electronsoup.net
  date: !binary |-
    MjAxMS0xMS0xMSAwMTozMzowMiArMDEwMA==
  date_gmt: !binary |-
    MjAxMS0xMS0xMSAwMDozMzowMiArMDEwMA==
  content: ! "Nice - I've just finished coding some PHP functions that take PlaneFeed.json
    and read out a list of nearby aircraft. There was <a href=\"http://forum.flightradar24.com/archive/index.php/t-24.html\"
    rel=\"nofollow\">a discussion</a> about why they don't offer API access. Apparently
    some contributors don't want others to get a commercial gain from data that they
    donated to Flightradar24.\r\n\r\nOne thing I might do is log the data for my city
    for 24 hours, then <a href=\"http://www.youtube.com/watch?v=1XBwjQsOEeg\" rel=\"nofollow\">visualize
    it</a>."
---
So, I've made my first Android application. That was a nice experience, especially after having hacked J2ME on Symbian for a short while. Only sad thing is that I haven't got an Android phone, so I can only use my app in the emulator, which is boring as hell, since it's a GPS based application. Well, I'm getting ahead of myself - so first some background about me, and then some more about that app.

Sometime in my early twenties, I once spent something like two whole days flying around the world in Microsoft Flight Simulator, in realtime. My old friends still like to remind me of this slightly autistic and highly nerdy feat once in a while. For my own part, it's mostly a reminder of the oceans of free time I had while studying at university (I distinctly remember spending a considerable amount of the hours over the pacific studying for some math course I took at the time).

These days, I don't even have flight simulator installed, but my interest in airliners and flying still linger in the back of my mind, and when the skies are clear, I often find myself drifting off, thinking about the contrails I see, what aircraft it might be, where they're heading and where they're coming from. In the last year, this little hobby has gotten a bit more interesting, thanks to a site called <a href="http://flightradar24.com/">flightradar24.com</a>, which makes it easy to check if it actually was a 747 that just passed by overhead, or if it was some other four engine model. (As a side note, flightradar24.com got a lot of media attention while the Icelandic ash cloud from EyjafjallajÃ¶kull grounded most air traffic over Europe for a couple of weeks, since everyone was very keen on seeing all the planes that weren't flying. That was sort of weird. Anyway.)

The only thing that isn't perfect about flightradar24.com for my little hobby, is that I'm not very often at a computer when I spot aircraft, and that their site is very Javascript-based, and hence not very useful in a phone browser. To solve this issue, some on and off hacking for a couple of months have resulted in a solution:

<ul>
  <li>A web service that uses data from Flightradar24.com to list the planes currently closest to a certain location, and presenting it as HTML, JSON or HTML</li>
  <li>A small application for Symbian/J2ME that uses a phone's GPS to query the mentioned web service</li>
  <li>A small application for Android that does the same</li>
</ul>

The Symbian version is still a bit too much of a hack to actually show to anyone else, but the server parts and the Android application is in a state which I feel is sort of usable. So, if you're interested, here's the application file for version 1.0.0 of <em>What plane?</em>, which will show you the five aircraft closest to where you are, their direction and distance, and some more detailed information on model, airline, where they're heading, and so on.

<del datetime="2010-08-10T07:40:30+00:00">WhatPlane-1.0.0.apk</del>
<em><strong>Updated 2010-08-10: </strong></em><del datetime="2011-06-09T21:20:36+00:00">WhatPlane-1.0.1.apk</del>
<em><strong>Updated 2011-06-09: </strong></em><a href="http://www.liedman.net/share/WhatPlane-android-1.1.1.apk">WhatPlane-android-1.1.1.apk</a>

...and for those anxious of you who absolutely need screenshots, here's a couple of those:
[caption id="attachment_171" align="alignnone" width="324" caption="List of closest aircraft"]<a href="http://per.liedman.net/wp-content/uploads/2010/07/Whatplane-screenshot1.png"><img src="http://per.liedman.net/wp-content/uploads/2010/07/Whatplane-screenshot1.png" alt="" title="Screenshot 1" width="324" height="484" class="size-full wp-image-171" /></a>[/caption]
[caption id="attachment_172" align="alignnone" width="328" caption="Aircraft details"]<a href="http://per.liedman.net/wp-content/uploads/2010/07/Whatplane-screenshot2.png"><img src="http://per.liedman.net/wp-content/uploads/2010/07/Whatplane-screenshot2.png" alt="" title="Whatplane-screenshot2" width="328" height="480" class="size-full wp-image-172" /></a>[/caption]

For those interested, I plan to make the source available at some point in the future (that I haven't done it already is mostly because I don't know where it's best to host it, and I haven't got that much time to work on this). Also, it must be noted that all the data shown in the application is from flightradar24.com - and it's really <em>their</em> data. I haven't checked with them if it's ok to use it in this way, but since they're a free service, aggregating information mostly from enthusiasts sharing the data from their ADS-B receivers, I hope this application is in the spirit of their vision.

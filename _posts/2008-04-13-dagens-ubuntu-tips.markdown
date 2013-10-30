---
layout: post
status: publish
published: true
title: Dagens Ubuntu-tips
author: Per Liedman
author_login: per
author_email: per@liedman.net
author_url: http://per.liedman.net
wordpress_id: 123
wordpress_url: http://per.liedman.net/?p=123
date: 2008-04-13 18:17:36.000000000 +02:00
categories: []
tags: []
comments: []
---
Jag är en stor vän av tangenbordsgenvägar. Tydligen till den grad att jag inte ens märker att jag använder dem. Däremot blir det problem när de plötsligt slutar fungera. Därför är en av de få irritationsmoment jag haft sen jag <a href="http://per.liedman.net/?p=116">konverterade till Ubuntu</a> varit att en så enkel sak som att flytta markören i URL:er i Firefox inte längre fungerar som jag är van vid.

I Windows kan man förflytta markören snabbt genom en URL till nästa "logiska stopp" (punkt, snedstreck, &-tecken, etc.) genom att hålla inne Ctrl samtidigt som en av piltangenterna. I Ubuntu leder (med default-inställningarna) tyvärr detta till att man hoppar direkt till slutet respektive början av hela URL:en, till föga nytta.

Efter att äntligen orkat upparbeta en tillräcklig irritation över detta, Googlade jag och fann lösningen: ändra inställningen <em>layout.word_select.stop_at_punctuation</em> till <em>true</em> i Firefox (genom att gå till <a href="about:config">about:config</a>). Underbart lätt. Varför detta inte är grundinställningen är ett mysterium.

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
Jag Ã¤r en stor vÃ¤n av tangenbordsgenvÃ¤gar. Tydligen till den grad att jag inte ens mÃ¤rker att jag anvÃ¤nder dem. DÃ¤remot blir det problem nÃ¤r de plÃ¶tsligt slutar fungera. DÃ¤rfÃ¶r Ã¤r en av de fÃ¥ irritationsmoment jag haft sen jag <a href="http://per.liedman.net/?p=116">konverterade till Ubuntu</a> varit att en sÃ¥ enkel sak som att flytta markÃ¶ren i URL:er i Firefox inte lÃ¤ngre fungerar som jag Ã¤r van vid.

I Windows kan man fÃ¶rflytta markÃ¶ren snabbt genom en URL till nÃ¤sta "logiska stopp" (punkt, snedstreck, &-tecken, etc.) genom att hÃ¥lla inne Ctrl samtidigt som en av piltangenterna. I Ubuntu leder (med default-instÃ¤llningarna) tyvÃ¤rr detta till att man hoppar direkt till slutet respektive bÃ¶rjan av hela URL:en, till fÃ¶ga nytta.

Efter att Ã¤ntligen orkat upparbeta en tillrÃ¤cklig irritation Ã¶ver detta, Googlade jag och fann lÃ¶sningen: Ã¤ndra instÃ¤llningen <em>layout.word_select.stop_at_punctuation</em> till <em>true</em> i Firefox (genom att gÃ¥ till <a href="about:config">about:config</a>). Underbart lÃ¤tt. VarfÃ¶r detta inte Ã¤r grundinstÃ¤llningen Ã¤r ett mysterium.

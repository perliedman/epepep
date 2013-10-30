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
Jag &auml;r en stor v&auml;n av tangenbordsgenv&auml;gar. Tydligen till den grad att jag inte ens m&auml;rker att jag anv&auml;nder dem. D&auml;remot blir det problem n&auml;r de pl&ouml;tsligt slutar fungera. D&auml;rf&ouml;r &auml;r en av de f&aring; irritationsmoment jag haft sen jag <a href="http:&#47;&#47;per.liedman.net&#47;?p=116">konverterade till Ubuntu<&#47;a> varit att en s&aring; enkel sak som att flytta mark&ouml;ren i URL:er i Firefox inte l&auml;ngre fungerar som jag &auml;r van vid.

I Windows kan man f&ouml;rflytta mark&ouml;ren snabbt genom en URL till n&auml;sta "logiska stopp" (punkt, snedstreck, &-tecken, etc.) genom att h&aring;lla inne Ctrl samtidigt som en av piltangenterna. I Ubuntu leder (med default-inst&auml;llningarna) tyv&auml;rr detta till att man hoppar direkt till slutet respektive b&ouml;rjan av hela URL:en, till f&ouml;ga nytta.

Efter att &auml;ntligen orkat upparbeta en tillr&auml;cklig irritation &ouml;ver detta, Googlade jag och fann l&ouml;sningen: &auml;ndra inst&auml;llningen <em>layout.word_select.stop_at_punctuation<&#47;em> till <em>true<&#47;em> i Firefox (genom att g&aring; till <a href="about:config">about:config<&#47;a>). Underbart l&auml;tt. Varf&ouml;r detta inte &auml;r grundinst&auml;llningen &auml;r ett mysterium.

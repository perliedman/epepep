---
layout: post
status: publish
published: true
title: Debugmeddelanden - en resa mot vansinnet
author: Per Liedman
author_login: per
author_email: per@liedman.net
author_url: http://per.liedman.net
wordpress_id: 5
wordpress_url: http://www.liedman.netprogrammering/debugmeddelanden---en-resa-mot-vansinnet/
date: 2003-12-01 00:35:58.000000000 +01:00
categories: []
tags: []
comments: []
---
Har efter en l&aring;ng tids unders&ouml;kningar kommit fram till att meddelanden som f&ouml;rfattas av programmerare i deras ivriga jakt efter problemfri programvara samtidigt kan tj&auml;na som dokumentation av hur deras f&ouml;rst&aring;nd l&aring;ngsamt bryts ner. Vad som b&ouml;rjar som logiska och m&aring;lmedvetna f&ouml;rs&ouml;k till att leta upp problemet f&ouml;rtvinar allt eftersom hoppl&ouml;sheten s&auml;tter in och tilliten till f&ouml;rnuft b&ouml;rjar sina. Vad som b&ouml;rjade som en jakt efter ett race condition f&ouml;rvandlas smygande till ett ifr&aring;gs&auml;ttande av programmerarens f&ouml;rst&aring;nd, och desperationen kan l&auml;ttast sp&aring;ras i utskrifterna i programmerarens konsoll.

F&ouml;r att illustrera s&aring; v&auml;l som kategorisera har jag valt att etablera den <b>Liedmanska fyrgradiga skalan av debugutskriftsvansinne<&#47;b>:

1. <b>F&ouml;rst&aring;ndiga utskrifter<&#47;b>: Utskrifter som l&auml;mpar sig s&aring;v&auml;l som f&ouml;r att hitta problemet, som f&ouml;r andra programmerares &ouml;gon. Meddelanden en labr&auml;ttare p&aring; en programmeringsutbildning hade varit n&ouml;jd med. Exempel: <i>"Detected unexpected value for object foo. Expected 'fnurra', but was 'knurra'."<&#47;i>

2. <b>Irriterade utskrifter<&#47;b>: T&aring;lamodet b&ouml;rjar tryta. Programmeraren skiter i om utskrifterna verkar vettiga i l&auml;ngden. De g&ouml;r sitt jobb just nu. Exempel: <i>"42, 42, 42, 42, 42, 43, 42, 42. Interrupt. 42, 42, 42, 42. Brk"<&#47;i>

3. <b>P&aring; ruinens brant<&#47;b>: Det st&aring;r nu klart f&ouml;r programmeraren att hans f&ouml;rst&aring;nd inte kan omfatta problemet. V&auml;rlden &auml;r skev och overklig, saker tycks inte l&auml;ngre h&auml;nga ihop. Ifr&aring;gas&auml;ttandet av det som tagits f&ouml;r givet kan sp&aring;ras i meddelandenas ton. Exempel: <i>"Impossible error."<&#47;i>, <i>"***Shit has happened***"<&#47;i>, <i>"Yeah, right."<&#47;i> (det sist &auml;r ett autentiskt meddelande fr&aring;n n&aring;gon &auml;ldre version av ICQ)

4. <b>Bortom f&ouml;nuftets gr&auml;nser<&#47;b>: Det spelar ingen roll l&auml;ngre. Det finns ingen r&auml;ddning och &auml;ven om det fanns det bryr vi oss inte. Vi &auml;r f&ouml;rlorade, borta, desillusionerade fr&aring;n v&aring;ra f&ouml;rest&auml;llningar om programutvecklingsmetodik. Bortom detta finns inte buggar, bara kaserad kod. Exempel: <i>"fisksoppa"<&#47;i>, <i>"fyrmanst&auml;lt"<&#47;i>, <i>"king edward"<&#47;i>

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
Har efter en lång tids undersökningar kommit fram till att meddelanden som författas av programmerare i deras ivriga jakt efter problemfri programvara samtidigt kan tjäna som dokumentation av hur deras förstånd långsamt bryts ner. Vad som börjar som logiska och målmedvetna försök till att leta upp problemet förtvinar allt eftersom hopplösheten sätter in och tilliten till förnuft börjar sina. Vad som började som en jakt efter ett race condition förvandlas smygande till ett ifrågsättande av programmerarens förstånd, och desperationen kan lättast spåras i utskrifterna i programmerarens konsoll.

För att illustrera så väl som kategorisera har jag valt att etablera den <b>Liedmanska fyrgradiga skalan av debugutskriftsvansinne</b>:

1. <b>Förståndiga utskrifter</b>: Utskrifter som lämpar sig såväl som för att hitta problemet, som för andra programmerares ögon. Meddelanden en labrättare på en programmeringsutbildning hade varit nöjd med. Exempel: <i>"Detected unexpected value for object foo. Expected 'fnurra', but was 'knurra'."</i>

2. <b>Irriterade utskrifter</b>: Tålamodet börjar tryta. Programmeraren skiter i om utskrifterna verkar vettiga i längden. De gör sitt jobb just nu. Exempel: <i>"42, 42, 42, 42, 42, 43, 42, 42. Interrupt. 42, 42, 42, 42. Brk"</i>

3. <b>På ruinens brant</b>: Det står nu klart för programmeraren att hans förstånd inte kan omfatta problemet. Världen är skev och overklig, saker tycks inte längre hänga ihop. Ifrågasättandet av det som tagits för givet kan spåras i meddelandenas ton. Exempel: <i>"Impossible error."</i>, <i>"***Shit has happened***"</i>, <i>"Yeah, right."</i> (det sist är ett autentiskt meddelande från någon äldre version av ICQ)

4. <b>Bortom fönuftets gränser</b>: Det spelar ingen roll längre. Det finns ingen räddning och även om det fanns det bryr vi oss inte. Vi är förlorade, borta, desillusionerade från våra föreställningar om programutvecklingsmetodik. Bortom detta finns inte buggar, bara kaserad kod. Exempel: <i>"fisksoppa"</i>, <i>"fyrmanstält"</i>, <i>"king edward"</i>

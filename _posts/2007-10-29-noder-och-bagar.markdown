---
layout: post
status: publish
published: true
title: Noder och bågar
author: Per Liedman
author_login: per
author_email: per@liedman.net
author_url: http://per.liedman.net
wordpress_id: 109
wordpress_url: http://per.liedman.net/?p=109
date: 2007-10-29 16:59:58.000000000 +01:00
categories: []
tags: []
comments: []
---
På senaste tiden verkare jag stöta på <a href="http://en.wikipedia.org/wiki/Graph_%28mathematics%29">grafer</a> var jag än vänder mig - alltså inte grafer som kurvor och diagram, utan sådana med noder och bågar, som illustrerar hur diskreta objekt är relaterade till varandra. Är det inte vem som är vän med vem på <a href="http://www.facebook.com">Facebook</a>, så är det artister och hur de liknar varandra på <a href="http://www.last.fm">last.fm</a>. I och med att grafer är ett så grundläggande begrepp inom datavetenskap är det kanske egentligen ingen överraskning att de blir en del av vår vardag i och med att IT i en mängder börjar bli just något väldigt vardagligt.

Trots alla denna data som har formen av grafer, har jag inte hittat så värst många verktyg för att visualisera dem. Alltså fick jag gräva fram lite kunskaper från min studietid, och har skrivit ett enkelt bibliotek för att skapa någorlunda förståndiga bilder av diverse grafer. Metoden bygger på vad jag förstår är den enklaste algoritmen för <a href="http://en.wikipedia.org/wiki/Graph_drawing">grafritning</a>, en metod där man modellerar grafen som ett fysikaliskt system, där noder är elektriskt laddade partiklar (som stöter dem från varandra), och bågarna som fjädrar (som håller dem samman).

När man väl började var det svårt att sluta. Nu har jag grafer över:
<ul>
<li>Artister och hur de hänger ihop, t.ex.: <a href='http://per.liedman.net/wp-content/uploads/2007/10/graph-lastfm-similarartists-nationalteatern.png' title='Artister relaterade till Nationalteatern'>Artister relaterade till Nationalteatern</a></li>
<li><a href='http://per.liedman.net/wp-content/uploads/2007/10/graph-lastfm-neighbours-liedman.png' title='Grannar på Last.fm'>Grannar på Last.fm</a>, namnet inom parentes är respektive användares mest spelade artist</li>
<li><a href='http://per.liedman.net/wp-content/uploads/2007/10/graph-ror-2007.png' title='Hur folk hänger ihop RoR'>Hur folk hänger ihop Ralf-o-Rolf</a></li>
<li><a href='http://per.liedman.net/wp-content/uploads/2007/10/graph-fb-friends-liedman.png' title='Mina vänner på Facebook'>Mina vänner på Facebook</a></li>
<li>Hur olika webbplatser hänger ihop med varandra. Tenderar dock att bli oerhört rörigt, så jag väntar med något bra exempel på hur det kan se ut.
</ul>

I händelse av att någon skulle vilja ha programkoden för egna experiment, så finns den här: <a href='http://per.liedman.net/wp-content/uploads/2007/10/springsgraphtar.gz' title='Källkod för grafritning'>SpringsGraph.tar.gz</a>; kräver <a href="http://www.python.org">Python</a> 2.5, <a href="http://www.pygame.org/">pygame</a> samt <a href="http://www.crummy.com/software/BeautifulSoup/">Beautiful soup</a>.

Fler förslag på vad jag kan visualisera som en graf? Hör av dig.

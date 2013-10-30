---
layout: post
status: publish
published: true
title: Noder och bÃ¥gar
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
PÃ¥ senaste tiden verkare jag stÃ¶ta pÃ¥ <a href="http://en.wikipedia.org/wiki/Graph_%28mathematics%29">grafer</a> var jag Ã¤n vÃ¤nder mig - alltsÃ¥ inte grafer som kurvor och diagram, utan sÃ¥dana med noder och bÃ¥gar, som illustrerar hur diskreta objekt Ã¤r relaterade till varandra. Ã„r det inte vem som Ã¤r vÃ¤n med vem pÃ¥ <a href="http://www.facebook.com">Facebook</a>, sÃ¥ Ã¤r det artister och hur de liknar varandra pÃ¥ <a href="http://www.last.fm">last.fm</a>. I och med att grafer Ã¤r ett sÃ¥ grundlÃ¤ggande begrepp inom datavetenskap Ã¤r det kanske egentligen ingen Ã¶verraskning att de blir en del av vÃ¥r vardag i och med att IT i en mÃ¤ngder bÃ¶rjar bli just nÃ¥got vÃ¤ldigt vardagligt.

Trots alla denna data som har formen av grafer, har jag inte hittat sÃ¥ vÃ¤rst mÃ¥nga verktyg fÃ¶r att visualisera dem. AlltsÃ¥ fick jag grÃ¤va fram lite kunskaper frÃ¥n min studietid, och har skrivit ett enkelt bibliotek fÃ¶r att skapa nÃ¥gorlunda fÃ¶rstÃ¥ndiga bilder av diverse grafer. Metoden bygger pÃ¥ vad jag fÃ¶rstÃ¥r Ã¤r den enklaste algoritmen fÃ¶r <a href="http://en.wikipedia.org/wiki/Graph_drawing">grafritning</a>, en metod dÃ¤r man modellerar grafen som ett fysikaliskt system, dÃ¤r noder Ã¤r elektriskt laddade partiklar (som stÃ¶ter dem frÃ¥n varandra), och bÃ¥garna som fjÃ¤drar (som hÃ¥ller dem samman).

NÃ¤r man vÃ¤l bÃ¶rjade var det svÃ¥rt att sluta. Nu har jag grafer Ã¶ver:
<ul>
<li>Artister och hur de hÃ¤nger ihop, t.ex.: <a href='http://per.liedman.net/wp-content/uploads/2007/10/graph-lastfm-similarartists-nationalteatern.png' title='Artister relaterade till Nationalteatern'>Artister relaterade till Nationalteatern</a></li>
<li><a href='http://per.liedman.net/wp-content/uploads/2007/10/graph-lastfm-neighbours-liedman.png' title='Grannar pÃ¥ Last.fm'>Grannar pÃ¥ Last.fm</a>, namnet inom parentes Ã¤r respektive anvÃ¤ndares mest spelade artist</li>
<li><a href='http://per.liedman.net/wp-content/uploads/2007/10/graph-ror-2007.png' title='Hur folk hÃ¤nger ihop RoR'>Hur folk hÃ¤nger ihop Ralf-o-Rolf</a></li>
<li><a href='http://per.liedman.net/wp-content/uploads/2007/10/graph-fb-friends-liedman.png' title='Mina vÃ¤nner pÃ¥ Facebook'>Mina vÃ¤nner pÃ¥ Facebook</a></li>
<li>Hur olika webbplatser hÃ¤nger ihop med varandra. Tenderar dock att bli oerhÃ¶rt rÃ¶rigt, sÃ¥ jag vÃ¤ntar med nÃ¥got bra exempel pÃ¥ hur det kan se ut.
</ul>

I hÃ¤ndelse av att nÃ¥gon skulle vilja ha programkoden fÃ¶r egna experiment, sÃ¥ finns den hÃ¤r: <a href='http://per.liedman.net/wp-content/uploads/2007/10/springsgraphtar.gz' title='KÃ¤llkod fÃ¶r grafritning'>SpringsGraph.tar.gz</a>; krÃ¤ver <a href="http://www.python.org">Python</a> 2.5, <a href="http://www.pygame.org/">pygame</a> samt <a href="http://www.crummy.com/software/BeautifulSoup/">Beautiful soup</a>.

Fler fÃ¶rslag pÃ¥ vad jag kan visualisera som en graf? HÃ¶r av dig.

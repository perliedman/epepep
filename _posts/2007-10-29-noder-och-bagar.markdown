---
layout: post
status: publish
published: true
title: Noder och b&aring;gar
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
P&aring; senaste tiden verkare jag st&ouml;ta p&aring; <a href="http:&#47;&#47;en.wikipedia.org&#47;wiki&#47;Graph_%28mathematics%29">grafer<&#47;a> var jag &auml;n v&auml;nder mig - allts&aring; inte grafer som kurvor och diagram, utan s&aring;dana med noder och b&aring;gar, som illustrerar hur diskreta objekt &auml;r relaterade till varandra. &Auml;r det inte vem som &auml;r v&auml;n med vem p&aring; <a href="http:&#47;&#47;www.facebook.com">Facebook<&#47;a>, s&aring; &auml;r det artister och hur de liknar varandra p&aring; <a href="http:&#47;&#47;www.last.fm">last.fm<&#47;a>. I och med att grafer &auml;r ett s&aring; grundl&auml;ggande begrepp inom datavetenskap &auml;r det kanske egentligen ingen &ouml;verraskning att de blir en del av v&aring;r vardag i och med att IT i en m&auml;ngder b&ouml;rjar bli just n&aring;got v&auml;ldigt vardagligt.

Trots alla denna data som har formen av grafer, har jag inte hittat s&aring; v&auml;rst m&aring;nga verktyg f&ouml;r att visualisera dem. Allts&aring; fick jag gr&auml;va fram lite kunskaper fr&aring;n min studietid, och har skrivit ett enkelt bibliotek f&ouml;r att skapa n&aring;gorlunda f&ouml;rst&aring;ndiga bilder av diverse grafer. Metoden bygger p&aring; vad jag f&ouml;rst&aring;r &auml;r den enklaste algoritmen f&ouml;r <a href="http:&#47;&#47;en.wikipedia.org&#47;wiki&#47;Graph_drawing">grafritning<&#47;a>, en metod d&auml;r man modellerar grafen som ett fysikaliskt system, d&auml;r noder &auml;r elektriskt laddade partiklar (som st&ouml;ter dem fr&aring;n varandra), och b&aring;garna som fj&auml;drar (som h&aring;ller dem samman).

N&auml;r man v&auml;l b&ouml;rjade var det sv&aring;rt att sluta. Nu har jag grafer &ouml;ver:
<ul>
<li>Artister och hur de h&auml;nger ihop, t.ex.: <a href='http:&#47;&#47;per.liedman.net&#47;wp-content&#47;uploads&#47;2007&#47;10&#47;graph-lastfm-similarartists-nationalteatern.png' title='Artister relaterade till Nationalteatern'>Artister relaterade till Nationalteatern<&#47;a><&#47;li>
<li><a href='http:&#47;&#47;per.liedman.net&#47;wp-content&#47;uploads&#47;2007&#47;10&#47;graph-lastfm-neighbours-liedman.png' title='Grannar p&aring; Last.fm'>Grannar p&aring; Last.fm<&#47;a>, namnet inom parentes &auml;r respektive anv&auml;ndares mest spelade artist<&#47;li>
<li><a href='http:&#47;&#47;per.liedman.net&#47;wp-content&#47;uploads&#47;2007&#47;10&#47;graph-ror-2007.png' title='Hur folk h&auml;nger ihop RoR'>Hur folk h&auml;nger ihop Ralf-o-Rolf<&#47;a><&#47;li>
<li><a href='http:&#47;&#47;per.liedman.net&#47;wp-content&#47;uploads&#47;2007&#47;10&#47;graph-fb-friends-liedman.png' title='Mina v&auml;nner p&aring; Facebook'>Mina v&auml;nner p&aring; Facebook<&#47;a><&#47;li>
<li>Hur olika webbplatser h&auml;nger ihop med varandra. Tenderar dock att bli oerh&ouml;rt r&ouml;rigt, s&aring; jag v&auml;ntar med n&aring;got bra exempel p&aring; hur det kan se ut.
<&#47;ul>

I h&auml;ndelse av att n&aring;gon skulle vilja ha programkoden f&ouml;r egna experiment, s&aring; finns den h&auml;r: <a href='http:&#47;&#47;per.liedman.net&#47;wp-content&#47;uploads&#47;2007&#47;10&#47;springsgraphtar.gz' title='K&auml;llkod f&ouml;r grafritning'>SpringsGraph.tar.gz<&#47;a>; kr&auml;ver <a href="http:&#47;&#47;www.python.org">Python<&#47;a> 2.5, <a href="http:&#47;&#47;www.pygame.org&#47;">pygame<&#47;a> samt <a href="http:&#47;&#47;www.crummy.com&#47;software&#47;BeautifulSoup&#47;">Beautiful soup<&#47;a>.

Fler f&ouml;rslag p&aring; vad jag kan visualisera som en graf? H&ouml;r av dig.

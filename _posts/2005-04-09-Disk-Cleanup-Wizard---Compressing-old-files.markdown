---
layout: post
status: publish
published: true
title: Disk Cleanup Wizard - Compressing old files
author: Per Liedman
author_login: per
author_email: per@liedman.net
author_url: http://per.liedman.net
wordpress_id: 15
wordpress_url: http://www.liedman.netdatorer-&amp;-teknik/disk-cleanup-wizard---compressing-old-files/
date: 2005-04-09 15:26:32.000000000 +02:00
categories: []
tags: []
comments: []
---
Jag hatar att f&aring; slut p&aring; diskutrymme, och framf&ouml;r allt n&auml;r det tar slut precis n&auml;r man h&aring;ller p&aring; med n&aring;got viktigt eller n&aring;got som m&aring;ste g&aring; fort. D&auml;rf&ouml;r &auml;r <a href="http:&#47;&#47;support.microsoft.com&#47;default.aspx?scid=kb;en-us;310312">Disk cleanup<&#47;a>, som finns i senare versioner av Windows, ett fint hj&auml;lpmedel f&ouml;r att st&auml;da upp det v&auml;rsta lite snabbt. Oftast har webbl&auml;sare och andra program sparat en massa m&ouml;g som man egentligen alls &auml;r intresserad av, och precis det rensas bort.

Tyv&auml;rr har <i>Disk cleanup<&#47;i> &auml;ven den m&auml;rkliga id&eacute;n att gamla filer b&ouml;r komprimeras, en &aring;tg&auml;rd som n&auml;stan aldrig verkar spara n&aring;got diskutrymme och dessutom tar ungef&auml;r ett &aring;r p&aring; sig att ens ber&auml;kna hur mycket utrymme som skulle sparas (f&ouml;ga &ouml;verraskande, eftersom varenda fil p&aring; h&aring;rddisken antagligen m&aring;ste unders&ouml;kas). <a href="http:&#47;&#47;www.microsoft.com">Microsoft<&#47;a> verkar  inte ha insett problemet, fast det i mina &ouml;gon f&ouml;rtar hela po&auml;ngen med att &ouml;verhuvudtaget ha en Disk cleanup-pryl; det g&aring;r ju snabbare att rensa manuellt.

Som tur &auml;r kan man st&auml;nga av compressed files-delen av Disk cleanup med ett registerhack. S&aring; h&auml;r g&ouml;r man:
<ol>
<li>&Ouml;ppna HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion \Explorer\VolumeCaches\Compress old files i RegEdit<&#47;li><li>Ta bort alla v&auml;rden under nyckeln<&#47;li>
<&#47;ol>

G&ouml;r det. G&ouml;r det nu!

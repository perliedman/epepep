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
Jag hatar att fÃ¥ slut pÃ¥ diskutrymme, och framfÃ¶r allt nÃ¤r det tar slut precis nÃ¤r man hÃ¥ller pÃ¥ med nÃ¥got viktigt eller nÃ¥got som mÃ¥ste gÃ¥ fort. DÃ¤rfÃ¶r Ã¤r <a href="http://support.microsoft.com/default.aspx?scid=kb;en-us;310312">Disk cleanup</a>, som finns i senare versioner av Windows, ett fint hjÃ¤lpmedel fÃ¶r att stÃ¤da upp det vÃ¤rsta lite snabbt. Oftast har webblÃ¤sare och andra program sparat en massa mÃ¶g som man egentligen alls Ã¤r intresserad av, och precis det rensas bort.

TyvÃ¤rr har <i>Disk cleanup</i> Ã¤ven den mÃ¤rkliga idÃ©n att gamla filer bÃ¶r komprimeras, en Ã¥tgÃ¤rd som nÃ¤stan aldrig verkar spara nÃ¥got diskutrymme och dessutom tar ungefÃ¤r ett Ã¥r pÃ¥ sig att ens berÃ¤kna hur mycket utrymme som skulle sparas (fÃ¶ga Ã¶verraskande, eftersom varenda fil pÃ¥ hÃ¥rddisken antagligen mÃ¥ste undersÃ¶kas). <a href="http://www.microsoft.com">Microsoft</a> verkar  inte ha insett problemet, fast det i mina Ã¶gon fÃ¶rtar hela poÃ¤ngen med att Ã¶verhuvudtaget ha en Disk cleanup-pryl; det gÃ¥r ju snabbare att rensa manuellt.

Som tur Ã¤r kan man stÃ¤nga av compressed files-delen av Disk cleanup med ett registerhack. SÃ¥ hÃ¤r gÃ¶r man:
<ol>
<li>Ã–ppna HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion \Explorer\VolumeCaches\Compress old files i RegEdit</li><li>Ta bort alla vÃ¤rden under nyckeln</li>
</ol>

GÃ¶r det. GÃ¶r det nu!

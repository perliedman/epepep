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
Jag hatar att få slut på diskutrymme, och framför allt när det tar slut precis när man håller på med något viktigt eller något som måste gå fort. Därför är <a href="http://support.microsoft.com/default.aspx?scid=kb;en-us;310312">Disk cleanup</a>, som finns i senare versioner av Windows, ett fint hjälpmedel för att städa upp det värsta lite snabbt. Oftast har webbläsare och andra program sparat en massa mög som man egentligen alls är intresserad av, och precis det rensas bort.

Tyvärr har <i>Disk cleanup</i> även den märkliga idén att gamla filer bör komprimeras, en åtgärd som nästan aldrig verkar spara något diskutrymme och dessutom tar ungefär ett år på sig att ens beräkna hur mycket utrymme som skulle sparas (föga överraskande, eftersom varenda fil på hårddisken antagligen måste undersökas). <a href="http://www.microsoft.com">Microsoft</a> verkar  inte ha insett problemet, fast det i mina ögon förtar hela poängen med att överhuvudtaget ha en Disk cleanup-pryl; det går ju snabbare att rensa manuellt.

Som tur är kan man stänga av compressed files-delen av Disk cleanup med ett registerhack. Så här gör man:
<ol>
<li>Öppna HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion \Explorer\VolumeCaches\Compress old files i RegEdit</li><li>Ta bort alla värden under nyckeln</li>
</ol>

Gör det. Gör det nu!

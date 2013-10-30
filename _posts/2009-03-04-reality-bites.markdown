---
layout: post
status: publish
published: true
title: Reality Bites
author: Per Liedman
author_login: per
author_email: per@liedman.net
author_url: http://per.liedman.net
wordpress_id: 135
wordpress_url: http://per.liedman.net/?p=135
date: 2009-03-04 18:43:51.000000000 +01:00
categories:
- '1'
tags: []
comments: []
---
I'm a software developer. I like abstractions, I enjoy mentally putting things in little boxes, structuring my mental model of the world, or at least the model of the problem I'm currently struggling with. I don't know if it's a requirement, but if you're a developer, it certainly helps to be border-lining to obsessive about knowing how stuff works, in excruciating detail.

Having said that, I find it fascinating how problems in programming constantly make you hit your head against the wall of reality - the wall located where pretty, simple and linear abstractions meet the real world. You know, the real world which refuses to be dumbed down into simple rules, and even when you <em>think</em> you've trapped it with you're rules, always breaks free with new twists and turns that you hadn't thought of. This is sort of the essence - problems that I've been working with more or less since I started programming, problems which also appear very benign from a casual viewpoint, that keep coming back, and simply refuse to be solved in a way such that you can put them behind you.

<strong>Time</strong> is the first and most obvious case. That something as fundamental and trivial (you learn to read the watch when you're what? Five? Six?) can be so complicated and easy to get wrong is truly fascinating. And then I haven't even mentioned dates yet. Just starting to think about dates will get any programmer into trouble. Before you know it, you're knee deep in Gregorian calendars and leap years - and even then, you won't get it right. In fact, I'd go so far as saying that any non-trivial date/time calculation in software will contain at least one bug, or one special case that you hadn't really thought of. 

Once again, then I haven't even mentioned <em>time zones</em> yet. Time zones, combined with daylight savings time, is the real killer, if you by pure miracle got the first date calculations right. At the company were I worked before, we had a standing joke two times a year - was this going to be the first day lights savings switch in the company's history where we didn't encounter a bug related to it? From what I can recall, we never had a bug free switch (in five years!).

<strong>Maps</strong>, or perhaps rather geographic locations, is the second thing that springs to mind as a seemingly straightforward thing, that just never ever gets right. 

From the day we learned how to use a two dimensional map, I actually think we're doomed into living in the wrong paradigm. In grade school we learn that north is up on the map, and using a ruler to measure distances on it is the way to go. Sure, both work. Sometimes. But equally often, it just almost works, it's almost true, kind of. "Almost true", deeply ingrained in your mind, happens to be a perfect and never ending source of interesting and subtle software bugs.

Add to that the fact that the earth isn't really a sphere, but almost, and while we have attempted to meaure its non-spheriness, we came up with several conflicting measurements, all giving slightly different results when you try to express where you are on this not-really-a-sphere thing. Sometimes, different measurements are mixed, and you will have to use completely non-trivial transformations to convert from one to the other, but those transformations only work for very special circumstances.

Even if you get it right, someone will probably want to calculate the distance from where you think you are to some other point, which isn't at all trivial on a sphere. But it wasn't a sphere, right? Yep, right - not a sphere, and that makes it just even worse. Luckily, I (and probably not you) don't need the last kind of precision very often, but that doesn't help, because we will <em>still</em> try to use a ruler (or its digital equivalent) to measure the distance on a map - which won't work, even if the teacher in fourth grade said it would.

<strong>Character encoding</strong> is my last example. Yes, getting characters to show up on your screen, more or less. Again, something very mundane and something a non-developer would take for granted. And yet, this is something that has been a problem in just about any application I've written, or seen being written, or used, for I don't know how long. I guess being a swede, using the funny Ã¥, Ã¤, Ã¶ characters a lot (or "ÃƒÂ¥, ÃƒÂ¤ and ÃƒÂ¶", as I've learnt to know them from years of UTF-8/ISO-8859 mangling), doesn't help, since you're so much more exposed to the problem.

Closing up, I want to attempt finding something that these three problems have in common, something that make seemingly simple things so very complicated. My first guess would be that its the perceived simplicity that is the core in all three - all are stuff that we in our daily lives take for granted, talk about while at the same time not paying much attention to the details: we look at our watches, make appointments and write them in our calendars, decide to meet at certain locations and talk about how far it is to places. We never ever think about the underlying details and complexities while doing this, it's all very intuitive to us. On the other hand, I think it's this very intuition that trips us when developing software; the fact that we think we know this very well gets in the way details (that most of us actually don't know).

Also, all three share that they in some way involve problems regarding frame of reference: time zone and daylight savings time problems are hard since you very easily get confused about what is fixed and what is relative. The map problems are very much the same - what is absolute in one frame of reference ("up", "north", "distance", etc.), does not necessarily translate to some absolute in another, and what you're doing is switching frame of reference, if it's going from a projected map to WGS84, or if it's transforming between two geodetic references. Character encoding, and translation from one encoding to another, is also only meaningful if you keep track of your frame or reference ("current encoding") through every step of the process - something which is very obviously much easier said than done.

At first, I also thought about adding the theory of relativity to the problems above. I decided against it, since it's really not something you deal with every day, and it's also far beyond my field of expertise. Interestingly enough though, it also talks about things we perceive as intuitive (time, length and weight being more or less constant) and turns it on its head, although more profoundly than the examples above. Also, the solution very much lies in keeping track of your frame of reference. 

This is also the conclusion: a perceived intuitivity about a problem, combined with transitions between different frames of reference, makes for a problem that you will come back to again and again.

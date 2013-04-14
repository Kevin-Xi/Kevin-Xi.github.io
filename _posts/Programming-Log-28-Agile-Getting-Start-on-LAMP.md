---
title: Programming Log 28: Agile, Getting Start on LAMP
date: '2013-3-12'
categories: Learning
tags: [Learning, Agile, LAMP]
---

Today afternoon I make some notes of the book *The Art of Agile Development*. Although I have read this book twice, it still hard to understand when you never have group cooperation experience.

An exciting thing today is that I installed the *LAMP* on my computer and make it worked. I wrote a simple *HTML* page of some pictures and texts on it.

When I add images,it at first can show. And I try to modify the authority of image files:

	sudo chmod 777 try.gif

And it worked. Why?

But when I tried to install *Mod_python* to bind python with Apache, the luck went away. At first I can't find the route of *apxs*, then I realized I didn't have one. and the *make* has failed because a missing header "*apr.h*".

When I first to learn the *make* tool suit, although it does make things easy, but I hold the view that a little project needn't it, and for a big project, it has too much to consider about that make "easy" no sense. Maybe just again I took a screwdriver as a hammer.

To sum up, I spent **3 hours** on programming today, and totally **101 hours**.
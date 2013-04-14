---
title: Programming Log 1: Thread, Different of Perl and Python
date: '2013-2-12'
categories: Learning
tags: [Learning, python, perl, java]
---

I learned something about **thread** with *Introudction to JAVA Programming* this afternoon. The thread stratrgy of Java is strange (I wonder there may have better design besides **Thread Pools, Locks, Blocking Queues, Semaphores, Resource Ordering, Synchronize**. Is there necessary that all this stuff come out together just for a "thread"?)
I have record some question:

+ How to process a the *resource ordering*?
+ what consequence of not using *GUI event dispatch thread*?
+ Why should wrap loop in try-catch block when a *sleep()* invoked? Is that indicate that the exception handling will deal in another thread isolating to the loop?
+ The essential differents among *abstract class*, *interface* and *ordinary super class*. It seems that *abstract class* declares "what it is?" and *interface* declares "how it appears (what attribute does it have)?"


The differents between python and perl are making things interesting during my learning. Some usage of perl is quite dirty. 

+ I don't know how exactly the *. operator*, which use to concatenate two strings together, work. For example:
	'hello world'."\n"
   is equals to
   	"hello world\n"
   , while 
   	"hello world".'\n'
   is equals to
   	'hello world\n'
   , why? Who decide whether or not the "n" escape?


To sum up, I spent **2 hours** on programming today, and totally **3 hours**. Since I try to go to bed at 2300, I will not program python today and, for compensate, try to get up early tomorrow.
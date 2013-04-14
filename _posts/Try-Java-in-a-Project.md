---
title: Try Java in a Project
date: '2012-12-29'
categories: Project
tags: [Project, Java]
---

The last four days, I devoted all of my free time to working on our group of the Java class final design. It is called MouseGesture, a little always-on-top frame that can catch your mouse trace and identify the trace to "realize" your intention(The first version can only open executable file).


During this experience, I realize that Java is not a good choice for system software. First I design the software should listen the mouse event in backstage, but I found it's difficult to instant, because a *hook* coded by C++ should provided its function to JNI. At first, I tried to modify the DLL file myself but it's hard to imitate without know nothing about JNI and the very basement of the system. I also have a long time to compile the DLL file: the Code::Blocks give me a 32 bits version which cannot aplied on my station and Visual Studio's option is so numberous enough to confuse a new hand.


So I decide to modify the design, let there be a tiny main frame include "Setting" & "Catching" button which will call the subframe when it has been pressed.


I encounrted another problem, that is when I run the application in Eclipse, it return the project menu as its root route, but when I write a *.bat* file to run this application in command line, I should change to the *bin* menu and use 

	java gui.mainframe

to do the same thing, so the program will failed when it read the setting file and can't find correct route. I use some dirty code to solve it, I hate to do that.


The authority is also a problem. I should call *nircmd* with argument *elevate* but not *cmd* to excute *reg add* command in Windows 7, and sadly, this will not work on Windows XP and below.


If I intend to transplant this application to Linux platform, I really don't like to image it: the program should detect which platform itself locate to decide which code will execute. So in this way, for me now as a new hand, the JVM is useless when the application should work as a system software.


I have really learn a lot in this project. Next time I should get a general acquaintance to a language before make disicion. Java has a lot of wonderful feature to bring code into life.

TODO with this application:

+ Call system default program to open any file & menu
+ Self-define mouse gesture
+ Show trace of cursor when drag mouse
+ Optimize algorithm of recognition
+ Cross-platform
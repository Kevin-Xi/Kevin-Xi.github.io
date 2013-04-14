---
title: Programming Log 15: Java GUI, Play with Python
date: '2013-2-26'
categories: Learning
tags: [Learning, Java, GUI. python]
---

I learned some about *Menus* and *Toolbars* in the morning. I have a question of the *JPopupMenu*.

	jTextArea1.addMouseListener(new MouseAdapter(){
		public void mousePressed(MouseEvent e){//The comment of this line is "For Motif", what's the meaning?
			showPopup(e);
		}

		public void mouseReleased(MouseEvent e){//The comment of this line is "For Windows", what's the meanings? Is that means different OS has different trigger? If so, why JVM don't unified them and what OS is "Motif"?
			showPopup(e);
		}
	});

	private void showPopup(java.awt.event.MouseEvent evt){
		if(evt.isPopupTriggrt()){
			jPopupMenu1.show(evt.getComponent(),evt.getX(),evt.getY());
		}
	}


And I again, found two logic bug in my statistics program *stage.py*. I didn't minus the day I already spent off the ETA, and the calculate way of *workdelta* is wrong. And at last I found the first "bug" is not wrong, I have already consider about it. Oh my brain...


I finished reading chapter 3 of *Diving into Python* and feel good.


I started reading chapter 4 afternoon, during its went on, I understood the code ever senseless to me. Learning in this way is cool and make me feel achievement.


To sum up, I spent **4 hours** on programming today, and totally **62 hours**.
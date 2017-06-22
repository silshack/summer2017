---
layout: post
author: Ibbi2010
title: "Final Project"
---

Here's the code for my Final Game APP Project:
<iframe src="https://trinket.io/embed/python/4d2408d2c0" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

Reflection:
The most excruciatingly painful thing for any perfectionist is, when they create anything less than perfect. This has been something I am facing again and again during this semester. I really wanted to come up with something exactly as I had envisioned for my final project but I feel there are many areas which still need a lot of work and improvement. 

Conception of my Final Project Idea:
I chose a game App for my final project because I love “turtle”. I have always enjoyed working and creating drawings with turtle on trinket. I wanted to create a simple run and chase game after watching the videos. I thought these videos can become a very good resource for me and keeping it simple would ensure that I will be able to come up with something substantially suitable for a game.

Perseverance:
Why Baseball field as a background? My decision of making baseball field as my game background sketch was a deliberate decision. The inspiration behind this was my 10 year old son(nael) , who started playing baseball at the age of 7, and have been steadfastly playing every game of every season, showing up for each and every practice with just one goal in mind, to make a home run one day.  His dream came true few days ago in the quarterfinals of his tournament but I had already started working on this project. The idea was to get him to do a home run in this game.

Basic Sketch:
I really enjoyed drawing the baseball field , it took me only few hours to come up with what you see in the game. It was not all easy and is still not perfect but I think its decent for some primitive run and chase game.

My resources:
For the drawing and everything in the instructions.py is my own code. I took major help from the game videos and it helped me immensely to create extension of custom turtle classes. I did some necessary changes to customize the code according to my game needs. 
I also had a huge help from my group especially Brian, who at a number of times came to my rescue by pointing out to some silly stuff which was messing up with my program. Like when I was not able to understand why I am not able to transfer the image and he showed me that I was omitting a space in file name. Seriously!
Also a huge credit to “Elliot Hauser” for bearing with me and giving me tremendous help and hints for my project. You were supposed to lend your half hour but ended up spending almost an hour on my program. Thank you so much! 

Process:
After I did my sketch, I made a runner (nael) and created tagger turtle class and the base turtle classes with special attributes and custom functions for intersecting and flashing the bases. I achieved all this in a relatively small amount of time and was really happy about my progress. So much so that I started making my milestones ambitiously more than what was needed at that point.
Then there were some road blocks, at first I was not able to make my reset function work (which I am still working on) then my “Help” button was not working properly, I was overlooking a minor detail.
I took longest in deciding how to implement my in creasing difficulty levels in the game. One idea was to create a timer and decrease the allotted time for the runner to make a home run. Another idea was to increase the number of tag turtles with every level. I decided to go with the timer option. I did not want to overcrowd my field, also I already had an intersect function going on with the bases so I decided not to include the tag function (i.e intersecting with the tag turtles). I did not want it t be too much for me to handle. So the tag turtles in the field are essentially to increase the stress level for the runner. I intentionally kept their speed to low at “2”.
So while going through different game Apps from the students of last semester, I came across an App which had the timer exactly like one I wanted for my game. That person had created an extension of turtle class for a timer. (“I can provide the reference for this”) I took the idea from there and modified the code suitable for my App. The only problem was that I could not get to stop the timer when the all the bases were hit (which is what I wanted the game to do). I tried multiple ways but honestly I think I was not even going in the right direction. So I asked for Elliot’s help and he got me out of this dilemma.
By now my game had started to look like a real game at least. The next steps were to make levels.
Elliot had given me some very straightforward hints and I knew exactly what route to take to make at least 2 levels of increasing difficulty. The main challenge was to reset everything. I don’t know why it took me so long but I was able to reset the tag turtles, my runner and even the screen settings. The only problem I had was to reset the bases. There is so much going on in the Base class that it showed errors no matter what I tried. At one point I don’t know what I did with it that my whole App got crippled. This point was really frustrating and overwhelming for me. I was desperate not to fail and let myself and especially Elliot down, who had given me such clear instructions.  As I write all this, I am still working on this problem. I hope sometime during the night or by tomorrow, I might come up with my solution. 
In the meanwhile, I decided to write my reflection to just look through my journey and feel a little better about myself.

Milestones:
This is what my last milestone list looked like
My Revised Milestones list
- [x] Get my Runner “image” transferred and figure what’s stopping the image transfer
- [x] Get my “Help” function to work properly
- [ ] Get “restart” to work
- [x]	Figure out a way to stop timer after home run
- [x]	Create setup screen
- [x]	User Instructions
- [x]	Create Runner
- [x]	Make Tag turtles Class
- [x] Make bases (Base Class)
- [x] Get the bases to flash after intersecting with nael
- [x]	Organize my code
- [x]	Make timer
- [x]	Make win screen
- [x]	Make ‘ you lost’ screen
- [x]	Get my check position to work
- [x] Create levels
- [x] Display User information like time and level
- [ ] Get levels to work properly
- [ ] Use of dictionaries(e.g in levels,score etc)

I am still not satisfied but I think I have been able to pull off something to share with the class. I would want to keep working on my strtch goals and make this App a little more challenging and interesting by involving the Tag turtles to perform some action too, like tagging and reducing the lives or chances of runner to make it to "Home" . I would want each and every component of my game to work perfectly ,with a purpose and without any error or bug.

New Things Learnt:
Along the way, I did learn many new things, like how to add an image, setting a timer clock and manipulating it through various methods, creating turtle class extension and emotionally I discovered my tenacity and resilience.

My Future Goals:
I still have six months before I start my Masters program. I intend to utilize all this time in improving my skills. I will touch base with Elliot to find out the ways and strategy to stay  a disciplined learner. Meet ups will be one way to keep me engaged and connected but I do want to indulge in some active learning. No matter how much trouble I have been through, I really like Python and want to keep excelling at it. 






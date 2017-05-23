---
layout: post
author: samsr31
title: "Sam's Logical Turtle Exercise"
---

Here is my program for the logical turtle exercise:


<iframe src="https://trinket.io/embed/python/79fd346189" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

Reflection:
Ok, so I had a whole little drawing program which I wrote, which checked all the boxes for this assignment, and which I thought was creative enough.  But, as I wrote the reflection for that, I got thinking about where I could go next with what I had made, and I latched onto the idea you see here.  This is a rudimentary recreation of the game Battleship!.  The game asks you for coordinate prompts, and then tells you whether you hit a target or not with either a white or red circle on the map.  You have ten tries to hit the three targets.
    I didn’t think this was something I would finish in one night, and so I didn’t take notes about reflections and learning moments while I was working on it.  Looking back on it though, what difficulties and roadblocks did I have?  Drawing the game board was simple enough, if time consuming.  Figuring out the conditional statements was probably the hardest part, and I feel like they’re still probably inefficiently written.  I used the “pass” statement to help build the structure of the statements without making them do anything, and then worked backwards to fill in each potential condition.  I also tested it repeatedly, entering odd combinations of numbers to find ways to break it.
    Going forward, I’d like to find a way to change the target numbers each game.  As is, there are three static targets hardwired in.  I think what I’d need to do next is find a way to generate a set of random coordinates, and then set up the if statement such that if any of those coordinates were struck, it counted as a hit, rather than setting up a long “if...elif” statement to cover each possible coordinate.

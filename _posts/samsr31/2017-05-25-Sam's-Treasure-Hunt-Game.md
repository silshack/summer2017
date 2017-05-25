---
layout: post
author: samsr31
title: "Sam's Treasure Hunt Game"
---

Here is my Treasure Hunt assignment game:

<iframe src="https://trinket.io/embed/python/c2dd7f2eb5" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>


I had a few main ideas I wanted to implement going into this assignment.  First, I wanted to try out screen.onclick again, so that the player could click where they wanted to try to find the treasure.  Second, I wanted to add some more character and user convenience to the program, since for the last few days I’d been focusing on recreating someone else’s board game, and had not put a lot of text prompts into that program to help explain what was going on.  Lastly, once I had the main structure of the game set up, I wanted to experiment with changing difficulty settings, and with creating a system to change tina’s color along a scale from green to red, depending on how close she was to the treasure.
 
The “onscreenclick” was relatively simple to set up, and I ended up putting a lot of my actions into that one function.  Inside that function, the program checks the distance between the click coordinate and the treasure coordinate, outputs that distance into a global variable, tells tina to go to the click coordinate and make a stamp, varies tina’s color based on the distance from the click and the treasure, and prints to the user a statement telling them how close they are.  With most of the program happening inside that one function, the “while” loop at the end mainly just keeps track of whether the player has gotten within range of the treasure yet, by comparing “distance” to a set value.
 
As for usability and color, I had some fun coming up with a “setting” for the treasure hunt - a desert island!  I also made a point of actually giving some instructions before everything got started, and giving regular text feedback on how the player was doing.
 
Once I had everything running nicely, I added a choice for the player before the game got started, which allowed them to choose a difficulty.  This then led to a simple multiplication of some of the variables involved, to make either a larger or smaller play area, with a larger or smaller possible range of treasure locations, and a more or less forgiving range for finding the treasure.  The one thing that stopped me up was getting tina’s varying colors to feel just right.  Upon seeing in the “congratulate” function that you can vary a turtle’s color with RGB values, I had an idea to try to use the distance value to vary the colors from red to yellow to green along a continuous gradient.  However, I had a lot of trouble building a function to do this properly.  I’ve been able to get it to be pretty red when it’s far away, and very green when it’s close, but the in-between colors aren’t quite what I want.  Also, even if I find values that work well at one difficulty setting, they usually don’t scale well to the other two settings.  For now, it works alright, but I’m sure there’s a way to get it to slide between the colors the way I’d like even better.

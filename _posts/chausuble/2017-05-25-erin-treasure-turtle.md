--- 
layout: post
author: chausuble
title: "Erin's Treasure and Mine Turtle"
---

<iframe src="https://trinket.io/embed/python/0af9499cd7" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

I wish the first thing I did was to have the game print the treasure's coordinates to make it easier for me to test them!
It would have made testing a lot easier.

The first real thing I did was to work on the win conditions, using what we learned in the videos.
I put the raw_input into an int(), like what we reviewed in class yesterday, and then I could subtract
them from the treasure_x/y values, and do evaluations. I even started adding in the hints based on distance - only
to find that my program didn't run at all because I kept getting a PrintError. I pulled my hair out all night over it!
I searched all over the internet, using Reddit, StackExchange, and more, and nothing was similar to what was happening
to my program. I think eventually, I gave up on internet searching and retyped the program from scratch. Then, one "typo"
I made saved the day. Note to myself for the future: The less-than-or-equal-to symbol is <=, NOT =<.

And then my program worked out fine once I fixed that. I made it easier to read by following the suggestions yesterday
in class, and putting my extended logical conditions under variables. Then, once I figured out how to do that, I just copied
the code and switched around the variables and printed text in order to put the mine in the game, with its hints. I added
things that would make the game easier for me, personally - like coloring in the area where the game is played, changing the
turtle's color as it gets closer to a treasure or mine, and, for the mine, dropping circles in the places where you approach
the mine.

Around this point, I found a problem: Even when you win, it would still go through the mine conditions. So, it would draw
the treasure chest, but still say "You're close to the mine!" and draw a circle on the map. After a while of experimenting,
I realized that the mine conditions should also rely on whether you have won the game or not. Doing that solved another
potential problem - what if the treasure and mine are placed right next to each other? Now, if you land on the treasure,
you automatically win even if you also hit the mine.

The other problem that I only JUST fixed before submitting this post was that I wanted my turtle to leave a path based on where
you've been, but it wouldn't do that unless you got close to a mine. Furthermore, it wouldn't draw the circle showing where
you landed close to a mine the first time you got close to it. It turns out, taking a break and going back to reading the code
works - I realized I should have the "try" statement start with .pendown after receiving the player's instructions.

Finally, I just had fun drawing the treasure chest and explosion. The setheading() function really helps to renavigate your
turtle's direction, which I learned from the teacher's comments on one of my old turtles.

If I were to edit this program some more, I might have an error if you try going out of bounds of the game area, or ensure that
the mine and treasure don't appear in range of each other. I was also considering an optional hint system, where if you keep
missing the treasure, the game will give you the option if you want a hint, and then give you an X or Y coordinate close to where
the treasure is. I tried it, but it kept causing errors that I didn't have time to fix, so I just saved it to a different trinket.
I think it would also be cool to include difficulty settings, like it would add more mines the harder you wanted the game to be.

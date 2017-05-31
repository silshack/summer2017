---
layout: post
author: samsr31
title: "Sam's Clicky Turtle Assignment"
---

Here is my submission for the Clicky Turtle assignment:


<iframe src="https://trinket.io/embed/python/8d3b395e03" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

Reflection:

The most time consuming part of this program for me was definitely drawing and defining the racetrack.  Even keeping everything to multiples of 5 and simple 90 and 180 degree turns, drawing everything out just took a long time, and going back and defining the rectangles where the turtles were allowed to be was pretty time consuming too.  Along the way, I had some issues with getting turtles to draw circles clockwise instead of counterclockwise, but eventually learned how to do this.  As for defining the boundaries of the racetrack, I opted to define big rectangles that approximated the track, rather than finding a way to keep turtles inside the curved portions of the track.
 
Other than drawing everything out, I did not have any major roadblocks.  Most of the time, any issues I ran into were caused by some minor typo, like not putting two == signs in a logical statement, forgetting the colon at the end of a function definition or if statement, or forgetting that calling a function always requires parentheses, even if they’re empty.
 
As it stands, the npc racers you play against make random actions, and have almost zero chance of completing the race.  The program actually isn’t even listening for them to reach the checkpoints and win, since their randomization makes it so unlikely to have happen.  In the future, I would want to work on their AI, so that they have some chance of making it through without just giving them a set path to follow.  I also had some fun ideas for extra animations if the player turtle goes very fast, and a lose condition for if the player hits a racetrack wall going over a certain speed.

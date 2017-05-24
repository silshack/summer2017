---
layout: post
author: samsr31
title: "Sam's Functional Turtle Program"
---

Here is a link to my revised Battleship! game:


<iframe src="https://trinket.io/embed/python/b9402e3499" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

Reflection:
As soon as I started reading the functions chapter I knew that I would be able to use it to expand on the Battleship! game I made for the previous assignment.  Specifically, I wanted to add randomization to the game targets, and I also figured I could turn the markers and counters into functions.  Drawing the circle markers through a function worked easily enough, but trying to move the count down and count up statements into functions produced errors.
Originally, I was using a few lines of code to count down the number of shots the player had left, and to count how many hits they had made.  The code looked like this:
 
```
# counting down the number of shots left
Shots_Left = 10
 
Shots_Left = Shots_Left - 1
```
 
And
 
```
# counting up the number of hits
Hits = 0
 
Hits = Hits + 1
```
 
That way, whenever the conditional statement registered a shot, Shots_Left was lowered by 1, and whenever it registered a hit, Hits was increased by 1.
 
However, I tried to turn these into functions, so that I could define the function once and place it around the conditional statement where needed.  At first I tried this:
 
```
Hits = 0
 
def Hit_Count():
    Hits = Hits + 1
 
Hit_Count()
```
 
But this produced an error saying that I had not defined the ‘Hits’ variable, even when I had.  I then tried adding a parameter to input, like this:
 
 
```
Hits = 0
 
def Hit_Count(Hit):
    Hit = Hit + 1
 
Hit_Count(Hits)
```
 
This worked, and would correctly add 0 + 1 = 1, but it did not then save that number to the ‘Hits’ variable, meaning it did not count upwards upon repeated uses of the function.
After talking about this with Prof. Hauser, I came up with two ways of solving this.  One by referencing the ‘global’ version of the variable ‘Hits’, and one by having the function return it’s result to an outside variable.  Both are shown here:
 
```
Hits = 0
 
def Hit_Count():
  global Hits
  Hits = Hits + 1
 
Hit_Count()
 
# and
 
Hits = 0
 
def Hit_Count(HitNumber):
    HitNumber = HitNumber + 1
    return HitNumber
 
Hits = Hit_Count(Hits)
```
 
Once I got all of these functions working, it was time to try to randomize the game targets.  I did this by using random.randint(1,9) to produce random coordinates with X and Y values between 1 and 9.  I also set up a ‘while’ loop to check that each new coordinate generated was not identical to any of the previous coordinates.  After making sure this worked, I expanded it by plotting out a system to make multiple targets in a row, like the ships from the actual board game.  I started with the largest ship first, since it takes up the most space, and is the most restricted in where it can sit.  The program generates a starter coordinate randomly, and then checks if that coordinate is too close to any of the game board’s edges.  Depending on where the coordinate lands, it chooses an acceptable direction randomly, and then plots out the correct number of additional coordinates in that direction.  The program then does the same for size four, three, and two ships, and also checks that none of their coordinates overlap.
 
The biggest stumbling block I hit with this section of code was it’s size.  If I were to revisit this to improve it, I would want to find a way to condense all of the target coordinates into a set of some sort, and check each entered coordinate against that set.  As is, the program has every single possible target coordinate comparison written out, and it compares the player’s entered coordinate against each of these separately.
 
Another issue I’d like to fix at some point is recording the game board’s state.  As is, after the program draws a circle on the board, it does not record that that coordinate has been shot at.  So, players are allowed to shoot the same coordinate multiple times.  That doesn’t matter so much for misses, but I realized during testing that, as it stands now, you can repeatedly enter the same hit coordinate over and over, and win the game without finding all of the other targets.  To fix this, I’d need to find a way to record whenever a coordinate was entered, and stop people from entering that coordinate again.

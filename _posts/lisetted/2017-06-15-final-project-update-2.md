---
layout: post
author: lisetted
title: "Lisette's Final Project updat 2"
---



<iframe src="https://trinket.io/embed/python/9e6bc6b9bf" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

Previous milestones

-[x]mario turtle moves right and left and jumps 
-[x]other turtle exist that mario will hit 
-[x]gameboard 
-[x]randomly generate numbers to assign to the turtle boxes 
-[x]turtle boxes can change colors
-[x]Mario stays within boundaries
-[x]change the color of the turtles appropriatly, red if guessed wrong, green if guessed right 
    -[x]update--use a function or dictionary to make fix the current lag
-[]user can see a counter that goes up when the user guesses correctly 
-[]maybe create some animation when you win the guessing game 
-[x]fix the gameboard to make it look nicer 
-[x]fix the instructions to only flash when the user needs them
-[]user can select multiple levels
-[x]user can click to show instructions and remove instructions
-[x]use of image to show instructions

New milestones
-[]nice code that is iterated for the 3 rows of turtles
-[]nice code that is iterated for both levels of the game

Reflection:

I made a lot of progress last night! The game functions the way I want it to and the turtle boxes change the correct colors when they get hit by the mario turtle. One thing that is nagging me about my code is that I coded it brute force style. Since I know that I am going to implement an additional level where the user has to correctly guess 5 boxes rather than 3 I have been coding for 5 instances. This means every action has to be written in the code 15 times! I know that it would be elegant to create a loop to iterate this code, but I think that might something I'll figure out after everything works.

I am really happy that I was able to understand why the turtle boxes were changing colors at the wrong time. The steps were 1) determine the turtle box was hit 2) count the jump number 3) compare jump number to random number 4) change color of box if box was hit and jump number equal to random number. However, because this iterated at every jump, there are situations that turtle box color would change on  marios next jump. I fixed this by setting the intitial jump number to -1, and putting the jump number in the jump dictionary.

I think my milestones are reasonable, though making my code nicer by iterating it for the three rows and two levels is a bit of a stretch for me. In my head, I know exactly how I would do that in SAS, but I'm not sure how I could do it in python. I'm going to continue to think on it since it would make my code easier to understand, but since it won't impact the functionality of the game it wil be a finishing touch.

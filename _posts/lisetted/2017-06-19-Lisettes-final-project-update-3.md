---
layout: post
author: lisetted
title: "Lisette's Final Project Final Update"
---


<iframe src="https://trinket.io/embed/python/49b949df54" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

Milestones

-[x]mario turtle moves right and left and jumps 
-[x]turtle boxes show up
-[x]mario can jump to hit the turtle boxes and change their color
-[x]gameboard can be read by user
-[x]randomly generate numbers to assign to the turtle boxes 
-[x]turtle boxes can change colors
-[x]Mario stays within boundaries
-[x]change the color of the turtles appropriatly, red if guessed wrong, green if guessed right 
    -[x]update--use a function or dictionary to make fix the current lag
-[x]user can see a counter that goes up when the user guesses correctly 
-[x]after user guesses 3 correctly in one row have some animation 
-[x]fix the gameboard to make it look nicer 
-[x]fix the instructions to only flash when the user needs them
-[]user can select multiple levels
  -[x] allow user to click a hint button to make the game easier (easier level)
-[x]user can click to show instructions and remove instructions
-[x]use of image to show instructions
-[x]allow user to click done
-[x]prompt user to enter intials when done with playing
-[x]game board displays top scores

Over the weekend, I changed some of my plans for my game. Last week, my idea for 2 levels was to have one with 3 squares to guess and one with 5 squares to guess. I decided 5 squares is really too many to guess and the user won't easily be able to win. There are also many pieces of code that would have to be adjusted to allow the user to change from 3 to 5 squares on a click, and it didn't see worth it to spend so much time on integrating a click-level-change when I really didn't think the higher level would be fun and would just frustrate the user. Instead, I implemented a hint button that will change the color of one turtle box per row that is not the first box (could be either the 2nd or 3rd box) to be selected. This will make it a little easier for the user to guess corretly.

This weekend, I also implemented a high score board, which was a stretch milestone for me. It takes the previous scores, puts them in dictionary, writes the dictionary to a text file, sorts the dictionary and displays the 3 highest scores on the screen. When the user is finished playing, the user can click "done" and enter their initials to the score file. How to implement this took me a quite a bit of thinking about it and I had to reference many of the exercises and examples we had. I also had to find some additional information about the sorted() function so that I could sort the dictionary by the value rather than the key. I'm glad I took the time to implement it! My game is rather simple, so I think having a high score display may make it more interesting for the user to play.

I still have some things to polish before I am done. I want to make sure the user can put in 3 letters in their initials. I am also having a hard time turning off the animations that happen when the user correctly guesses all 3 turtle boxes on that row. I want to get some feedback from my group related to the hint button. I'm not sure it really constitutes another level, and I think the instructions and functioning of it may not be clear to the user. I think the hint button will overwrite the turtle box color if the user clicks it after they guess a row. I also need to play the game a bunch and search for other bugs that exist.

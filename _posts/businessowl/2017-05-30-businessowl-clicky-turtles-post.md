---
layout: post
author: businessowl
title: "Aaron Plocharczyk's clicky turtles post"
---
<strong>Here's the game:</strong>
  <iframe src="https://trinket.io/embed/python/3467660586" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>
<br/>
<br/>
<strong>Reflection:</strong>
<br/>
I got really far into another, more complicated game, and I ran into a lot of problems. I got very frustrated with it and quit, because it wasn't turning out to be a very entertaining program anyway. I changed my direction completely when I decided to make a "Simon" game. The rules of the game are pretty simple. You just click to repeat the sequence that flashes on the screen. There are four, differently colored quadrants that flash. The first thing I do in the game is display instructions. You are disabled from playing while the instructions are showing.
<br/>
In my setup() function, I just call a helper function named "drawSquare" four times to display the four quadrants. After the setup function runs, I decided to take in the user's full name as a global variable and then make the game start automatically by waiting a moment, starting the game with startGame(), adding the first number to the game's sequence of flashes by calling the helper function addToSequence(), and flashing that sequence by calling the helper function flash(). flash() momentarily draws a brighter colored square over one of the quadrants and then quickly overlays it again with the more subtle version of the color.
<br/>
The user then clicks a quadrant that they believe flashed, the turtle momentarily becomes a color corresponding to the quadrant, and clicky() calls addGuess(), which then adds your guess to the list of guesses and compares your list of guesses to the list of correct flashes. If at any point you pick a wrong quadrant, the lose() function executes. But if you guess seven flash sequences in a row correctly, the win() function executes. lose() and win() both call startGame() at the end, so the game restarts automatically. lose() and win() both use for loops to flash each quadrant as an end-of-game signifier. win() flashes the quadrants in order, while lose() flashes them in backwards order. lose() and win() both parse out the name you entered, determine if you entered a first name, a full name, or no name. If you entered no name, it just says "YOU WIN" or "YOU LOSE". If you gave a full name, the program inserts the middle name "problem-solver" or "bad-problem-solver" into your full name depending on whether you won or lost. If you only entered a first name, the program will do the same thing, but it will use "McGee" for your last name.

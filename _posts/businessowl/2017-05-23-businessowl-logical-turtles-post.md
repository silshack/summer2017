---
layout: post
author: businessowl
title: "Aaron Plocharczyk's logical turtles post"
---
<strong>Here's the game:</strong>
  <iframe src="https://trinket.io/embed/python/686d92a70f" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>
<br/>
<br/>
<strong>Reflection:</strong>
<br/>
It seemed like this program was supposed to be a game, and when I think of games that have something to do with drawing, I think of hangman and tic tac toe. I decided to go with tic tac toe because it interested me the most. I started out just drawing the "#" board, and from there I needed to have a way for the user to tell the turtle where to draw for their turn. I decided labeling each option with a color and telling the player to pick a color would be easiest for the player. From there, I made the turtle draw the player's symbol in the place they chose.<br/><br/>
  Instead of just leaving it at that, I also decided to have the game detect when somebody has won, so the players didn't overlook anything. For this, I had to keep track of the symbols at all 9 places on the board and check for all possible winning lines across the board. Once I did that, I took it another step forward by addressing the issue of what to do if a user types invalid input. I decided that if the player mistyped the color they chose, or if that color was already taken, they would forfeit their turn. I just thought that added a fun little layer to the game when two people are playing against each other. Of course, that brought up another issue. If a player can forfeit their turn an infinite number of times, they have to be able to give an infinite number of inputs. So I put that part of the code in an infite loop that could only be broken by raising an error caused by the end of the game.<br/><br/>
  The except clause that catches this error checks if it was a tie game or if somebody actually won. If someone won, I made the turtle do a little colorful celebratory spin. If it was a tie, the turtle still spins, but it's a dull spin. Once everyhting was put together, I played with the colors on the screen and messed with the sizes of the X's and O's to make everything look nice and polished.

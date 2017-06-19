---
layout: post
author: kmorbitzer
title: "Kathryn's final project update"
---

For my final project, I’m going to be using the tic-tac-toe game already started.  The milestones are below:
•	Incorporate a draw game into the code 
•	Implement levels of difficulty
o	First level will be normal play
o	Second level will have a piece erased using the random number generator so that on ¼ turns, a piece will be erased
o	Third level will have a piece erased using the random number generator so that 1/3 turns, a piece will be erased
o	I will also incorporate the key events into the levels of difficulty by having the user key which level they want to play
•	A score tracker that is updated every time a game is played will need to be incorporated
•	A custom image will need to be incorporated
•	A custom turtle class will need to be incorporated
•	A win screen and an end screen will need to be incorporated
•	A help dialog needs to be incorporated
Project update: I was having a lot of difficulty getting the board to clear and re-draw correctly to start a new game.  The issue ended up being how the turtle was facing when the previous game ended.  I was finally able to change up the code to get the new board to draw correctly.  Additionally, I added in code to keep a running score of Player 1 total wins, Player 2 total wins, and draw games.

<iframe src="https://trinket.io/embed/python/cd3525a356" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

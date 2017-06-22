---
layout: post
author: kmorbitzer
title: "Kathryn's final project"
---

Below is my code:
<iframe src="https://trinket.io/embed/python/cd3525a356" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

Below is my reflection:
For my final project, I expanded on the tic-tac-toe game that I had created for the clicky turtles exercise.  I found the project challenging, but was glad that I was able to use my skills to expand upon a previous program and make it better.  

With this tic-tac-toe game, it starts out by asking the user for the level of difficulty.  Difficulty level 1 is a normal tic-tac-toe game that alternates between player 1 and player 2. A player will win by getting either 3 X’s in a row or 3 O’s in a row.  Additionally, the program is also set up to recognize a draw game.  Difficulty level 2 is an increase in difficulty from level 1 as there is a 1 out of 4 chance that a piece on the board may be removed.  Difficulty level 3 is the most difficult level as there is a 1 out of 3 chance that a piece on the board may be removed.  

The tic-tac-toe game was enhanced from my original exercise by doing the following:
•	Have a graphical user interface – responding to key and click events:
o	The tic-tac-toe board is set up by having nine spaces.  The spaces are numbered 0 to 8 in a list that has a length of 10 and the last spot in the list stores which player’s turn it is.  Multiple functions were created to check to see if the player clicks in bounds and mark the board with an X or O depending on the player’s turn.  If the user clicks outside of the defined space or on a line within the board, then an X or O will not appear.  

```python
def in_bounds(x,y,board_s, settings):
  if x < 150 and x > 50:
    if y < 150 and y > 50:
      if board_s[2] == 0:
        if board_s[9] == 1:
          board_s[2] = 1
          mark_board_x(2, tina, settings[1][1])
          return True 
        else:
          board_s[2] = 2
          mark_board_oh(2, tina, settings[2][1])
          return True
```

o	The program uses key events in multiple places.  Key events are used initially to delineate whether the user wants to play difficulty level 1, 2, or 3.  Key events are also used at the end of the game when the program asks whether the user wants to play again.  With the difficulty level, the user can specify the difficulty level by entering 1, 2, or 3.  If anything other than 1, 2, or 3 is entered, then the game will default to difficulty level 1.  Similarly when the game asks whether the user wants to play again, the user can enter y or Y and anything entered outside of that will automatically default to the user not wanting to play again. I originally did not have my key events set up this way and the only options to select for both questions was 1, 2, 3, y, Y, n, N, but during class when others were trying my program, they entered options outside of that and suggested that I should include those scenarios.  There is also a key event for the help screen that is described further below. 
•	Have a constantly available help dialog:
o	I struggled with how to create the help dialog and what to put in it.  I finally decided to create a function that would call the help screen if the letter h is selected during game play.  The way that I developed the help screen was by using tina.write commands and I positioned the lettering to appear at the bottom of the screen.  The lettering will stay present until the user selects the letter h again.  The way that I was able to get the help screen to disappear was to have a rectangle draw over the lettering that is the same color as the background color.  I had a hard time determining what actually needed to go in the help screen, so finally I just put how the user can win tic-tac-toe: “This is tic-tac-toe.  You win by getting 3 of your places in a row either horizontal, vertical, or diagonal.”  I also didn’t originally state in the program how to toggle the help screen until the classmates in my group told me to put that in somewhere, so I put it on the same screen where you pick the difficulty level.
•	Display information about a program’s state such as score or level
o	The tic-tac-toe game is now iterative (described more below) so users can play multiple games without stopping the program.  With the iterative interface, I incorporated a score screen at the end of the game.  Once a game is over, the screen will state how many games player 1 has won, how many games player 2 has won, and how many games were a draw.  The function to determine who won was the same function as in the first exercise in that I had to create all the different scenarios for each player to win.  However, I originally did not have the function incorporate a draw game, so this was something new added in using the !=.  
•	Have at least 3 levels, increasing in difficulty
o	As described above, there are 3 levels of difficulty for the program.  Difficulty level 1 is a normal tic-tac-toe game that alternates between player 1 and player 2. A player will win by getting either 3 X’s in a row or 3 O’s in a row.  Additionally, the program is also set up to recognize a draw game.  Difficulty level 2 is an increase in difficulty from level 1 as there is a 1 out of 4 chance that a piece on the board may be removed.  Difficulty level 3 is the most difficult level as there is a 1 out of 3 chance that a piece on the board may be removed.  This was done by creating a function that is only called if the difficulty level is 2 or 3.  A random number is generated in that function to first see if a piece should be removed and then a second random number is generated to see which spot on the board is to be removed.  If it selects a spot that does not already have a piece, then no piece is removed.  If a piece is to be removed, then the program will draw over it.  

```python
  #if the user picked difficulty level of 2 or 3 this calls the functions to remove pieces
  if tina.difficulty_level == 2 and valid_click == True:
    spot_to_remove=remove_p(tina,4, board_spaces, settings[0][1])
  elif tina.difficulty_level == 3 and valid_click == True:
    spot_to_remove=remove_p(tina,3, board_spaces, settings[0][1])
    
  if spot_to_remove != -1:
    board_spaces[spot_to_remove]=0

def remove_p(tina, remove_odds, board_s, background_color):
  #This gets a random number to see if a piece should be removed, currently 1 out 4 chance of 'harder' and 1 out of 3 for 'hardest'
  if random.randint(0,remove_odds-1) == 0:
    #A random number from 0 to 8 decides which piece should be removed
    remove_spot=random.randint(0,8)
    
    if board_s[remove_spot] !=0:
      draw_over(tina, remove_spot, background_color)
      print("A piece was just removed!")
    return remove_spot
    
  #If a piece is not to be removed it returns -1  
  return -1
```

•	Extend a custom Turtle class
o	The Turtle class was extended to make a custom Turtle class for the program that has a dictionary to keep the score tally and it also keeps track of whether the help screen is toggled and the difficulty level that was selected.

```python
class CustomTurtle(turtle.Turtle):
  def set_init_scores(self):
    self.scores = {'Player_1':0, 'Player_2': 0, 'Draw': 0}
    self.help_is_currently_toggled = False
    self.difficulty_level = 1
```

•	Have a ‘win’ screen
o	Along with adding in the score tally, I also added in a ‘win’ screen.  After one of the players gives the correct combination to win a game, a screen will appear that states which player won the game and what the current score tally is of each player.  As stated above, I also incorporated draw games if neither player is able to give the correct combination to win the game.  If this occurs, the screen will appear stating that it is a draw game and the score tally also keeps track of the number of draw games.  

•	Have an iterative interface.  That is, the user should be able to perform any number of supported actions (such as playing the game over and over)
o	After a player has won the game, or if the game is a draw game, the program asks if the user would like to play again.  As stated above, the user can enter y or Y for yes, and anything else entered will mean no.  If the user does want to play again, then the board will clear and be re-drawn.  Re-drawing the board was difficult for me.  The board kept being re-drawn in a different spot and wouldn’t line up with the game spots.  It ended up being an issue with how the Turtle was oriented at the end of the game, so I had to work on getting his orientation correct to correctly re-draw the board. Even though I didn’t end up using it, my group gave the suggestion of using the command setheader.  If the user does not want to play again, then a screen will appear stating “Thank you for playing!” and the image of a rocket flies across the screen.

•	Use one or more custom images
o	For my image, I originally wanted to use a stick figure that had a thumbs up after one of the players won the game.  However, the image that I wanted to use took up the entire screen when I imported it and I couldn’t figure out a way to decrease the size of the image.  Therefore, I ended up using the image of the rocket that moves across the screen once the user stated that they no longer want to play.  

Overall, I’m happy with how my final program turned out.  It’s a simple program in that it is a tic-tac-toe game, but I feel like I was able to incorporate all of the skills that I learned throughout the class.  

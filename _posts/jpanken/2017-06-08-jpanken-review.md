---
layout: post
author: jpanken
title: "Jaffa's Peer Review of Erin's Blackjack"
---


<a href= "https://silshack.github.io/summer2017/erin-blackjack-game.html"> Erin's blackjack and reflection</a>

Erin’s blackjack game works perfectly.  It has a clean and simple user interface.  There are custom functions and custom modules that leave main.py a mere 14 lines long.  She calls the game with a function called “play_the_game”, which lives in card_functions.py, which houses most of the code.  All of her variables live in a module called, conveniently enough, all_variables.py.  The variables are imported into card_functions.py and the card functions are then imported into main.py.  


I think that it was interesting choice to keep main.py mostly clear and do the heavy lifting in card_functions.py.  That modules has both functions and while loops.  As I was reading through the code, defining functions and using them in the same module was a little confusing.  If I wanted to remember how each those functions worked, I had to scroll up the page to find the mentioned function.  Then I had to return to my original place in the code, which was difficult to find again.  I also had difficulty keeping track of how certain functions and variables were different from each other.  For example, she has a variable/loop called "game_over" and a function called "finish_game()":
```python
if play_it_again == "y":
            del player_card_list[:]
            del dealer_card_list[:]
            deck_card_list = [1, 1, 1, 1, 2, 2, 2, 2, 3, 3, 3, 3, 4, 4, 4, 4, 5, 5, 5, 5, 6, 6, 6, 6, 7, 7, 7, 7, 8, 8, 8, 8, 9, 9, 9, 9, 10, 10, 10, 10, 10, 10, 10, 10, 10, 10, 10, 10, 10, 10, 10, 10]
            setup()
            game_over = False
          else:
            finish_game()
```  
To understand the difference between these two statements, I would have to go to two separate modules and look up their definitions.  Perhaps a clearer distinction between naming practices of variables and functions would help me out.


Erin’s code structure was complex and intricate.  I admired her logic and the intense effort that it must have taken to work piece by piece and put together something that actually works.  At the same time, I could not explain to you exactly how it works.  There are so many functions nested inside of other functions that I would need to study her work more thoroughly.  I clearly have a lot to learn from Erin’s work.


For one, defining and using functions is not my strong suit.  I did most of my coding in the main.py window and struggled when I had to implement functions from my helper code.  Judging by her extensive use of functions, Erin seems to be quite comfortable with them.  By defining the variables in a separate module and importing them directly into card_functions.py, perhaps she was able to bypass some of the issues that I have had with passing variables between modules.  


Like myself, Erin used a simple and intuitive user interface.  Perhaps we both could have rolled out the red carpet for our users a bit more, but sometimes all the flourishes get distracting.  I think that we were both focused mostly on utility rather than flair.  Making the game easy to play should be the highest priority and I think that we both succeeded in this aspect.


In the future, Erin plans to integrate visuals into her program.  Given the artistic talent that she has shown in her other programs, her integration of text and visuals should be entertaining.  Perhaps she will also consider using for loops to create her deck of cards rather than typing out a whole list.  The deck was the first part of the program that I elaborated on and I think that it would be a neat, if understated, addition to an already impressive project. 

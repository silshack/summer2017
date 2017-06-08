---
layout: post
author: businessowl
title: "Aaron Plocharczyk's Blackjack Peer Review & Self-reflection post"
---
<strong>Here's my game:</strong>
  <iframe src="https://trinket.io/embed/python/3211a2fc5c" width="100%" height="356px" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>
<br/>
<br/>
<strong>Here's Sam's game:</strong>
  <iframe src="https://trinket.io/embed/python/04f9f1eae5" width="100%" height="356" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>
<br/>
<br/>
<strong>Reflection:</strong>
<br/>
Sam satisfied and exceeded all requirements for this assignment. The most strikingly unique part of the app is its graphical user interface. He drew that table with a turtle, made 52 images representing the front of each card, and made an additional image representing a face down deck. I'm sure this took a lot of effort. Functionally, this deck works just like a real deck. If a card is already currently showing on the table, it cannot be drawn again until the deck is restored in the next round. Another striking addition that Sam made is having the option of betting on each hand. He made sure you could not bet more than you currently have, must bet more than 0, and if you reach 0 remaining credits, you lose and the game ends. It is a very creative app the goes well beyond even the advanced requirements. Here's a full list of all the unique features that make Sam's app so creative:
<br/>
- created a deck instead of generating a random number
- keeps track of dynamic values of aces
- cards cannot be dealt more than once per round
- allows for five card charlie
- allow for option of betting or no betting
- cleanly formatted text interface
- cleanly formatted graphical user interface
<br/>
Sam's app is very easy to use. Without even considering the graphical user interface, the text prompts and outputs are well organized and spaced, and the instructions are clear. Even if you type incorrectly, you get another chance to type valid input. The flow of the game makes sense, and the graphics just make everything that much better.
<br/>
Sam's code is clean and well organized into separate modules (main, dealer, and graphics). His graphics implementation was added at the last minute, so there are understandable no comments in the graphics module. The dealer module has a good amount of commenting. The main module does have commenting, but it would have been easier for me to read if more of the process in the main module was denoted with comments. Sam's code is clean and runs without errors. I'm not sure if Sam knows this but blocks of code like this:
```
  if betting == True:
    if player_wins == True:
      player_wallet = player_wallet + player_bet
    elif player_wins == False:
      player_wallet = player_wallet - player_bet
```
can be written like this instead:
```
  if betting:
    if player_wins:
      player_wallet = player_wallet + player_bet
    elif not player_wins:
      player_wallet = player_wallet - player_bet
```
as long as player_wins will either be True or False. That's just a stylistic thing though.
<br/>
I can tell from Sam's milestones that his process was well thought out. His starting point was well chosen, and he progressed logically from there.
<br/>
As far as improvements go, it seems unfair that I get to see my first two cards before I make a bet on the hand. It might be better if one of the cards is dealt face down and then flipped once I bet. Or, you could just deal one card and only deal the next card once I've chosen my bet. Also, Sam could have one of the dealer's cards showing while the player is hitting, to mirror reality. Sam could also look into "doubling" and "splitting your cards." Sam's app is so well developed already that I do not expect these improvements to take place.
<br/>
Sam's code did include modules, functions within the modules, and for loops as required. His coding and logic made for an easy flow of gameplay that caused no errors and ran continuously and appropriately even if the user gives invalid input. His code allowed for many things that my code did not, including using a deck instead of a random number, allowing betting, and having a graphical user interface. These are all great features that show excellence and dedication in this assignment. I considered making a graphical user interface myself but did not end up doing so. My initial though when I saw the cards was that Sam drew them with turtles, but I later realized that they were images that same had created and imported. If I were to come back and add graphics to this assignment, I would do it that way as well. Sam set up betting in his assignment just as I would have if I had implemented betting, so I'm sure referring to his code would give me general guidence on how to do that in my own code. I was satisfied with my own code, but I believe Sam took his work even further than I did. Overall, I would say that we both met the advanced requirements and exceeded them, so we both ended up doing very well with this assignment.

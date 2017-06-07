---
layout: post
author: businessowl
title: "Aaron Plocharczyk's blackjack post"
---
<strong>Here's the game:</strong>
  <iframe src="https://trinket.io/embed/python/3211a2fc5c" width="100%" height="356px" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>
<br/>
<br/>
<strong>Reflection:</strong>
<br/>
Creativity for me was going beyond the requirements and implementing features that I thought would make the game more interesting than it already was. To do this, I implemented five card charlie, made the game automatically count your aces as either 1 or 11 (whichever worked out best for your hand), and keep track of your win percentage. The inputs are always either "y" or "n", so the game is very easy to use. While the game shows you what your hand is, it does not require you to count your hand yourself. That could be tricky because aces could be either 1 or 11. Instead, the game calculates your best possible current score for you automatically. Zooming through a round of blackjack is easy. <br/>
My code is organized into five modules: main, runthrough, deck, scoreboard, and styledPrint. Main just has a loop that says the program will run through a round as long as the user wants to keep playing. Runthrough calls all the functions in deck, scoreboard, and styledPrint to run through a round of blackjack. Deck deals with everything having to do with cards, like dealing a a new card, getting the player's hand, and scoring a player's hand. Scoreboard deals with getting a player's score after the player hits and getting the dealer's final score. StyledPrint simply has a function to print mirrored strings with another string in the middle. This separation of code makes the program much more intuitive to read and navigate. Additionally, nearly every line is commented out in plain english so it is easy to understand what is going on in the code.
My milestones include what was required in the basic and advanced version of the assignment, as well as what I chose to add to the assignment. They are as follows:<br/>

### Milestones:
- [x] make function to deal a card
- [x] make function to deal dealer random hand between 16-21
- [x] make function to deal player appropriate amount of cards and return their current score
- [x] make basic "runthrough" function to deal cards to the dealer and player during a round of blackjack
- [x] in the runthrough function, keep asking the user if they want another card until they say no
- [x] if the user busts, they lose
- [x] compare dealer's hand with player's hand and write verdict
- [x] ask if the player wants to restart the round
- [x] implement jacks, queens, and kings
- [x] change dealer's deal function to actually deal cards until the dealer has reached at least 16
- [x] write if dealer busts
- [x] change function that scores a hand to count aces as either 1 OR 11.
- [x] print out the player's hand every time it changes so they can keep track of their aces and the complexity of their hand
- [x] allow player to reach a five card Carlie and automatically win
- [x] allow dealer to reach a five cards Charlie and automatically win
- [x] keep track of win percentage
- [x] print win percentage after every round
- [ ] show dealer's top card during each round
- [ ] implement betting
- [ ] implement minimum buy in for each round

<br/>The design of my user interface followed closely to the sample output I was given in the assignment. I did make some changes though. Because I decided to allow my program to display the player's maximum score (because aces should be counted as 11 instead of 1 until that would cause the user to bust), the user must know if he has any aces in his hand so he knows if it is safe to hit or not. Because of this, I chose to display the player's hand upon the initial deal as well as every time the player hits. Further, the game seemed to have little purpose until I implemented a win percentage, so I decided to emphasize the win percentage by writing a bunch of dashes before and after it once each round finishes. That seemed to give the game a point. I would love to improve on this game in a couple ways if I had the time to do so. First, I'd like to show the dealer's top card while the player is hitting. That would mirror reality more closely. Secondly, is like to implement a betting system wherein the user can bet on each hand. Third, I'd like to implement a minimum "buy in" that the player must pay just to play a round, like they do in real blackjack.

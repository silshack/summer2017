---
layout: post
author: samsr31
title: "Sam's Blackjack Game"
---

Here is my finished blackjack game project:


<iframe src="https://trinket.io/embed/python3/9c2e46209e" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

EDIT: I got the graphical version to work!  Here is that version:


<iframe src="https://trinket.io/embed/python/04f9f1eae5" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>



Reflection:

    My first thought when reading through this assignment was that I wanted to try to use lists and tuples to model a full deck of 52 cards, rather than use random number generators creating values from 1-10.  I decided to make a list of tuples, because then I could store different types of data in fixed positions in each tuple, and use index slicing later to collect just what I needed at the time.  As is, each tuple has a string representing a card’s name, used to display what a player has in their hands, and an integer value, representing the card’s value in the game.
    Once I got the basic deck of cards done, and the basics of the game built, the next challenge was to handle ace values.  Since aces can be either 1 or 11, their value doesn’t fit nicely into a single position in a tuple.  This took some time to think through, but I ended up with a pretty neat solution.  Aces are assumed to be 11s, and are valued as such in their tuple.  However, when the scoring function is checking the value of a hand of cards, instead of just summing all of the values, it instead makes an intermediate list of card values.  If the sum of that list is greater than 21, it checks to see if there are any 11s in the list, and if so, it turns one of them into a 1.  It repeats this check until there aren’t any 11s left to change, or the score goes under 21.  This way, aces can have one set value in their card tuple, but for the purposes of scoring they can be changed from 11 to 1 if it is in the player’s best interests.
    After figuring that out, I spent some time cleaning up the overall flow and presentation of the program, I added a replay system so that it would keep looping until the player wanted to stop, and I added a five card charlie win condition after Aaron mentioned it in his program on Monday.  The last big improvement I added to the game was a betting system.  To do this, I added a question at the start of the game asking if the player wanted to use betting.  If they did, it set a “betting” variable to True, which caused various things to happen throughout the program.  I seeded little if statements wherever something involving betting needed to take place, whether it was displaying the player’s current credit total, or asking how much they wanted to bet.  If “betting” was true, this extra thing would happen, otherwise the program would move on as if nothing was there.
    As can be seen in my milestone list, there were a few ideas I had at the start which I either didn’t get to or decided not to do.  These were mostly features which at first I thought were part of normal blackjack, but as I did some research discovered didn’t work quite the way I had remembered, such as how the deck is shuffled, and how multiplayer works.  I also wanted to try to make a graphical interface to go along with the text, but ran out of time to implement this.  If I were to keep working on this program, implementing the graphics I made would be my main priority.

Milestones:

Milestone Plan
I definitely want to do more than just generate a random number from 1-10.
I would rather generate a whole deck of cards, which I think can be done with lists.  So...
Step 1: create a deck of cards, which can be randomly drawn from --- DONE
Step 2: assign values to cards (use tuples?)  Aces will be harder to handle --- DONE
Step 3: set up a basic game loop where the player can hit to get cards,
  cards are drawn from the deck into their hand, and they get feedback --- DONE
Long term goals:
 create a persistent deck, meaning that multiple hands of the game happen
   until the deck is empty, at which point it is refilled. --- I've decided against doing this
 allow players to "shoot the moon" --- After a bit of research, I think this is Not A Thing
     5 card charlie - That's what it's called! --- DONE
 general cleanup of text interface and layout --- DONE
 graphical user interface?
 multiplayer?
 betting? --- DONE

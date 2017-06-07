---
layout: post
author: neatoskeeto
title: "Matt Zimo's Blackjack game extravaganza"
---

<iframe src="https://trinket.io/embed/python3/e0de2dbc87" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

In my head, this was a lot easier when I first thought about the program. I was pretty confident I knew how it needed to be done, so I started out defining functions in helper modules right away. This proved to be a mistake, because I kept getting weird errors with unhelpful descriptions. 
Then I decided to start from scratch and put it all on one module with no separated functions. After a little bit of trial and error, I got the game to work. My next goal was to separate out the get_dealer_score function, because that seemed like the easiest to do. I then separated the get_card function, because it was used in the get_player_score function, which was the bulk of the code.
I added an overarching while loop to prompt the player if she wants to play again. In fact, I only used while loops in the first iteration of the game. That was one of the problems I had to address because the assignment required a for loop.
I was pretty satisfied with my code as it was and left it for a day, so I could work on other assignments. When I came back, I wanted to see if I could make the game more realistic by creating a deck of 52 cards and having the player and dealer draw cards from the same deck. That proved to be a more difficult task than I anticipated. I knew I needed to make the deck a global variable, but I kept doing it the wrong way, or using incorrect syntax when trying to use it. I think I deleted all the commented out global decks I had scattered around my code, but believe me, they were everywhere.
I also had some trouble with formatting the strings. I wanted to use a join statement to print all the cards in the player's hand separated by a comma and a space, but I couldn't get it to work. You can still see the corpse of that effort in lines 53-55 of my deck.py module:
```
        currenthand.append(currentcard)
        i = (i + 1) #increments the counter up by one
        x = getscore(currenthand)
        #aaa = ', ' #trying fancy formatting technique. I didn't get it to work
        print ("You have %d cards worth %d points: %s" %(i,x, currenthand))
        #print(aaa.join(currenthand)) test of failed fancy formatting technique
```
I don't know why it didn't work, but I assume it has an easy fix.
One of the last things I did was to make it so that the player sees what card the dealer is showing. I had to change the order of the get_dealer_score and get_player_score functions, so actually, the dealer plays first (and can potentially bust before the player plays). 
Further milestones I would like to take the program: make it automatically detect a five card charlie win (currently, it only detects it when the player declines to draw another card), ability to automatically switch the values of aces from 1 to 11 based on math, and make it possible to split the cards if the player is dealt two cards valued at 10 in the beginning.

Milestone list:
<ul>
<li>make the game randomly generate values for player and dealer</li>
<li>create logical statements to determine who wins</li>
<li>separate out the functions to make the code cleaner</li>
<li>switch from random integer generation to random selection from a deck of 52</li>
<li>make the program show what cards the player and the dealer have (still not completed to my satisfaction)</li>
<li>Upload the program to python 3</li>
<li>Update the program to work on python 3</li>
</ul>

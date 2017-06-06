---
layout: post
author: nvola
title: "Natasha's Blackjack Project"
---
I started this assignment knowing that I wanted to meet the advanced requirements so I created a milestone list based around those. Here are my original milestones:

	- [x]Create all 52 cards in deck in a list. This includes adding coding to deal with face cards, which all have the value of ten
	- [x] Define function to deal two cards to the user (deal_card)
	- [x] Card deal should be random sampling without replacement (i.e., need to use pop or delete methods to delete the randomly chosen cards from the list after they've been "dealt")
	- [x] Define function to compute the player's score and display it (get_player_score)
	- [x] The get player score function should handle the initial deal and the hit/stay loop
	- [x] Define loop to continue asking user if they wish to HIT or STAY
	- [x] If/else loop computer the user's score and comparing it against the dealer's score
	- [x] Generate the dealer's score (get_dealer_score)

Along the way  I realized I had forgotten some so I added:
	- [x] Store the cards that have been dealt in their own list to enable the get_score functions
	- [x] Ask user if they want to play again
	- [x] Compare player score against dealer score
	- [x] Get as close to the real rules of blackjack as possible, in terms of scoring
	- [x] Add time.sleep() so that all the dealer's moves don't just appear all at once
	- [x] Have user-driven start point so they don't just open the game and are given a card

After viewing others' work in class I decided to add these milestones.
	- [x] Break up the program into smaller modules
	- [] Show the user their hand
	- [] Incorporate the five card charlie rule

I started the assignment by creating a list that would serve as a deck of cards (just one deck, because that was easier than including 6). I thought about including the face cards as actual faces (e.g., A, K, Q, J), that would permit some additional nuance to the program and game play, but I didn't get around to thinking in depth about how (and where) I would convert these to numbers (probably in the get_player_score function).  This also means that I haven't integrated the ability for Ace to be 1 or 11, it's always 1. Also, I decided to code this as random sampling without replacement, this is one of  the reasons as to why I decided to store the cards for the dealer and the user in lists. 

I hit a snag when defining the function to compute the users' score.  For one,  I originally was forgetting that that (of course) I have to deal some cards first to get a score. I ended up handling this function a bit differently than the requirements outlined it ; the requirements had that the card deal should be part of the getting the player's score, however  I decided against this because in doing so (at least in the way I was attempting to do it) there was not a way to have 2 card deals for the initial card deal compared to one card deal when the player chose to hit.  Also, in doing so, it was essentially doubling  the core (dealing twice) each time I ran the "get score" function. I was also having some difficulty incorporating this into the if else statement that would continue game play. To get the dealer's score, I ran into some similar issues; it was a lot easier for me to control the flow of the program if I defined a SEPARATE function to deal the cards and add them to a list, and then to have a function that calculates the score creating a sum of the list. 

I also had a bit of trouble when I first tried to make the game play into a loop to keep asking the player whether they wanted to play again. I had an issue where the score just kept increasing. I realized with testing that I needed to put literally everything into the main function.

Another thing that I found to be more consuming was that I was trying to get the scoring as realistic as possible, and this required a lot of testing with comparing the scores with the user and the computer. Relatedly, another reason I did decided to store the player's and the dealer's hands in lists was because when I tried to compare the scores later in the code (to determine winners), it was much easier to refer to. Further, if I hadn't kept the deal_card function separate from the get_score function, I wouldn't be able to simply retrieve the scores.  

The only milestones I wasn't able to check off my list was showing the user their hand and incorporating the 5 card Charlie rule. I added these after viewing a few peoples' code in class. However, I wasn't able to incorporate those features due to time constraints, but I believe I know how I would implement these two features had I had additional time to do so.

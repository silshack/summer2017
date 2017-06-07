---
layout: post
author: kmorbitzer
title: "Kathryn's Blackjack App"
---

Below is my code:
<iframe src="https://trinket.io/embed/python3/cd7034c5da" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

Below are the milestones:
•	This is a program that allows a user to play a modified version of Blackjack with a dealer
•	First, I need to define the four functions used in the game to comply with the design requirements
    o	main: this is the main function where everything else will get called and organized
    o	get_player_score: this handles how the player gets their cards and allows them to decide if they want more cards
    o	deal_card: this function calls a random number between 1 and 10 that is dealt to the player 
    o	get_dealer_score: this is where the dealer is randomly assigned their score value between 16 and 21
•	In main, there needs to be a while loop that continued looping until the player decided to stay
•	The player plays first and get_player_score needs to be called first to get their hand
    o	In get_player_score needs to be decided if this is the first hand or not to decide how many cards the player gets
    o	If the player hits and wants another card, deal_card is called
•	Once the player is done playing, the get_dealer_score function is called to get the dealer’s score
•	Once both players have their score, the scores are compared to determine who won
•	Lastly, the program asks if the player wants to play again

Below is the reflection:
The Blackjack App was a fun program to create.  I started out by creating the variables needed for the program.  I then moved on to the player’s cards.  The player’s score is based on a random number generator between 1 and 10, and after each additional score, the program asks if the player wants a hit or stay.  The program is also set up where if the player gets a score greater than 21, they bust.  After finishing everything up with the player, I moved onto the dealer hand.  The dealer’s hand is set up where they will get a random number generated between 16 and 21.  In my program, the dealer can’t bust.  Once the dealer hand is dealt, the program will compare the dealer score to the player score, and then determine who won.  The program then also asks if the player would like to play again.  

Will this assignment, I certainly saw the benefit in staying organized and having clear comments.  Do this helped me keep better track of the code and more easily find parts to change if an error occurred.  During class when people were showing their initial programs, some cool concepts were brought up, like being able to see one of the dealer’s cards before determining whether to hit or stay.  It would be cool to incorporate additional things like that into the program.  

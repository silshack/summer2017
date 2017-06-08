--- 
layout: post
author: chausuble
title: "Erin's Review of Jaffa's Blackjack Game"
---

Jaffa’s Blackjack game accomplishes almost everything the assignment requires, and above all, is fun to play. It plays more like a traditional Blackjack game than mine, where you see the starting hand values for both the player and the dealer. The player is allowed to draw cards to their satisfaction or until the hand goes bust, then the dealer draws cards until they draw the card that makes the value of their hand exceed 15. Just browsing through the code for the first time, I already saw the first difference that I was kicking myself to implement – her program, unlike mine, leaves room for a tie where no one wins or loses. I just have the player lose!

It’s really easy to go through and see how the program works – every line is commented with an explanation, and every stage of the “while” loop is clearly demarcated. Furthermore, her module includes helper functions for making the deck, choosing cards, and replaying the game. I really liked the way she made her deck, using a “for” loop to add four sets of 1-9 and 10s into an empty list for the cards. In my case, I just physically copied 1 – 10 four times into a list and used that. Furthermore, her drawing a card function uses an alternative method to .pop(), through using .add() and .remove().

Her use of a “calling” loop, in the case where neither the player nor the dealer went bust or got a Blackjack, helps to make her program even cleaner and readable. At every win or loss possibility, she simply prints what the dealer’s hand is worth, who won, and then calls her play_again() function. In her reflection, she doesn’t seem to think that her code is well-structured and readable, but I think it’s great. Probably what led to good results in her program is her use of milestones, going through the game process step-by-step – making a list of all the cards in the game, then lists for the player and dealer’s hands, and having that display the total value, and so on. 

One thing I really like about the program is its speed. I realized while making the program is that I like to start the game right away, rather than navigating through any menus to or typing in options – I just click run, and Jaffa’s program fires right away with your hand and the dealer’s hand. Honestly, the only problem I can see is that the replay loop will restart a game, but if you type “n,” it won’t end the game. If the program were to be improved upon or with a new interface, I would like it if it kept the speed.

I relate to several of Jaffa’s ideas in the reflection – I didn’t even think about changing the value of an ace to 1 or 11, or programming in betting and all those multiples, but those are cool ideas to add into the program. Above all, however, it’s the simple, clean and intuitive interface that really won me over, and I’m glad she made it a priority in her work. This was a great program.

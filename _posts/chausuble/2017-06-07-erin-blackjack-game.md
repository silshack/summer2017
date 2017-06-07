--- 
layout: post
author: chausuble
title: "Erin's Blackjack Game"
---

<iframe src="https://trinket.io/embed/python/daf1e2ebe5" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

-[x]make random number generator
-[x]random number generator can remove and return values from deck list
-[x]random number generator and remove values and add them to player/dealer card list
-[x]player can draw cards
-[x]player can end turn
-[x]dealer can draw cards
-[x]dealer draws cards as long as their total value of list is less than 16
-[x]program win conditions: player = 21, player > dealer, dealer > 21
-[x]program lose conditions: player > 21, dealer > player, dealer = 21
-[x]game can replay or close
-[x]game presents number of wins and losses on close
-[x]all list values reset on replay
-[x]make replay function
-[ ]replay works as a function

As I mentioned in the in-class reflection, I did this project piecemeal. I figured that we would need a random number generator, a list for all the card values in the game, and the lists for the player and the dealer’s cards. I made those lists first, then worked on the random number generator, which wasn’t bad once I looked up how to import those functions, and what exactly they each did.

From there, I had to look up the rules of Blackjack and incorporate them with the assignment’s guidelines. First, I programmed the basic loop of the game, making functions to draw cards for each player, where I used the .pop() function to remove and return the card from the deck. Overall, drawing the cards wasn’t too bad – it was making it into a whole big game loop that took me a long time. This is where I learned to use global variables, so that my functions could always read them. I don’t remember the exact process, but once I figured out one block of the game, the rest was easy to fill in.

The biggest struggle, easily, was learning how to make the modules. Seeing other people in class use the “import *” really helped, rather than me having to use “import player card list, dealer card list, deck card list…” and so on. In the end, my struggle was, yet again, for a really petty reason – I accidentally added an extra “0,” to the dealer_draws_card() function, which made the whole ride break down. I think it’s fixed now.

The other big problem: I wanted to make a function called replay(), that would include the following:

```
          play_it_again = str(raw_input("Do you want to play again? y/n"))
          if play_it_again == "y":
            del player_card_list[:]
            del dealer_card_list[:]
            deck_card_list = [1, 1, 1, 1, 2, 2, 2, 2, 3, 3, 3, 3, 4, 4, 4, 4, 5, 5, 5, 5, 6, 6, 6, 6, 7, 7, 7, 7, 8, 8, 8, 8, 9, 9, 9, 9, 10, 10, 10, 10, 10, 10, 10, 10, 10, 10, 10, 10, 10, 10, 10, 10]
            setup()
            game_over = False
          else:
            finish_game()
```

Then, at the end of each game, I would just call replay() without having to copy and paste it everywhere. But when I do this, the program will print “Your total is [number].” But it doesn’t prompt the player to draw a card! Again, it works perfectly fine if I copy and paste the whole thing into the function, but not if I call it. I don’t understand why it isn’t working, or else I’d fix it.

In the future, it would be fun if I made this with visuals, or was able to at least let you see whether you drew a King or a 9 of hearts, or things like that. I couldn’t figure out the latter in time.

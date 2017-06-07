---
layout: post
author: jpanken
title: "Jaffa's Blackjack App"
---


Here's the code:
<iframe src="https://trinket.io/embed/python3/9fb6c666c6" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>



Playing Python blackjack is super fun.  It's a good thing that I don't gamble, though, because I'm not very good at it.  


I started working on this program last week by planning out how I might create a more realistic deck of cards on a piece of paper.  By working on paper, I was able to refine my ideas before I started in Trinket.  Then, I conceived of the game as a series of while loops.  It wasn't until later that I realized that I needed all those while loops to be within a main while loop to restart the game.  Even later, I figured out that only some of the while loops were necessary for tasks that needed to repeat.  I feel like that should have been obvious to me from the beginning, but live and learn.


### Milestones:
- [x] Create cardlist
- [x] Create players/dealers list to keep cards
- [x] Create players/dealers list to display sum
- [x] Hit/stay loop
- [x] Dealer's loop
- [x] Calling loop
- [x] Figure out how to start a new game
- [ ] Clean it up with helper.py


Since I got everything to work this weekend, I have tried to structure my code so that it is readable.  Mission not totally accomplished.  I have a lot of variables and I haven’t been able to import them them all from the helper code into main.py.  I got some help at the clinic after class, but that revealed that I need a stronger understanding of 'return' and how to implement functions.


In the future, I think that I will try to be more disciplined about how I construct my program.  Instead of waiting until it works to replace bits of code with functions, I will try to make them work along the way.  In addition, I would like to build on this code by introducing some sort of scoreboard.  I may not have a strong enough grasp on the concept of gambling to implement betting, but I could probably figure out how to construct logic that determine whether an Ace (just a 1 in my program) should be an 11.  I could also work on the user interface.  For this project, I went for simple, clean, and intuitive, rather than clever.   Those are achievable elaborations that I could have added with more time and patience. 

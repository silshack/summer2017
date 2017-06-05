--- 
layout: post
author: chausuble
title: "Erin's Reflection"
---

The most useful problem solving strategy, for me, is just to wait. Even though we’re on a time crunch, I finish for the night 
when I get stuck for more than one hour. I squeeze in what time I can in the morning before I go to work. So sometimes I don't 
get the program working exactly as I need it to, but at some point, when something isn't working, I just have to draw the line.  
My general process is to pick one thing I think I can do, and do that. For Blackjack, it was making a working random number 
generator, learning how to import "random" and its friends, then using it to print random numbers. Then, I made a “deck” of 
cards, and made sure the generator was picking out random cards from it (rather than just generating the same number over and
over again!). Then, it would add that card to a list for the player’s "hand." Suddenly, that’s the basic loop done. 

Basically, I accumulate my program like this until I get stuck. Generally, when something goes wrong, it’s a lot of little 
problems, so I go back and do a review of the code, printing out the results at every step. Then I fix it until it’s right. 
There’s no real problem solving process I can really think of, off the top of my head - just making sure I don’t have any 
typos, or, for some functions, such as in the case of adding objects to a list, it’s just changing the method I do that - 
whether by + [object] or something else.

Because of how I solve things, I can’t actually think of any revolutionary light bulb moments - just, “whooppee, I fixed a 
typo.” Even though I’ve accomplished a lot in this class, I’m not sure how much of it I'm actually learning and how much is just
coincidentally working out.

Resolving anything fuzzy is just by going in and beating the problem against the wall until it fixes itself. I don’t understand 
why list += [object] doesn’t work in one program, but list = list + [object] does. Reading explanations makes my head spin! 
Instead, I just figure out which method will work this time around, and then stick to that. Eventually, I guess I 
subconsciously pick up on patterns. 

But here are concrete things that I don't understand: Why sometimes, making a function doesn’t work, but copying in the function’s 
properties totally does, which is a weird problem with my Blackjack program. Another fuzzy thing is...global variables. We 
reviewed them in class but since I hadn't encountered them up that point, I didn't get what we were talking about. When I 
stumbled across their use, I still don't get what they are or why Python fanatics went rabid over people using them in their 
code. I tried reading up on them on the official Python guide, Stackexchange and Wikipedia, but the explanations just flew 
over my head. They work in my program to their intended effect, at least. For programming, I've found that confusion doesn’t 
usually help me learn about the  but to find alternative roads around whatever's confusing me, or just doing what Trinket 
pops up with and not questioning it. So far so good!

Two code excerpts: First, from my Blackjack game, the simple fact that I stumbled upon a time when 
I can actually use the del function! I'm guessing it's used for global lists? I'm not too sure about this - I didn't really 
get what "del" did in the chapter we read. I'm just glad it works for my program.

```
  if play_it_again == "y":
    #reset the lists
    del player_card_list[:]
    del dealer_card_list[:]
```

And then, the revelation of how to have one "game over" condition. If you make it possible for the player to both lose and win
the treasure hunt game, strange things can happen. So, I had to make a 2-in-1 logical statement - how close the mine is, and
affirming the fact that the user hasn't won yet. This way, if the user does win, it will bypass all of the lose conditions. 
Related to that, but not quoted here, is the idea that the order in which you nestle logical statements matters - otherwise,
you can get in a state where even when the player is supposed to win or lose, they never do.

```
elif mine_veryclose and user_has_won == False:
```

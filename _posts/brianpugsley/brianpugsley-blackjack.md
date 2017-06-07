---
layout: post
author: brianpugsley
title: "Brian's Blackjack Game"
---

This was a really interesting exercise and I had a lot of fun. I was able to zip through the basic stuff pretty quickly and forgot to duplicate it before I started on the advanced stuff. My goal was to start small and attach the functions. Those were pretty easy because I was able to, pretty much, use the same code from the player's deal and score for the dealer's deal and score. 

After I created those basic functions, I ended up nesting them in the main function. A few times, I had to take a step back and trace back through all of the loops because of a few errors that were popping up. Finally, it was just a matter of collecting the user input to begin the program and run the functions and creating an if/else to handle the yes or no.

Here is the basic program:

<iframe src="https://trinket.io/embed/python/8f6d93e78a" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

While I didn't have a whole lot of major challenges when it came to getting the basic stuff to work, I did have a few minor hiccups along the way. For example, I, accidentally put parentheses around my print statements which resulted in getting some unwanted parenthesis in my outputs. After getting those minor bumps worked out, I moved on to the advanced issues. Mainly, I tried to work to make the program continue to run as many times as the user wanted. The issue I ran into was the the scores kept adding up instead of resetting. I wasn't sure how to get around that issue. I checked my loops and they all looked good. But, sitting here, writing my reflection, I figured out the issue. I needed to clear the lists after every game. 

There are still some minor glitches in this iteration of the program but I just didn't have enough time to work them out and would like to have commented a bit more.

<iframe src="https://trinket.io/embed/python/62a50e8078" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

My milestones for this project were:

[x] make function to deal a card
[x] make function to deal dealer random hand
[x] make function that helps the dealer choose whether to hit or not
[x] make function to deal player 2 cards
[x] make main function to run through the blackjack game
[x] create loop in main function to determine whether to hit or stay
[x] if the user busts, they lose
[x] compare the dealer's hand and the player's hand to determine who wins (if neither busted)
[x] ask if the player wants to continue playing
[x] implement jacks, queens, and kings
[x] write if dealer busts
[x] created function to choose between 1 or 11 for aces.
[ ] five card charlie



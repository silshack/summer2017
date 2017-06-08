---
layout: post
author: neatoskeeto
title: "Matt Zimo's review of Justyn Felder's Blackjack game"
---

<a href= "https://silshack.github.io/summer2017/jbfelder-Blackjack-App.html"> Link to Justyn's game and reflection</a>

Justyn's blackjack game meets all of the requirements of the blackjack assignment. Furthermore, Justyn added an input function to start the game, whereas my program just started immediately. I like that, and I would do an input function like that in the future.
Another aspect of Justyn's program that I like is how he makes the program print lines of dashes between turns, which makes the experience more readable.
I also appreciate Justyn's coding organization. He separated the deck creation from the rest of the game in a separate module. I also like how he separated function definitions with long lines of "#####", which makes the code easier to read.
However, my favorite aspect of his commenting is his use of comments to check if things work. For example, line 9 in his create_deck module is:
```
#print(complete_deck) #Checks to see if deck is randomized [Works]
```
This shows where how he tested to make sure the create_deck() function works (i.e., by using a print statement that he later commented out. But he also adds the tag at the end [works]. This shows how he tracked progress in his programming and makes debugging easier. 

In his reflection, Jordyn describes the difficulties he experience while trying to program the advanced options from the assignment prompt and his own personal ideas at the same time. He stepped back, deleted all of the code, and worked to complete the advanced options alone. I can relate to that difficulty. In my program, I thought that certain aspects could be done in the same function, and tried to do them together. For instance, I wanted to find a way to score the value of aces as 1 or 11 depending on the other cards in the hand. I thought I could write that in my function that converts other face cards to 10 for scoring purposes. I tried to program the ace calculation at the same time as the face card calculation, and I got stuck. Jordyn writes that he wanted to find a way to include a multiplayer option that enables users to join or leave the table at will, but he tried to code them at the same time as the prompt's advanced options. Both of us found out that it is better to focus on a single task at a time.
I think Jordyn comments his code much better than I do, and I am going to use his technique of writing lines of dashes in print output and lines of #'s in code when separating functions and other blocks of code. He also used a for loop to populate the deck by running through a list four times:
```
for i in range(4): #Adds four 'suits' to the deck
    complete_deck = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 10, 10, 10] #A singular suit
```
That was a lot easier than my method of typing out each value four times.
P.S. I definitely learned some good techniques by taking this closer look at Jordyn's program. Reviewing a classmate's code is an excellent exercise.

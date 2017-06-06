---
layout: post
author: businessowl
title: "Aaron Plocharczyk's reflection post"
---
<strong>Lightbulb moment:</strong>
<br/>
When creating my blackjack game, I tried to pass a list of the cards in the user's hand to a function that would evaluate the value of each card and total it. But after I got the total, it seemed like the user never had any face cards. It turns out that this was because I was overwriting values in the supposedly "local" list that got passed into the function I was calling. I realized then that even though the list was passed as a parameter, its scope was not local to that function. It was a pointer to a list instead of a separate copy of the list, so I had been overwriting values on a larger scope than I had intended. In the future, when I pass lists to functions, I will clone the list before editing it so I don't run into unforseen complications. Here is the beginning of that function where I was having the problem:
```
def hand_to_score(hand):
  my_hand = hand[:] # this line clones the list and solves the issue
  
  for i in range(len(my_hand)):
    if my_hand[i] > 10:
      my_hand[i] = 10
```
<br/>
<br/>
<strong>Confusion:</strong>
<br/>
Editing global variables is different in python than in other languages. I am not used to having to specifically say that a given variable is global at the beginning of a function, and I still gloss over this sometimes. Before I figured out that this was a requirement, I had no idea what was wrong with the code I was writing, but now I understand. It is a constant reminder to remember the scope of my variables. Here is the beginning of a function from the "Simon" game that I made for my clicky turtles post. It exemplifies this concept well:

```
sequence = []
guesses = []

def addGuess(newIndex):
  global guesses, sequence
  guesses.append(newIndex)
```
<br/>
<br/>
<strong>Still fuzzy:</strong>
<br/>
I have never bound a function to a keypress in python, so I think that is something I could experiment with. I have understood the examples in class, but I'd like to try it myself. If I don't try it out in a class assignment, I will definitely give it a go on my own. I think it's something that can be more fully grasped after doing it myself.
<br/>
<br/>
<strong>Problem solving strategy:</strong>
<br/>
I am a huge fan of picking a reasonable direction <i>first</i> and <i>then</i> starting to code. I try to do this all the time so I don't get three hours into an assignment and realize that I don't like what I'm creating or that it isn't going to work well. On my clicky turtles assignment, I got a couple hundred lines into a failed, unexciting experiment before I called it quits and started over, and it was all because I was just messing around and never chose a solid direction to go in when I first started coding. The assignment went much better when I actually decided to make a concrete thing like the "Simon" game.

---
layout: post
author: zman7895
title: "zman7895s understanding of dictionaries"
---


We moved pretty quickly through dictionaries it seemed. After the 30 mins we did in class, I definitely understand how they are set up, organized, etc., and I can immediately see recognize that I could have really utilized them in my blackjack app, but I am not quite sure exactly how. For example, I set up a function with several lines to check card scores by going through my deck and asking if it starts with this, assign it a score of this. I realize that a dictionary could have probably taken care of this by having keys for cards pointing to values for card score. But with the method of how I set up my deck, taking two lists (one of numbers, and one of unicode suits), I don't know how I would have iterated through those, added those as keys, and made values to them. So, while I get the gist, I am certaintly not completely there. The code I have in my app that I believe would have most benefitted from a dictionary is below.

```python
playerhandscore = 0
def getcardscores(card):
  global playerhandscore
  global p_1_card
  global p_2_card
  if card.startswith("2"):
    cardscore = 2
  elif card.startswith("3"):
    cardscore = 3
  elif card.startswith("4"):
    cardscore = 4
  elif card.startswith("5"):
    cardscore = 5
  elif card.startswith("6"):
    cardscore = 6
  elif card.startswith("7"):
    cardscore = 7  
  elif card.startswith("8"):
    cardscore = 8  
  elif card.startswith("9"):
   cardscore = 9  
  elif card.startswith("10"):
    cardscore = 10  
  elif card.startswith("Jack"):
    cardscore = 10  
  elif card.startswith("Queen"):
    cardscore = 10  
  elif card.startswith("King"):
    cardscore = 10 
  elif card.startswith("Ace"):
    if (playerhandscore + 11) > 21:
      cardscore = 1
    else:
      cardscore = 11
  playerhandscore = playerhandscore + cardscore
  if playerhandscore > 21 and (p_1_card.startswith("Ace") or p_2_card.startswith("Ace")):
    playerhandscore = playerhandscore - 10
    p_1_card = "none"
    p_2_card = "none"
```


Part of this issue may be the speed in which we did a few of the class exercises. I missed out completely on the second and third long way to go through and loop the states and the count. I was still trying to fix errors in my first loop while the rest of the class did the 2nd and 3rd long way. By the time I was caught up, we had shortened it down to the 6 lines. Which is good that I know the simple way, but I may have grasped concepts better had I seen it repeated. I plan on going and doing this exercise in full on my own this evening, and then spending extra time on the dictionary hw problems this weekend to try and come in monday feeling closer to medium confidence on dictionaries.


My ultimate goal would be able to grasp this enough where I could go back into my blackjack game and maybe even implement it to be able to shorten up my program and make it more readable. I am not sure if my program is set up to be able to make that change very easily, but I will definitely give it a go after this weekends exercises!

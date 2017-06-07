---
layout: post
author: zman7895
title: "zman7895's Blackjack Game"
---

 Below is my embedded game.
 
 <iframe src="https://trinket.io/embed/python3/099bbc9293" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>
 
 Quick backstory, then reflection...
When I saw the assignment posted I got very excited. I have been an avid blackjack player since I was like 4 years old. In fact, I have been an avid gambler since I was 4 years old. My grandpa taught me all the games before he past away because he himself was a gambler. I started kindergarten early because when the teacher asked my mom why she thought I was ready for kindergarten my mom responded with "he is pretty advanced, he does have a hard time understanding the difference in odds from an inside straight draw to an open ended straight draw though". The teacher agreed I was ready. And the little gambler in me was born. I have gone on to play blackjack often in casinos ranging from Atlantic City, West Virginia, Maryland, down to Florida. I go where the action is. Therefore, I had big dreams for my blackjack app.


Where to start??? After I got excited about the assignment, I started thinking about it day and night. My mind was taking all the things it knew about the game of blackjack and starting to picture what it might look like in code. I was playing blackjack on the computer (as I usually do) while brainstorming and not even realizing I was looking at something on screen that was doing essentially what I wanted my game to do (granted the online casinos have graphical interfaces). I brainstormed my milestone lists throughout the weekend, and came into monday without having even sat down to code yet. However, my brainstorming was very detail oriented and wasn't stuck around simple ideas of concepts, but more of exactly how code would look for it. So on monday, when I finally did sit down, I wasn't beginning from scratch.


I sat down for the first time monday night, and the gameplan was to first create a real deck of cards. That was step one. I utilized two lists I created for card numbers (Ace, 2, 3...King) and card suits (Diamonds, Hearts, Spades, Clubs) and ran three for loops within eachother to create a full blackjack shoe of 8 decks. The next step was creating the dealing pattern that would mimic the real casino. In order to do this I had it deal a random card to the player first, then the dealer's down card, then the second players card, and then the dealers shown card. Each time these cards were being permanently removed from the deck (later on added a shuffle for when the deck would run out) as it would happen in the casino. The next step was scoring the cards. I created a function for both player score and dealer score to equate each card to a number and total them up. This is where the first tricky part I encountered. I wanted to make the Ace equal to 1 or 11, but also not make it choose one and stick with it. I wanted it to change based on what the player or dealer needed. So basically, if the player was using it as an 11, but then got a card that busted him, the ace would change to 1. But I wanted all of this to be automatic. It took lots of plug and play methods to finally get one that worked. That was a hell of an aha moment in the early going and set me up to reach for bigger and better things going forward. My deck loops to create the 8 deck shoe is below.

```python
cardnumbers = ["Ace", 2, 3, 4 ,5, 6, 7, 8, 9, 10, "Jack", "Queen", "King"]
cardsuits = ["♦", "♣", "♥", "♠"]
fulldeck = []
for i in range(8): 
  for number in cardnumbers:
    for suits in cardsuits:
      card = (str(number) + " of " + suits)
      fulldeck.append(card)
```


The next piece was just getting the game flowing. This came together in pieces, and didn't stop until 5 minutes ago. I first added the basic elements, in terms of calling the initial deal, ask to hit or stay, and what to do with each response. That all came pretty easily. At that point my basic game was done and I was happy with what I had in the amount of time I had spent on it, but I was also excited to move on and try many more things. At this point I went to my milestone list and just started knocking items off the list. The first and most important was adding betting. I have always said you can't play casino games with nothing on the line. Why wouldn't you hit and risk it everytime if there is nothing to lose right?? So I added inputs to ask the user to bet, and then kept count of running chip counts, winning and losing amounts, etc. using variables that adjusted based on each outcome. At this point I had a lot of input, between the game itself, the betting amounts, etc. that I decided to safeguard everything with try and excepts, as well as range limits. You can't bet a non money amount, and you can't bet more than you have, etc. I also made it so if you buy back in the amount the player is winning or losing accounts for all buyins rather than just the initial one (found this error thanks to Prof. Hauser). These safeguards actually may have taken some of the most time just because of how many locations of input I had. Some examples are below. 

```python
if betamount > chipcount:
      print("\nI am sorry, you don't have that many chips! Betting more than you have is a sign of gambling issues. I am going to have to ask you to step away from the table.")
      quit()  
    elif betamount <= 0:
      print("\nIf you don't feel confident to risk any money, it is a sign you should stop gambling all together. Come back later!")
      quit()
```


After safeguarding all my input entries, it was onto the really fun stuff. I decided to make things more user friendly, slow down the game in between big moments like waiting to see if the dealer had blackjack, or waiting after you hit on a big hand, etc. I then added more info on the screen so you could see how much you won or lost once you quit, and what the dealer would have had even if you already lost (thanks to prof. hauser's idea), and check how many chips you have at any given time, among other user based aspects. 


The second to last milestone I hit for my game was implementing the aspect of doubling down. Doubling down is when a player doubles his initial bet (after he gets dealt his two cards), but then only gets 1 card to make his hand and then it moves onto the dealer. This is one of the most fun elements of blackjack in the casino and so it was a must for my game. However, a problem I ran into is once I implemented it, you could double everytime even if you had already hit previously, which isn't allowed in blackjack (however it is in Spanish 21). I then had to safeguard it so once you hit and had more than 2 cards, you couldn't double down later on. This was extrememly difficult to do with the way my code was set up, and took a while to find a way around it. Ultimately, if you try doubling later, it will tell you you can't, and just hit normally for you. Not the best thing, as I would like to remove the option, but actually works pretty good and probably mimics how it would go down in a casino pretty well.


Lastly, I added luckyladies. The luckyladies is a side game where you can bet on the side of your hand bet, and get money back based on the initial 2 cards you get. The goal is to get 20 total on your first two cards. If you do, you get paid back at some kind of odds (usually 2:1). If your 2 cards are 20 and they are the same suit you get back money at even higher odds (like 9:1). If they are the same exact card, higher odds, and if they are both queen of hearts (lucky ladies) you will be rich! I implemented this into my game and was surprised how smoothly it fit into my logic. It just needed to check score and cards right in the beginning of the hand and return the result. It was pretty awesome. The only trouble was that at first I could bet the luckyladies even if I had made a bet on that hand that would leave me with 0. I eventually added it so if my chip count minus that bet amount was <5 you don't get the lucky ladies option. This code is below.

```python
if chipcount - betamount >=5:
      luckyladies = input("Want to put 5 bucks on luckyladies?")
      luckyladies = luckyladies.lower()
    playerhandscore = 0
    dealerhandscore = 0
    dealinitialhand()
    playerhasnothit = True
    dealt21 = True
    dealer21 = True
    getcardscores(p_1_card)
    getcardscores(p_2_card)
    if (luckyladies == "yes") and (playerhandscore == 20) and (p_1_card == p_2_card):
      chipcount = chipcount + 500
      print("Wow, identical cards, you just got paid 100:1 on that for 500 bucks!")
    elif (luckyladies == "yes") and (playerhandscore == 20) and (p_1_card[-1] == p_2_card[-1]):
      chipcount = chipcount + 125
      print("20 with matching suits, that pays 25:1, take this 125 bucks you lucky lady!")
    elif (luckyladies == "yes") and (playerhandscore == 20):
      chipcount = chipcount + 20
      print("Lucky Ladies hit again, 4:1 for 20 bucks, not bad at all!")
    elif (luckyladies == "yes"):
      chipcount = chipcount - 5
```
 
There are still things left on my milestone list I didn't accomplish. They are listed below in order...

1) Splitting hands (my biggest issue is missing this major component of blackjack, it would be like not having doubling down, just neccessary to have for a reallistic blackjack game)
2) Offerring insurance to players when dealer is showing an Ace (just another gameplay element that is available in real blackjack that I would like to have)
3) Be able to save the game and the amount of chips one has, and when the program is run again later utilize the amount from the previous game (I assume this deals with saving and loading, but just seemed to daunting to start after all the other work)
4) Just making the interactions even more user friendly. Accepting more inputs and not defaulting to certain answers if it wasn't a specific input. Overall I have a lot of safeguards that make this actually pretty decent, but definitely a few places it could get better.


That's it, hope you enjoy and win some mooohlahhhhhh!!!!
 

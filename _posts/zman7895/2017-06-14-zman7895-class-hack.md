---
layout: post
author: zman7895
title: "zman7895's class hack post"
---

Below is my embedded trinket.

<iframe src="https://trinket.io/embed/python3/9065d6f27e" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

I took my blackjack game and created a class for a player. Essentially, the player class has your standard initializing function that requires two parameters, name and nickname. Then, the functions are to getname, getnickname, and a string method that returns a small statement. In my blackjack game I made it so a player gets initialized at the beginning of the game, and the two paramters are created by asking the user for inputs to enter their name and nickname. Then, through methodcalls to the class, the name is utilized throughout the dialogue in the game. Some example code to make this happen is below. I feel fairly comfortable with the creation of a basic class. I will be interested however, to see how to take my final project and implement a class when I am struggling to figure out what could be turned into a class. I look forward to the challenge though!

```python
  while getbuyin: 
    try:
      initialchipcount = float(input("So " + mrplayer.getname() +  ", how much would you like to buy in for?"))
      getbuyin = False
```

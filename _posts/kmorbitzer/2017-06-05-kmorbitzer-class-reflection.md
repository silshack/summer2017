---
layout: post
author: kmorbitzer
title: "Kathryn's class reflection"
---

I’ve learned a lot in this class so far, but it’s been challenging.  The first lightbulb that went on for me was during our first exercise, the turtle drawing.  I drew a castle and it was quite simple, but to make it symmetrical took a lot of time.  That being the first program I have done, it made me realize how much concentration and precision is needed for programming.

```python
tina.speed(30)

tina.penup()
tina.right(90)
tina.forward(170)
tina.pendown()
tina.right(90)
tina.forward(160)
tina.right(90)
tina.forward(225)
tina.right(90)


tina.fill(True)
tina.forward(30)
tina.left(120)
tina.forward(30)
tina.left(120)
tina.forward(30)
tina.color("orange")
tina.fill(False)
tina.fill(True)
tina.color("black")

tina.left(120)
tina.forward(60)
tina.left(120)
tina.forward(30)
tina.left(120)
tina.forward(30)
tina.color("orange")
tina.fill(False)
tina.fill(True)
tina.color("black")

tina.left(120)
tina.forward(60)
tina.left(120)
tina.forward(30)
tina.left(120)
tina.forward(30)
tina.color("orange")
tina.fill(False)
tina.color("black")
```

Another lightbulb went off during the clicky turtles exercise.  I had to create a lot of functions to get my tic-tac-toe game to work, including creating every scenario for a player to win, but the game was fun to play when I finished.

```python
def did_win(board_s):
  if board_s[0] == 1 and board_s[1] == 1 and board_s[2] == 1:
    tina.goto(0, -180)
    tina.write("Player 1 wins!", None, "center", "16pt bold")
    print("Player 1 wins")
```

Being this is my first time programming, I experience confusion during every exercise, but can normally figure out a way to solve whatever I’m doing.  It’s definitely made me realize how coding is an iterative process.
I’m still fuzzy on when to use ‘’ vs. “”.  I usually try one or the other until one works.  That also gets into my problem solving strategy.  I’m someone who just likes to keep trying things until I can get it to work.

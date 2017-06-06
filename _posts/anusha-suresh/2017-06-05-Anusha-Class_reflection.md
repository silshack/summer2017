---
layout: post
author: anusha-suresh
title: "Anusha's Class Reflection"
---

Until the last week or so, I have felt quite confident about my progress in the class. I found that I was much happier with all of the open ended exercises. I always started them with a lot of hesitation, but was content with the final products. In terms of the chapter exercises, I seem to stumble upon them. I think I just put too much pressure on myself to understand problems that other people give me, so I cannot understand right away. I have to take a lot of time to think about the issues and I tend to over complicate the solutions. These are things that I have been trying to work on. Usually, when I run into an issue, I try to understand what the program wants me to do. Then I think about the steps that the program needs to take. I think my main issue then is that I get stuck on simple things and sometimes the hard code itself. When it comes to mathematical programs, those I get very tripped up on. If you recall the computegrade function. I struggled very much on that one, but the code is very straightforward. I think the issue I was having was converting the score to a float and then where that line should be placed in regards to the try block. Oddly enough, I am very proud of the code below.
```python
input_score = input("enter score.")
try:
  score = float(input_score)
  if score > 1.0:
    print("please enter score within range")
  elif score >= 0.9:
    print("A")
  elif score >= 0.8 :
    print("B")
  elif score >= 0.7 :
    print("C")
  elif score >= 0.6 :
    print("D")
  else :
    print("F")
    
except:
  print("please enter a score within range")

```
I think the piece of code that I most satisfied in life is some code from my treasure hunt.
```python
  else:
        our_screen.bgcolor(random.choice([ "magenta", "red", "grey", "yellow", "light blue", "green", "gold", "pink", "purple"]))
        print("you are this far away: ", tina.distance(treasure_xy))
        # Tina points to the treasure, but with random error for difficulty  #borrowed this line from elliot's treasure hunt
        tina.seth(tina.towards(treasure_xy)+random.randint(-25,25))
        tina.pendown()
        tina.circle(2)
        tina.penup()
        tina.goto(0,0)
        tina.seth(0)
```
I am very happy with this code for the sole line about the background color. For the life of me, I could not figure out how to change the background color on each submission. I was moving that line, left, right, up, down, sideways, every possible place. Then when I was writing my reflection for that assignment, I figured out that this was the place to put it, and there was a huge sigh of relief right then

In terms of things I am still fuzzy on, files, lists, strings, and slicing, are all high on that list. I am still trying to understand them. I think a couple of those fuzzy things will come with practice, but then there are a few of those that just require me to keep working and reading in a way that I can understand. Oh, also global variables. I have no clue about those ones. I'm in a spot where I feel like there are a lot of concepts coming at me while I still don't understand some others, so I'm just trying to navigate my way through everything. I feel like going forward, I can and want to do more, it just requires me to get out of this funk first.

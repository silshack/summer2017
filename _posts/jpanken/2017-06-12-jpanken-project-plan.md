---
layout: post
author: jpanken
title: "Jaffa's Project Idea and Work Plan"
---


Although I considered adapting ‘Hungry, Hungry Hippos’ for Turtle, I decided that analyzing data would be more useful for me.  I went to <https://www.kaggle.com> and downloaded a dataset of the most backed projects from Kickstarter.  I’ve been working on cleaning up the data so that I can break down the success stories by category, study the relationship between goals and amount pledged, and how much each backer pledged on average.  I will have to think of other ways to use the data, but I am just getting started.



Right now, I have a piece of code that calculates and displays the percentages of each category over 0%.
```python
categories=set(categories)
for category in categories:
  count=0
  for line in mb_list:
    if line[1] == category:
      count+=1
    else:
      continue
    percentage = int(100*count/len(mb_list))
  if percentage>0:
    print(category + "\t" + str(percentage) + "%")
  else:
    continue
```
It is based off the final part of the CSV 1 homework.  That code works for both the domestic and foreign datasets.



Before I go any further, I need to decide whether to include the titles of the projects.  They certainly won’t make a neat table, but it seems that ship might have sailed anyways.  It might be nice to have a function that allows the user to search through the title for keywords.  After that, I will work to design a bunch of different ways to use the data. 

---
layout: post
author: grassycheetah94
title: "Thomas' Reflection"
---

This class has been a blur, but I feel like I have learned a lot. Although it has been a constant grind,
I have had many lightbulb moments. I think there have been non-bigger than the one I had just last week. During the Email Extractor Correction exercise I worked with Sam as we both had put in a lot of effort, but couldnt get it quite right and both of us had lightbulbs go off in different ways. It was a really good example of how thinking through a problem as a team is helpful when coding. 
Here is the example code:

```python
fhand = open('mbox-short.txt')
count = 0
for line in fhand:
    words = line.split()
    if len(words) > 2 and words[0] == 'From' :
      print(words[1])
```

A simple 6 line code that was the solution to hours worth of problems. The lightbulb moment came when we both realized that we needed to define what we wanted instead of defining what we didnt want. 

Another lightbulb moment I had was when I was trying to define the space that tina could not go to so as to stop the poet in the Slam Poetry exercise. 
Here is the example code:

```python
while (True):
  y = tina.ycor()
  def check(y):
    if (y>-176):
      return True
    else:
      return False
  check(y)
  if check(y) == False :
    break
```

Using while true was about the 8th way I tried solving the boundary issue. It was an assignment I acutally thoroughly enjoyed because it was an 'advanced' problem that I had enough time to think about and finally succeeded in writing code that successfully fixed my problem. 

"For" loops are still pretty fuzzy and for me the best way to alleviate this issue is to just continue to use it and read about it. I constantly go back to read the loops chapter and eventually when I practice enough it will ingrain into my memory. 

A problem solving strategy that has worked for me is simple rest. Just getting away from the computer and refreshing my brain has done wonders. I had to walk away from the computer at least twice when writing my slam poetry code. When you come back the code becomes a fresh canvas in which you can see the issues more clearly and you dont get caught up in what you have already written. 

I have also found working with a partner has been very useful. Sometimes just because they know something you dont, but mostly because it makes you form your ideas fully in order to explain it to your partner and it becomes clear whether or not it will work or not much faster. 

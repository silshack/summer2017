---
layout: post
author: alexreher
title: "class reflection"
---

For loops and lists were a little confusing to me at first. I'd used them a long time ago for another class, but they had a counter and it always seemed to be defined in integers. The way it works with lists in python was not registering for me until seeing it in the context of the file reading program. It turned out to be much more intuitive than I expected and for some reason that was initially confusing until it was in the format of lines in fhand and word in words. The closeness to natural language suddenly made sense.

```python
for line in fhand:
    words = line.split()
    #print(words)
    for word in words:
```

I had a bit of confusion with the return function. I understood it for the most part, but at some point we did an exercise in class on the screen. Seeing someone else work with it in real time and do a couple different things clarified the return's functionality quickly. 

I'm still not a confident as I'd like to be with the list/string operations. I see those as potentially useful in my work, so getting more practice with those would probably do me some good. I glanced at the Automate textbook and some of that material has immediate practical value to me so I should probably consider getting it. Repetition and making little iterative bits of progress towards developing useful tools is the only way I see myself getting better. If I don't quickly tie it to something useful I will have more trouble sticking with it.

I've been slow to comment much of my code after completing pieces. Our assignments have mostly been short enough that they didn't require comments. Even if I were to revist them I think I could figure them out pretty quickly. The poetry assignment was a little more complex, and while I felt like I could think through it, I had trouble keeping my plans straight as I developed and tested the code. I ended up commenting ahead of actually getting things working and they were little helpful guides or mini-milestones that helped get me unstuck. I started making much better progress once I commented out the plan a bit.

```python
 #loop through all the words  
    count = 0
    while count < tot_words-1:
      #loop through building an acceptable string
      chars = 0
      fragment = input_line[count]
      while chars < max_chars and count < tot_words-1:
        #if adding a word keeps it below the count add a word, count the characters
        if len(fragment)+len(input_line[count+1])+1 < max_chars:
          fragment = fragment + " " + input_line[count+1]
          chars = len(fragment)
        #else send it out, kick out of the loop
        else:
          poem.append(fragment)
          chars = max_chars
        count = count + 1
    poem.append(fragment)    #catches the last piece
```

The stop and come back to the problem later strategy also works well, but it's harder with the short summer sessions. In other circumstances I'd do this more as it really works well.

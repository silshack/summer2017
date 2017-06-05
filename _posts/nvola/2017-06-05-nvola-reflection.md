---
layout: post
author: nvola
title: "Natasha's Class Reflection"
---
I've really enjoyed learning Python. I think my previous experience with coding has helped because I already had a grasp on a lot of the concepts we've covered, but I also think I've been able to flex my problem-solving muscles on the new concepts (or new ways to use concepts I've previously encountered). There have been a few strategies that have worked for me, including stepping away from the computer and task to give my eyes and brain a rest if I'm getting frustrated, and having some water (being dehydrated makes me pretty grumpy/unable to think well). But also coding one piece at a time, rather than trying to do everything at once has been helpful because I can make sure that each individual piece is working as it should. Something that has been particularly helpful is taking it old school and writing out the problem in pen and paper, especially if math or complicated if/else statements are involved. For example, in the Conditionals Exercise Computepay, writing out the calculation for how overtime pay is calculated just wasn't working for me until I wrote it on pen and paper, as I was having some issues with not only the fact that the variables needed to be treated as floats but also because there were some parentheses (and order of operations) involved; writing it out and thinking aloud in normal speech (as opposed to code speak) really helped me to simplify the process and figure out what needed to be done. See code below. 

``` python
hours = input('Enter Hours: ')
rate = input('Enter Rate: ')

try:
  if float(hours) < 40:
    pay = float(hours) * float(rate)
  else:
    pay = 40 * float(rate) + (float(hours)-40) * (1.5*float(rate))
  print('Pay: ' + str(pay))
except:
  print("You have not entered valid input.")
```

I don't know that I've had a ton of major lightbulb moments, but have definitely had some smaller ones, particularly with the syntax.  One major lightbulb moment that comes to mind is working with ```return```. We went over it a few times in class, but it wasn't until the second or third time we went over it, and that I subsequently tested it out for myself, that I finally understand how it worked. So experiencing that confusion and testing it out for myself helped because now I really know how to handle return statements.


I also experienced some confusion around keeping string methods separate from list methods. I don't think I've got those 100% memorized, but I faced this confusion when doing the  Romeo exercise in the list exercises. To combat it, I had to stop and check at various points in the code (and leave comments) to see how things were being stored along the way to know what methods to use next. See the beginning of the code for that exercise below, where you can see I left comments at each point. 

```python
user_file = input('Enter a filename: ')

#opens and reads the file
#lines are strings
file_read = open(user_file).read()

#splits all the lines into individual words
#stored as list, with each word as a string element
all_words = file_read.split()

#creates an empty list to store unique words
unique_words = []

```

Another concept that I think I'm still fuzzy on is defining functions; I understand the base of it, but what I'm still fuzzy on is defining the parameters for the functions. I just don't really understand how to choose the variable names for what goes through there, as I've defined some functions that have parameters with variables that haven't been defined and some with variables that have been defined that have worked… but I've also tried to define some functions that have parameters with variables that haven't been defined and they haven't worked! So I'm still not sure I completely understand what's going on with that.

In this class, I'd like to see more real-world applications of python such as what we see and do in the exercises; seeing everybody's work making games through Turtle is fun, but not being a particularly game-oriented/creative person myself, it has been difficult coming up with ideas at times, and that's not necessarily applicable to what I anticipate doing in any future jobs. Also with the pressure of time given the short timeframe of this class, it can be difficult to come up with an idea, so it would be nice to put the problem-solving strategies to work with some more concrete (to me) examples. . 

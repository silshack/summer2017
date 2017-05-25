---
layout: post
author: grassycheetah94
title: "Thomas' Logical Turtle Exercise"
---

Here is the link to the code I am embedding:
<iframe src="https://trinket.io/embed/python/663e0df644" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>


Reflection:
I wanted to create a calculator for tuition as that affects all of our lives now as graduate students. Here is a copy of my code.
```
#Calculating Tuition
try:
  hours = input('Enter hours:')
  tuition = input('Enter tuition:')
  if int(hours) <= 12:
    total_tuition = int(hours)*int(tuition)
    print('Total Tuition:', int(total_tuition))
  else :
    total_tuition = int(hours)*2*int(tuition)
    print('Total Tuition:',  int(total_tuition))
except :
  print('Error, please enter numeric input (no commas)')
  hours = input('Enter hours:')
  tuition = input('Enter tuition:')
  if int(hours) <= 12 :
    print('Total Tuition:', int(hours)*int(tuition))
  else :
    print('Total Tuition:', int(hours)*2*int(tuition))
#Annual Tuition
if int(hours) <= 12 :
    total_tuition = int(hours)*int(tuition)
else :
    total_tuition = int(hours)*2*int(tuition)
annual_tuition = int(total_tuition)*2
print('Annual Tuition:', int(annual_tuition))
'''
I wanted to add a out of state vs. in-state part of the calculator, but that is the one thing I struggled on the most. I tried for over an hour and then slept on it but still couldnt figure out a good way to do it that was user friendly. Other than that it is a lot like our weekly-pay calculator. I think it has a lot of replay value becuase you'd use it for every semester/year you were in school. 

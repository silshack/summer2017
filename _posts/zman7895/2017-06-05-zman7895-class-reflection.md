---
layout: post
author: zman7895
title: "zman7895's class reflection"
---

Lightbulbs- Picking one lightbulb would be impossible. I have had multiple lightbulb moments every single class session as well as every single night working at home. The first one that comes to mind was working with Matt Zimo in class during a session where we were paired up. He was having a couple issues with his program and we were desperately trying to figure it out. Ultimately, we realized we had a flow of control problem as there were pieces of code that could never be reached due to certain conditional statements. When we realized this we both got really excited and high fived which the professor even noticed and pointed out. As for myself, often times I am working on my own exercises and something will come to me. From simple things to even bigger things. For instance, before we had learned conditionals, I attempted to implement them in my work. I read up on them on my own, and added them to my code. Didn't work. I tried for a LONG time and even emailed the professor a full writeup question. Before he even responded I realized I was missing the indentation on the second line. While simple, it was a huge lightbulb moment. Sometimes, the smaller light bulb is even more rewarding because you can't believe you took so much time on something so small.


Confusion- Confusion like lightbulbs have happened early and often. Functions gave me some of my earliest issues. When using a function without a parameter I seemed to do okay. However, ones with parameters often through me off in terms of what I then would use in the function, what was being inputted, by who, and what it would return. I like to think I have started to figure that out just by utilizing them more often throughout my exercises. The code below shows one of the ones I was originally having a hard time working through (even though I had created it in the first place) and understanding what exactly I was doing.

```python
 def minepositions(name):
   if tina.position() == name.position():
    name.showturtle()
    print("You Lose! You hit a mine!")
    quit()
```

At first, understand what name was, and how it was used in the following lines was confusing. But then I realized that name is just a placeholder for an argument that will go in there. And if tina is entered into name, then the next line refers to finding tina's position, and then the turtle named tina will be shown in the third line. 


Still confused- I am still confused at how to learn how to do something the easiest way. I have quickly learned that there is not 1 right way to do many things. In fact, it seems like there are tons of way to do most things. But that doesn't mean there aren't easier, or even an easiest way. After doing exercises, we often only see 1 or two other peoples code, and since they are open ended exercises they don't always match what you are doing. The HW however, often is looking for a specific thing or item. And yes, there are many ways, but the question or premise allows for us all to compare code and to see or find a simple solution that everyone could use. However, we don't really go over the HW together or in groups. So, I just have to go with what I did, and continue to do it that way in my exercises, even though there may be a wayyyyy easier way. The code below is an example.

```python
runningprogram = True
total = 0
count = 0
average = 0
while runningprogram:
  number = (input("Enter a number:"))
  if number == "done":
    print(total, count, average)
    runningprogram = False
    break
  try:
    numbers = float(number)
  except:
    print("Invalid Input")
    count = count - 1
    total = total - numbers
  total = total + float(numbers)
  count = count + 1
  average = total/count
```

This code works, and returns the results that the HW exercise was looking for. However, I can't imagine that within an except block backtracking variables like I did with count and total is the easiest way. I assume there is a location I could have put try and except that wouldn't have effected those. Or I assume there is just another method to make it so except doesn't effect the variables. I guess just being able to take a common task that we all have to do like a HW, and go over a way that seems like the best way (but of course knowing there are other ways) would be beneficial to me. 


Strategies- I have taken a lot of the strategies from the class notes. Many times I have utilized well timed and well placed breaks when I have hit a wall in my work. A few times I have come back and the right answer or method has immediately hit me and I was able to break through and continue on, however, a few other times I have come back to endure the same issues. My favorite strategy has been going back and looking at my or others old work. Often times, something I want to do for a current exercise, has been done in a similar circumstance in either one of my previous exercises or in other classmates previous exercises. I will go and look at past work and a piece of code will hit me as something that could be similar. I will then go back to my current exercise and ask myself what is different and how could I tweak it to make it relevant. This has worked and helped me immensely on several occassions. My last line of defense is always go to the internet. I try to avoid this, but in the cases mentioned above where even my other strategies didn't work, I will go online and look up what I am trying to do. This has gotten me out of a few jams, however, it has often caused even more confusion as it is hard to find stuff that helps, but doesn't go to advanced for where I am at in this class. 

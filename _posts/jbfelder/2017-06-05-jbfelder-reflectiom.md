---
layout: post
author: jbfelder
title: "Justyn Felder's reflection"
---
<strong>Lightbulb Moment</strong>
<br/>
My lightbulb moment(s) occur when I realize that I completely over look some simple syntax issues with my code. Developing the higher-order code wasn't a problem, and finding ways to simplify it isn't either, but I would forget simple things such as: making sure all whitespace is the same, adding a colon to the end of conditionals, and making sure to use '==' instead of '='. I would forget these simple things and I would go back to look at all my higher-order code for errors, while overlooking the simple stuff. Here is an example:
```
if x <= 10:
# Will iterate through x times 
 for i in range(x):
  createTurtle()
  emptyTina()
```
My code would not run all because I did not add a colon to the end of the conditional. I needed to pay careful attention to my work.
<br/>
<br/>
<strong>Confusion</strong>
<br/>
I usually experience much confusion when trying to create whole programs at once instead of breaking it down into parts that can be meshed together. Usually I jump right in without a game plan, creating much chaos in my code that I can't remember what I was trying to obtain even with comments. Now I try to set up some sort of plan I can follow, but occasionally jumping right in gives me the prefect boost I need to give me a start on my work.
<br/>
<br/>
<strong>Fuzziness</strong>
<br/>
Calling and editing global variables is very different in python. I have trouble remembering to call global variables at the beginning of functions and actively try my best to avoid doing so as I fear I will keep causing mistakes trying to use them. I should actually try using them more in order to become used to their usages so that I will be more comfortable.
<br/>
<br/>
<strong>Problem Solving</strong>
<br/>
One strategy that I use is to setup blocks of code inside my programs that will test code as it progress/as I code it so that I know what I have is working at that point. Whether it is implementing a simple print statement, or creating a counting function, I try to create blocks of code that are irrelevant to the grand scheme of my code but help me know what works and what doesn't. And once I make sure this code works, I usually comment it out while adding "Works" beside of it. Here is an example:
```
#Test to see that user input was taken in [Works]
#print(lines) 

#Test to see that indexes can be printed one at a time [Works]
 #Apply this code to Tina drawing the poetry and add a line where Tina moves down 40 - 100 pixels whenever she finishes an index
#while True:
 #if i < len(lines):
  #print(lines[i])
  #i += 1
 #else:
   #break
```

---
layout: post
author: abaker8
title: "Amandas reflection"
---

     FOR THIS SUMMER SESSION, I THINK ONE OF THE THINGS I DID THAT REALLY WAS NOT A SMART IDEA WAS TAKE TOO MANY CLASSES. I AM UNABLE TO SPEND AS MUCH TIME AS PROGRAMS NEEDS SO I THINK THAT IMPACTS MY UNDERSTANDING OF MANY OF THE CONCEPTS. HOWEVER, I THINK ONE OF MY LIGHTBULB MOMENTS WAS GETTING LOOPS TO WORK, I HAD A LITTLE BIT OF AN ISSUE GETTING LONG LOOPS TO WORK BUT IT JUST TOOK SOME PRACTICE TO GET EVERYTHING WORKING OK. I AM STILL REALLY STRUGGLING WITH CONCEPTS SUCH AS EXTRACTING EMAILS AND MAKING LISTS FROM THEM. I THINK IT WAS AT THIS POINT OF THE SEMESTER WHERE I HONESTLY HAVE NO IDEA WHERE TO GO OR HOW TO PROCEED. I HAVE LOOKED AT ALTERNATIVE TEXTBOOKS, YOUTUBE, SOME ARTICLES AND MORE AND REALLY HAVE NOT BEEN ABLE TO GET THE LIGHTBULB TO GO OFF. SOME OF THE STRATEGIES THAT HAS WORKED BEST FOR ME THIS YEAR IS STEPPING AWAY AND TAKING A BREAK. ONCE I DO THIS, I CAN GO BACK AT SOMETHING WITH AN INNOVATIVE APPROACH AND SOMETIMES GET WHERE I WAS LOST. OTHER TIMES, I EVEN START OVER AND ATTEMPT A NEW CODE THAT WORKS PERFECTLY. 
     FOR THIS CLASS, I REALLY WISH WE HAD MORE IN CLASS CODING SESSION. SOMETHING WHERE WE WOULD GO THROUGH A CODING EXAMPLE SO THAT WE CAN ALL BE ON THE SAME PAGE. WHILE IT IS GREAT TO GO OVER PEOPLE’S TURTLE EXAMPLES, THEY ARE ALL DRASTICALLY DIFFERENT SO IT IS NOT LIKE WE CAN LOOK AT SOMEONE’S CODE AFTER TO SEE IF THE LIGHTBULB WOULD CLICK. I THINK HAVING MORE TIMES WHERE WE CAN CODE TOGETHER WOULD ALLOW US TO FORM SOME BASE CODE INSTEAD OF PAVING OR OWN PATH. IN THIS WAY, SOMETIMES I FEEL LIKE MY Code is complicated and not straight forward and hence could give me problems down the road. While it is difficult to lecture code, I think going about this approach would be really helpful. 


```python
try:
#goal is to figure out two things
#did the person work overtime?
#if so by how much?
#If not, only calculate for 40
#if so need to subtract hours-40
  hours = float(input("How many hours did you work?"))
  rate = float(input("what is your hourly rate?"))
except:
    quit()

#once you have those variables, you can start by calculating the overtime.

if hours > 40:
  overtimeRate = 1.5 * rate
  overtime = (hours-40) * overtimeRate
  # the remaining 40 hours will earn the regular rate
  hours = 40
else:
  overtime = 0

#calculate the regular hours
regular = hours * rate
print(regular + overtime)
python
```


While this exercise was not difficult, I was getting strange error messages. This was one of the times I really needed to use some of the methods we discussed such as taking a break, putting in print or input statements and seeing where I was having the issue.
```python
count = 0
total = 0.0
x = input("Please enter a number: ")
while x != 'done':
  count += 1
  xvalue = float(x)
  total += xvalue
  x = input("Please enter a number: ") 


avg = total/count
print("Your total amount of entries was", count, "today!")
print("Your total was:", total)
print("Your average of all your entries was:", avg)
python
```

Sorry about the later post, I thought it was due at midnight.

---
layout: post
author: Lisetted
title: "Lisette's logical turtle"
---

<iframe src="https://trinket.io/embed/python/8eb8196b88" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

``` 
birthmonth=input("What numeric month were you born (1-12)?")
while True:
  try :
    month = int(birthmonth)
    break
  except ValueError:
    print("Put in a numeric")

if month > 12 :
  print("Error: your birth month should be between 1 and 12")
elif month == 12 :
  print("You were born in December")
elif month == 11 :
  print("You were born in November")
elif month == 10 :
  print("You were born in October")
elif month == 9 :
  print("You were born in September")
elif month == 8 :
  print("You were born in August")
elif month == 7 :
  print("You were born in July")
elif month == 6 :
  print("You were born in June")
elif month == 5 :
  print("You were born in May")
elif month == 4 :
  print("You were born in April")
elif month == 3 :
  print("You were born in March")
elif month == 2 :
  print("You were born in February")
elif month == 1 :
  print("You were born in January")

#= abs(12-month)
print("Your half birthday is in the month number"  , abs(12-month))
```

Reflection: I decided that I wanted to output the user's birth month by getting them to provide the numeric value for the month they were born. The input was generally easy and similar to the trinket exercise, though I did have problems with sending an error if the user provided a nonnumeric or if they provided a number outside of that range. After I created the date input (and one of the error messages) and the month output, I realized it seemed like a rather boring program and added the message telling the user what month their half birthday is. I first tried using an absolute value function, but then realized that that was not the correct way to determine the half birthday and that an if/then statement would be needed because there is one equation if the person is born in the first half of the year and a different equation if they were born in the second half of the year.


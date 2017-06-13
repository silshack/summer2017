--- 
layout: post
author: nurahill
title: "Nura's CH. 13 dict exercise"
---

Here is my code:

<iframe src="https://trinket.io/embed/python3/28479871fc" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

In this excercise, I decided to make it tell the user the: city, county, state, number, street, and zip code. I commented something out from the original code to clean it up a bit. I added some spaces in between inputs to make it easier on the eyes of the user.

I unsuccessfully did a try and exept at the end. I could not figure out how to get error checking to work. whenever the json data doesn't include one of the variables above I get a tranceback with an index out of range. I am not sure how to do that, so I kind of just left it:
```
 try:
      print("The address you entered is: " + number, street, city + ", ", zipcode, county + ", ", state)
    except:
      len(js['results'][0]['address_components']) < 6
      
    if not county or not city or not zipcode or not street or not state or not number:
      print('==== The data your requested is not availabe ====')
      print("this is what's available: " + data)
      continue
```
Because of this issue, I just asked the user "Enter Coordinate".


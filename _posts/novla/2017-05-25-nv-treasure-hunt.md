---
layout: post
author: nvola
title: "Natasha's Treasure Hunt Exercise"
---
Here is my Treasure Hunt Turtles Exercise:


<iframe src="https://trinket.io/embed/python/cb703c766f" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>



The first thing I did to complete this assignment was to print the coordinates of the treasure so that I could know where the treasure was during testing. I did this by using the PRINT statement shown below (taken out of the final code because otherwise there'd be no game!):

```
treasure_x = random.randint(-100,100)
treasure_y = random.randint(-100,100)
treasure_x = int(treasure_x)
treasure_y = int(treasure_y)
print(str(treasure_x) + " " + str(treasure_y))
```


Next, to let the player know how close (or far) they are from the treasure, I decided to change the color of the turtle in addition to printing feedback. I did this just because I thought it would be fun and a more visual way (so the user doesn't necessarily have to read the printed feedback to have an idea of how close they are). The "coldest" color turtle was blue, followed by purple, then yellow, then orange, then red for when the turtle was "red hot" close to the treasure. I did this by using a series of IF/ELIF statements based on the distance between the coordinates input by the user and the coordinates of the treasure. See code below:

```
  # Gives the user visual and printed feedback on how close they are to the treasure
  if (abs(user_x-treasure_x) <= 5 and abs(user_y-treasure_y) <= 5):
    print("You found the treasure!")
    user_has_won = True # If the user is within 5 pixels of the treasure, they win!
  elif (abs(user_x-treasure_x) <= 15 and abs(user_y-treasure_y) <= 15):
    tina.color("red")
    print("You're red hot! \n")
  elif (abs(user_x-treasure_x) <= 20 and abs(user_y-treasure_y) <= 20):
    tina.color("orange")
    print("You're getting hot! \n")
  elif (abs(user_x-treasure_x) <= 25 and abs(user_y-treasure_y) <= 25):
    tina.color("yellow")
    print("Warmer... \n")
  elif (abs(user_x-treasure_x) <= 30 and abs(user_y-treasure_y) <= 30):
    tina.color("purple")
    print("Cooler... \n")
  else:
    tina.color("blue")
    print("You're ice cold. \n")
```

The most challenging part of this assignment for me was coding a way to deal with bad input. Though I understand the TRY/EXCEPT and IF/ELSE statements and how they can be used to verify the input, I was having a hard time thinking of a way to incorporate the two tests required to test for the two potential types of bad input: 1) to make sure the user's input could be converted to an integer (i.e., ensure they input numbers rather than letters) and 2) to make sure the user's input did not exceed the canvas space (defined as -100 to 100 on both axes). I was also having a hard time incorporating both of these into the loop such that if a user's input did not pass both of these tests, they would be re-prompted to enter coordinates, because I obviously did not want the subsequent code (moving the turtle) to run and thus cause an error. Also, the timing of the tests was a really important factor because if the input did not pass Test 1 (is it a number?) then there would be no reason for it to be tested agains Test 2 (is it a valid number?). After extensive Googling, I came across this question in Stack Overflow that saved me by opening my eyes to the CONTINUE statement, which tells Python to go back to the beginning of the loop: https://stackoverflow.com/questions/1843659/how-to-get-back-to-the-for-loop-after-exception-handling. So my final code ended up looking like this: 

```
  # Get user X and Y coordinates.
  # Make sure to handle bad inputs.
  user_x = raw_input("Choose an X coordinate between -100 and 100")
  user_y = raw_input("Choose an Y coordinate between -100 and 100")
  
  # test that ensures that user input can be converted to an integer
  try:
    int_x = int(user_x)
    int_y = int(user_y)
  except:
    print("Bad input. Try again")
    continue 
  
  # sets user input as integers
  user_x = int(user_x)
  user_y = int(user_y)
  
  #test that ensures that user input is within the defined scope
  if (user_x < -100 or user_x > 100) or (user_y < -100 or user_y > 100):
    print("Bad input. Try again.")
    continue

  # Makes Tina go to the user's X and Ys
  tina.goto(user_x, user_y)
```

Unfortunately, I was not able to figure out how to use user click movements. Though the ONCLICK function itself wasn't difficult to figure out (i.e., I was successful in getting the turtle to go to where the user clicked on the screen), I couldn't find a way to return the coordinates of the turtles position (using the turtle.position() function). This was essential to the approach I was taking since the closeness of the turtle to the treasure was based on the turtles coordinates, so I would've liked to have had more time to work on that part (thinking in hindsight/if I'd had more time: I would probably define a new function).
    

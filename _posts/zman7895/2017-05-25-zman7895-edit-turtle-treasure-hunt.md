---
layout: post
author: zman7895
title: "zman7895's turtle treasure hunt"
---

Below is my embedded treasure hunt trinket!
<iframe src="https://trinket.io/embed/python/3ef52a43e0" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

This was a lot of fun. My first step was to take the code provided and finish it just to get it to the point where the game worked and was fully playable. I decided to try and make it as piratey as possible and use directional navigation (like northwest, southeast, etc.) to tell users where they were in regards to the treasure. Once the basics of the game were complete and the logic was working and it was playable, I decided to have my own fun and just hack away. This is when it became quite neat!


I first decided to add a treasure turtle that was of gold color and that would appear once the user won. That was relatively simple and didn't have any frustrations or any aha moments. Then, I moved onto the congratulation celebration. I decided to take the celebration provided, but instead of it creating 100 stamps, I wanted it to create the number of stamps to equal the number of guesses the player made throughout the game, and then also report that number of guesses to the player. I played with this for a bit and then realized I could add a variable prior to the guess loop, and increment it each time that loop played through. I then could call the congratulate while loop for that same variable, and print it out with a congratulatory statement that included that same variable to report the number of guesses by concatenating the strings.


Lastly, I wanted to add mines. I actually surprised myself with this and figured out how to create a mine list relatively quickly, and even was quick to figure out I could randomize each location of the mines by calling a loop on each mine in the list. The aha moment came later when I was implementing the conditionals to see if the player guessed on a mine. At first I had an if statement for each mine, basically asking if the player guessed the exact position of a mine, then do this (aka game over). But then, I realized I could once again crete a function that implemented this logic, and then use a loop to call this function for every single mine that existed. I have to say, this might have been my favorite aha moment of the class so far, and felt really really cool when it worked!


My biggest frustration was not being able to figure out if there was an easier way to add mines to the mine list. I wanted to create 100 mines. However, I was creating each mine with the code below
```
mine## = turtle.Turtle()
```
And then adding it to the list manually
```
minelist = [mine1, mine2, mine3, mine##]
```
I stopped at 30 because it was taking forever. If there was a way to create a new turtle mine, and add it to the list automatically, I would have gone to the 100. I assume I could do this with another function or loop, but I gave that a good hour of an effort and couldn't get it. 


Overall though, this was awesome and a ton of fun!

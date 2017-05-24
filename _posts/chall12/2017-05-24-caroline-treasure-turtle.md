---
layout: post
author: chall12
title: "Caroline's Treasure Hunt Turtle Game"
--- 


Here is an embedded link to my treasure hunt turtle exercise:


<iframe src="https://trinket.io/embed/python/91b46ec019" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>


Reflection:


When I first read this assignment, I had internal dialogue that consisted mostly of panic because I had absolutely no idea how to begin this exercise. After watching the tutorial videos, I felt like I had a much better grasp on how to approach this problem. The first thing that I did was to create Tina as an individual turtle and change her into a disticnt color (pink) that would not appear as a background within the game. Next, I created a black background to act as a neutral to contrast with Tina's pink color and then inserted my treasure as a hidden turtle for the user to find. 

My main struggle was in getting the code to quit the program and provide an error message if a number outside of (-100,100) for x or y was entered into the program. After working through this at the beginning of class, it was brought to my attention that my struggles came from not reading the code chronologically. I was getting frustrated because the code was actually doing exactly what I was telling it to. After reordering my error messages and if statements for the inputs, the code worked and I bypassed this hiccup. Lesson learned for this one!


Afterwords, I thought it would be helpful to inform the user of how they would know if they were getting closer to the treasure or not. The distance of Tina to the treasure is calculated using a distance formula that I imported from math that involves the unknown random coordinates of the treasure and the user's Tina inputs. I initially began to try to code out the actual calculations for the distance formula, struggled, and then figured that there had to be an easier way. Stack Overflow helped with this and pointed me to the math.hypot function that I used (Distance math formula: https://stackoverflow.com/questions/5228383/how-do-i-find-the-distance-between-two-points). I used background colors that were defined by ranges of distance between Tina and the treasure as the way to inform the user of their proximity to the treasure (green - you're far away, yellow - getting warmer, orange - warm, red - hot, celebration - you're there!). 


I modified the congratulations/celebration step of the game by incorporating some code that we discussed in class, which is using a for loop and rotating Tina around slightly to flash different colors before calling the congratulations code and stamping randomly colored Tinas all over the place. I thought that this added some flair to the celebration of winning! 

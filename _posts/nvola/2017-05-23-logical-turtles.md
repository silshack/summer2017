---
layout: post
author: nvola
title: "Natasha's Logical Turtles Exercise"
---

My logical turtles program is a basic grade calculator. The user is asked to input the grade received and the weight for the assignment, is asked whether they'd like to enter more grades, and calculates the final grade. The output is: the list of weighted grades and the final grade.


<iframe src="https://trinket.io/embed/python/6c8da1e644?start=result" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>


The most challenging part of this--aside from coming up with an idea--was learning the ins and outs of lists since we haven't worked with them yet. I had some difficulties with adding the calculated weighted grades to the list; the error message I received reminded me that I need to change the user input to float type. I also did not realize that I could not concatenate a string with the list in the output; again, I relied on the error message to point this out to me. 


The loop was not very difficult since I created a loop in my Turtlehacks exercise, but checking to make sure it work and tweaking it such that it did exactly what I wanted was time-consuming. With more time I would have liked to incorporate logical tests to produce error messages if the user did not enter usable input (e.g., grade less than 0 or greater than 1) or if the sum of the weights they input exceeded 1. 


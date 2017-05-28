---
layout: post
author: zman7895
title: "zman7895's turtle hack"
---
Below is my embedded Turtle Hack program.
<iframe src="https://trinket.io/embed/python/ccad0f5a12" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

I knew from the very beginning I wanted to implement a competitive game for my turtle hack, mainly because I am a competitive person. I decided I was going to do a trivia game between two players. This was all in my mind playing out without being in front of the project. Later in the evening I was watching the NBA Playoffs, and I liked the idea of having the game be a best of 7 like the series are in the NBA. I realized in order to do this, I would need 7 questions, and someone would have to win each round, to make it a best of 7. I didn't know how I was going to do this, but I had my overall idea to sleep on. It was the next day that I sat down in front of my project. I first created the graphic of a black screen with a white finish line. Then I created two turtles to appear as opposing players. I utilized the input method we learned in the exercise to ask players the trivia questions. All of this came pretty easily just off of what we had done in class. Then things got interesting.


I needed to learn how to react to right and wrong answers. I went ahead and read about logic and conditionals. I knew I needed to utilize these to have the playing turtles react to right and wrong answers. Figuring this out took forever, and after an hour of trying everything I emailed the professor for help. Only to realize I was simply missing the colon after the IF statement! I was extrememly frustrated with myself but also relieved. Then I spent a lot of time determining what I wanted to happen when players got it right or wrong, and had to figure out how far a turtle should move in order to make it that 4 right answers (or a combination of right answers and wrong answers by the other player) got the player to the finish line. I tried playing my game, and I realized that what I was typing wasn't always giving me the response I wanted. I realized players might answer different variations of the right answer (for example, capitalized answers versus not capitalized answers). My next step was attending to this issue and adding several right answers.


I had my 7 questions and my variations of answers. Now I needed to figure out how to end the game. The game could go to all 7 questions, and therefore I easily added a finishing touch to the 7th question. However, someone could win after only 4 questions. I needed to both a) figure out if a player had won after question 4,5, and 6, and b) end the program if someone had. After lots of trial and error failure on how to do this, I copped out and just decided to ask if a player had reached the finish line. If the player answers yes, the game ends. I eneded the game by looking up how to stop a program and learned about the quit function. 


Making this was a ton of fun, and there were definitely aha moments throughout. The one improvement I would like to make is have it so the program knows that a player won rather than asking. Once I got to class I learned about the position function, and I immediately realized I could use conditionals to ask if the turtle had reached a certain position behind the scenes and if it has then the game will end and congratulate the player who won. I might go back and try this out if I have enough time!

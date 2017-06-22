--- 
layout: post
author: nurahill
title: "Nura's Final Project"
---

here is my embedded code for my final project:	

<iframe src="https://trinket.io/embed/python/f4fb42a88f" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

After thinking a lot about it, I decided to choose to do a turtle game as my final project. I had this idea of making this game off of my drawing app, then I decided that this idea won’t work at all, and that it would make so much more sense to start from scratch. Last week, once I started, I decided to begin with making all of my images using piskel, instead of starting with coding.  I spent a few days just working on all of those images. Then once I sat down and started the process of coding, this is when I realized that starting from scratch was the more logical steps. My idea for the the game was for it to have a total of 3 levels. The user will have to help a monkey find the hidden bananas.  In the 1st round, the user will have 30 seconds to find 5 bananas. The 2nd round the user will have 30 secs to find 8 bananas, and the 3rd and final round the user will have 30 secs to find 10 bananas. The three levels will look the same, however, the 1st level will have a sunrise, the 2nd level a sun up, and the 3rd level would be night (moon). I intended to have a winning screen and a loser screen. I also wanted to have a timer and score show up. I also wanted to have music and sounds effects playing in the background. After these expectations and starting the process of coding, I realized that some of these things were not happening for me. So I had to do some damage control to change the issues I was having in order to make it work. First, I had a really hard time getting the monkey to ‘find bananas’, meaning that I was not able to figure out how to make the banana click in random location and for it to make a banana show up. I did find some instruction on how to use a timer, but I could not get it to work like I wanted to, so I decided to change that as well. Once those two things did not work out as I planned, I changed the rules of the game by making the user only have 10 attempts (clicks) to find 5 bananas per level. Then after a banana is found the score is placed up top in form of the the number of bananas that the player finds. I also really wanted to add music, but I realized that I was not able to do that with trinket.

In terms of my attitude throughout this process in doing the final project, I can definitely say that there were many attitudes and emotions that emerged. In the beginning I felt like it was doable, but then once I started coding and coming across more complicated ideas, I kind of panicked. I felt really stressed when I got sick, because I felt like I could have been productive during those days, but I wasn’t. Once I got through some of the kinks, and saw more of a finished product, I felt a little better. I definitely felt like my final product should/ could have been better. For example: the score (bananas) stay on the screen every time you reset the game, meaning that when the game is reset, you still see the score of the previews game. Also, the bananas kind of pile beside each other after each level is passed, making it hard for the player to keep track of how many bananas they collected in the current level. I tried .undo(), but it didn’t work the way I wanted it to, therefore I decided to just leave it like that. The monkey shows up in random places in the screen. I have it set to start out where I want it, but then it appears back at 0,0 position, and it also appears in the win screen and lose screen, which I didn’t want. Also, once the monkey finds a banana, the player can just keep clicking in the same area and get points for the same banana, which is something that I would like to change in the future.
Another aspect of this process that really took me a while to get a handle on was this concept of finding the bananas. I could not figure out how to make that happen, so it took me a very long time to test different things and come up with something usable. So I did this:
```
# Create a Banana object that adds points if it is clicked
class Banana(object):

    def __init__(self, x, y):
        self.x = x
        self.y = y
    
    # Checks to see if the monkey is near one or more bananas
    def is_monkey_on_me(self, monkey_turtle):
        global score
        monkey_x = monkey_turtle.xcor() 
        monkey_y = monkey_turtle.ycor()
        # Check to see if the distance between the x and y coordinates of the monkey and banana fall between 0 and 50
        is_xclose = 0 < (monkey_x - self.x) < 50 # Self.x is x coordinate of banana, monkey_x is x coordinate of monkey 
        is_yclose = 0 < (monkey_y - self.y) < 50
        if is_xclose and is_yclose:
            score += 1
            draw_banana()
            pass_level()
        set_level()
```
There are many invisible bananas scattered on the screen, every time you click on the monkey it goes to that location and you have to check to see if there are any bananas around. So, I realized that it was almost impossible to click on the exact location of the banana, therefore i wanted to look at distance instead. So, as you can see in the code above, I subtracted the x and y coordinates of the monkey from each of the bananas of the list, and then I check to see if the distance between both x coordinates and both distance of the y coordinates was between 0 and 50. So if both of those things are true, then a banana was found. If either of them were false, the banana would not be found. 

Another part of the code that I feel like is very important is where the function called process_move takes placde:
```
def process_move(x, y):
    global clicks, score
    clicks -=1
    if clicks == 0:
      out_of_clicks()
    monkey.goto(x, y)
    for i in bananas:
        i.is_monkey_on_me(monkey) # See if monkey is near each banana
    #print("Score: " + str(score), "Remaining clicks: " + str(clicks))
```
What happens here, is that when the monkey is moved (clicked), then the 10 allowable clicks per level are decreased – 1 per click, and also where we check and see if the monkey is near each banana.

The instructions for the assignment were the following:

Both project types must use:
•	External data files. For Turtle, this can be game settings, character data, or etc. For the data tool, this should be your data.
•	Dictionaries: I used dictionaries to store all of my images.
•	Custom modules: I did this to try and separate some of the code up in order to make it easier to read.
•	definite (for) loops: I have two for loops. One is to see how close the monkey is to each banana, and the other is to append a banana object to the ‘bananas’ list.
•	Custom functions: I have several fuctions:
o	A set_level function
o	Pass_level function
o	Out_of_clicks
o	Process_move
o	Show_menu
o	Reset_game
o	draw_banana
•	Custom classes - Extended or created from scratch.: I used a banana class which I explain more of above to use as an example of something challenging I wrote.

Both must be:
•	readably coded: I feel like I did a good job making things understandable by commenting as much as I could.
•	well commented
•	well organized: Also tried doing this by making modules.
•	idiomatic
•	error-free: 
•	(largely) bug free. That is, your core use cases should work. Small bugs are OK but the quality level for the final should be higher than previous projects: when it comes to being error free, I feel like I am far from it. As mentioned above, there are a lot of things that I could have done to make it look so much better. 
Turtle games must:
•	Have a graphical user interface, responding to key and click events: I have that with my monkey and my menu and reset buttons.
•	Have a constantly available help dialog. This can take many forms but should allow the user to learn what they can do in the program at any time: I have this with my menu.
•	Display information about the program’s state such as score or level: I did include the levels, and, however its far from good, I also have the ‘bananas’ as scores.
•	Have at least 3 levels, increasing in difficulty: I do have three levels, but they do not get harder. 
•	Extend a custom Turtle Class: I did not realize that I had to do this, and its to late for me to try and make this happen at this point.
•	Have a ‘win’ screen: check!
•	Have an iterative interface. That is, the user should be able to perform any number of supported actions (such as playing the game over and over): my reset button.
•	Use one or more custom images: check! I used piskel for all of my images.

In terms of sources, here are a few things I found online that helped me undertand some things:

-	This is where I looked into the ycor and xcor:
	https://docs.python.org/2/library/turtle.html#turtle.update

-	for my menu, I did take ‘inspiration from Sam’s help window. I just thought It was a good idea. 

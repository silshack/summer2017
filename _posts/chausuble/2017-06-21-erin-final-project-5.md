--- 
layout: post
author: chausuble
title: "Erin's Final Project Final Update...Probably!"
---

<iframe src="https://trinket.io/embed/python/f5461f8c98" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

When I saw the data analysis option, I instantly knew I would never do it. Maybe I’m more likely to analyze data than create video games, but believe me, I would curl up and die if I had to do the data analysis option. Summer just isn’t the time for crunching numbers! So that left the game. Since it was recommended we build upon one of our earlier programs, I thought about the wizard turtle I did for our first assignment. That seemed like the core of a game - the user picked options to attack the monster. It wouldn’t take that much to make it into a game.

Then again, it would mean I would have to draw A LOT. I wondered about making a different card game. I considered “Cheat”/“I doubt it,” which seemed complex enough for the final project. You could have multiple computer players with different strategies, if and else statements for when they would call your bluff…but that simply didn’t seem fun. The wizard game would let me make art, which I’ve discovered I like doing, and figuring out how to draw with Turtle has become more of a relaxing activity for me. And the wizard game would have lots of visuals, more varied and challenging than just drawing a lot of cards. So I did my first experiment with that.

My first go at this was making the wizard change its picture as it walked around the screen. First, I tried using a “for” loop during an onkey function. That resulted in the wizard’s picture moving to where the user walked it to, and then the wizard firing through its two walking images at blinding speed until I stopped the program. I didn’t think it would be as simple as just switching the turtle shape while the user presses the key, and then changing back once the user releases the key. Even if you hold down the key, it still looks like the wizard is walking.

Great, so the wizard looked like it was convincingly walking. That’s when I had to choose how the wizard would fight. I flirted with the idea of a more “action-y” game, where you would have to move the wizard around with the keys to avoid monster attacks, and get into position so you press other keys to fire spells…I even had a basic concept of how it would go. The problem, I figured, was that if I pulled it off, you would only fight one monster, probably, and I knew programming in moving projectiles or monster strike areas would result in many glitches. I went for the simpler option, which was ultimately more satisfying, since I got to come up with more monsters and ideas for how to fight them, using just three spells.

So, a text-based approach was the way. To do that, however, I would definitely need to be able to change backgrounds and screens as the character moved around. No problem - we’ll just make lots of different screens, and clear them one by one as you get through the game. Not the case! If you use .clear() on one screen, I discovered, the whole program comes to a screeching halt. Oh no, I thought, what do I do now?

Well, if I move the player to a specific x coordinate…I can invisibly move them back to the other side of the screen, and I could at least change the background color. In the moving forward function, I decided, I would have it so that when the player goes to the x coordinate 250, they “refresh” the screen. But what happens when you get to the other side of that screen? Well…we make a nested if statement, which will refresh the current screen again into the new one. And we’ll do that again…and again.

Suddenly, the cute little “move forward” function was starting to become a monster. I still clearly remember the feeling when I saw the result: “Uh oh.” I thought it wouldn’t work! So far, it has…mostly. I made it look slightly less intimidating by making the “refresh” myscreen into a .myscreen_part# function. If the whole function were a real object, I would think of it as a reliable, if creaky, wooden ship. It works as it should for the most part, but sometimes, the screens didn’t change. This was the case in my early programs when I had no drawn backgrounds, just colored backgrounds. Early on, I associated that the background colors wouldn’t change if there was a problem earlier in the program - such as the monsters not appearing right, their monster_#_defeated variables not changing properly…and when they were right, the screen color changed to the correct one. 

This turns out to not necessarily be the case. I’m not sure why sometimes the screens don’t change. Maybe it’s because I hold down the arrow keys for too long, maybe it’s Trinket, maybe it’s a problem I keep overlooking - but sometimes, the backgrounds just don’t change. I can run the program in exactly the same way over and over, and there’s no consistent result. Other people do the same, and there’s no consistent result, either. All I know is that the more I called the my screen.bgpic() function, the more likely it would change to the proper background. Hence, the program is littered with a hefty dose of them!

As I went on, I figured that I would want to show this program to my friends and family. They are not programmers, but after reading about how companies hire people to test their programs, I figured some people could help with find problems with the program. Along the way, they found problems that I was too busy to notice, and helped me figure out what people needed advice on. It was very helpful to have their input!

I decided that it would be helpful to use key functions to display instructions, and also have them print at the beginning of the program if the user wants them to. I also thought that I could include a character the user could talk to for hints, and possibly to receive items in a more advanced version of the program. That’s how I made the “examine” function. As I mentioned in the program itself, it could be built upon to give hints for where the player can find hidden treasures in the different screens.

There were two parts of the project I was dreading: FILES! And jimmying with the spell functions to get them to work on all of the monsters. The files continue to be a mess, but they work in theory! They save properly, and they load almost properly. I’m very, very happy with the progress there. Seriously. Words cannot put how happy I am. There was joy in outsmarting the stupid files with strings and stripping and all that, and for a while, I had a cute idea to concatenate user-created file names with + “.py” so they would always work for me! But then I ran into the problems with using raw_input with .onkey() (the short of it - it will prompt the user for the raw_input forever. Even if you try a for loop!). That was where the user would name their file, and by that point I thought it would be easier on the user and me if we had dedicated file names, so the user just has to type 1, 2, or 3 at the beginning of the game to load their files.

Fixing up the spell functions? That ended up being a fun activity. I loved going back to my first program and being able to find places where I could shorten the function, and make it a lot easier and more flexible to work with. The blizzard_series function gets a lot of parameters - really, a lot - but it works and it was fun doing it. To pull that off, I made a separate trinket that placed the wizard and the monsters where I needed them to be, and then it was just a matter of changing all the variables and parameters for each version of the wizard and monster to get them in the proper place.

So here are some strange glitches: If you load an old file, you end up fighting two copies of the monster at once, but if you defeat one monster, you can walk away, but only sometimes you continue the battle on the next screen. I actually think it depends on how many times you run and prematurely stop the program in Trinket. Several times that I tested the game, the number of times I stopped the program in the middle of a monster fight resulted in that number of clones of the monster appearing. Mysterious!

Furthermore, when the user fights the third monster, there are sometimes problems with where the wizard ends up on the screen. I think it depends on if the user has the Python console window squashed or not, because sometimes, apparently, the wizard ends up on the dragon’s foot rather than in the middle, which messes up where the spells shoot from. It has worked consistently enough that I think it’s a matter of the user’s window, but I can look into it further later on.

Finally, there was the matter of drawing the spells. I realize that turtles don’t draw over other turtles. Sometimes it works if I hide the turtle…sometimes it didn’t? For a long time, I thought the answer was to make new backgrounds that place the wizard and monster in their usual position, and hide their turtles when this background displays. Then, the spell turtles will display properly. Instead, thankfully, I found out that stamps can be drawn over as long as you remember to hide the turtle doing the stamping right afterward. I’ve tried to do this for both the wizard and the monster in each battle, and it seems like it has worked.

For all the drawings, I started by making a base drawing in Turtle, to get a more unified art style. Then, I edited the drawings in Gimp, a free painting software that I found, to add details to them, or help distinguish body parts - the snow bird, for instance, started off as a big white blob before I added the black lines. It looks a little weird compared to everything else, but I’m not good enough of an artist to distinguish a whole, and very snowy bird with just colors. I loved making the treasure chest room, and it’s awesome when it actually shows up.

In retrospect - and for future practice - I would start by planning the separate modules in advance. I think my struggle with using them properly is that since I develop the whole program in the main module, my programs can get very interdependent on each other. At one point, when I was trying to separate the functions into out-of-battle and in-battle modules, it came to the point where I was importing both modules into each other in order for them to function properly. There, I bit the bullet and realized that would be negating the entire point of modules. Before, I was too distrustful of modules to make them to begin with, but now that I know what my problem with them is, I can use them properly. Hey, at least it only took a few weeks to figure out it was only my fault…usually it takes me months, if ever!

In a similar vein, I’m going to practice with using classes more. I know that I could have made all the monsters share one class, or perhaps even made the battle functions into a few classes, but I just didn’t have enough time to practice with them and really understand the details of what’s going on when I create classes. But I made a pretty extensive monster class for the turtle, so I’m satisfied with what I managed to accomplish.

I think after classes are done, I’ll still work on this program to see if I can include all of my stretch goals, and fix up the weird problems going on. I could also do more to have a text-based or purely visual-based game - I thought about it earlier, where you could have the monster damage on the screen. All in all, this was a very, very challenging project, but very rewarding! I’m so happy to have taken this class.

I'm not sure if we're supposed to have this, but here we go:

Milestones:

Basics:
- [x] User can move character by pressing left or right keys
- [x] When the character moves, their picture/.shape() changes so they look different.
- [x] Introduction can include instructions, which can also be accessed with "h" in or out of battle
- [x] Make instructions optional as a part of setup
- [x] You can examine environment by pressing the X key at any time outside of battle to get a textual description of location, or talk to at least one person in the game
- [x] You can enter a battle at specific locations - through tracking player X coordinate. When the player reaches a certain X coordinate, a battle will begin.
- [x] In a "while" loop, the player first types an action in the battle: fire, lightning, ice, and other moves. When the player types in a spell, an animation will play, and when it is done, the monster will take damage. Then, the monster will take an action, an animation will play, and the user will take damage. The battle continues until the user or the monster's health reaches 0. Then, you will win or lose.
- [x] Battle loop has been done; it's just the fancy stuff that needs to be finished
- [x] To do for the above: lose sequence, attack animations, placeholder spell dictionary.
- [x] During battle, the character should not be able to move around the screen when you hit arrow keys. When you win the battle, you can move again.
- [x] If you move to specific location and the monster is defeated, you advance to next area. Turtles are cleared and a new background is drawn.
- [x] When you defeat all monsters and move into the last area, you open the treasure chest and you win the game.
- [x] When the whole thing is working, then start organizing things into modules.

Modules:
- [x] Battle functions (all of these have been done, just put them in a module)
- [x] Out of battle functions (all/most of these have been done, just put them in a module)
- [x] Variables and dictionaries (all/most of these have been done, just put them in a module)
- [x] Monster classes

Variables, Lists, Classes, and Dictionaries:
- [x] Spellbook dictionary: keys for spell name, (possibly?) spell animation/function, the amount of damage the spell normally does
- [x] Monster Object/Classes: functions for monster name, health, attack names, attack damage. Better than a dictionary of dictionaries!
- [x] Player health
- [x] battle_is_finished (for battle loop)
- [x] player_turn_is_finished (for battle loop)
- [x] monster_turn_is_finished (for battle loop)
- [x] "name".Turtle() for each character (player, 3 monsters (NEW note: should be handled under classes), 1 random character, treasure chest, background drawings) 
- [x] A list for the main character's walking animation - it can switch between two images so it looks like they're moving

Art:
- [x] wizard
- [x] spell animations (pull from original turtle?)
- [x] have spell animation play when you cast the spell
- [x] monster attack animation (probably just an explosion-looking drawing) (finished, not implemented yet)
- [x] monster 1 (second illustration to be implemented)
- [x] monster 2
- [x] monster 3
- [x] random person
- [x] treasure chest
- [x] background 1
- [x] background 2
- [x] background 3
- [x] background 4
- [x] background 5 (aka yay you win screen)

Files:
- [x] you can save your progress, even though the game is so short!
- [x] it will save: name, the monsters you have defeated
- [x] as part of setup, allow user to reload file

Stretch goals:

Monsters:
- [x] a unique “strategy” for each: monster would have different attacks, and there is an ideal approach to defeating each monster quickly. (I think on a harder difficulty mode, you would not be able to recover your strength after each battle, so you would need to be more strategic in your decisions. Maybe even the monster can disrupt strategy on the hardest difficulty, but let’s see what I’m actually capable of doing, first!)
- [x] strategy for monster 1
- [x] strategy for monster 2
- [x] strategy for monster 3
- [x] optional: if implementing difficulty levels gets too hectic, have the monsters be the increasing difficulty levels

Extra ideas (elaborate on IF I complete the basics):
- [ ] User can move character by pressing up and down keys, allowing for more exploration
- [x] Implement "time" functions for good pacing through battles and animations, etc
- [ ] In environment, you can open up treasure chests that will give you more options in battle: such as alternate spells, or objects you can throw at the monster, or things like that
- [ ] Therefore: Extra spells (probably can be found/used on higher difficulties to allow for more flexible strategies)
- [ ] More than three monsters
- [ ] Change color of character (with a limited choice of colors)
- [ ] You can choose something to concentrate in: if you’re fast, you will get more chances to have a turn in battle (use += to player_turn or something like that - when player_turn =  multiple of 10 (arbitrary number), you get to go) - in exchange, you get hurt very easily and your attacks aren’t as powerful, but you can do things like put up a shield and immediately attack afterward to make up for it. If you have strong magic, your attacks will do a lot of damage and maybe accrue extra damage during the fight (like, it sets the monster on fire or something), but you are slower, but still have a good amount of health to make up for it. It really all depends on what the final strategies are for each monster.

Not too shabby. Still more to go, but I'm very happy with what I've managed...and very tired. Phew!

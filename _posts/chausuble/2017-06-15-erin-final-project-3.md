--- 
layout: post
author: chausuble
title: "Erin's Final Project Part 3: Update 2"
---

Today's turtle:

<iframe src="https://trinket.io/embed/python/c955fcb173" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

My goals to finish before today's class were:
- [x] Set up the lose sequence - flip over character on back, print “game over,” placeholder for allowing player to load an old save
- [x] Convert the scattered monster programs and turtles into individual monster classes, and make them into modules (skip monster dictionaries for the most part; dictionary will be for the spells instead)
- [x] Copy in the spell animations from my first turtle, stick them in a module
- [x] Make the entries in the spell dictionary - placeholders, at least

That was enough for me! Now I realize that I might have also been able to make my battle loop into a single class, rather than
copying the code for that three times. I would do so if I were making a more complicated game, but right now, with my tenuous
understanding of classes, I think I'm going to have to save that project to experiment with after finals. The goal right now:
get this program in working shape! And not have the player fight stick figures on eye-searing backgrounds.

Right now, I think I have it so that the player transitions into different scenes, fights the stick figure, and when you get
to the end of the game, it prints "You won." If your health runs out - which is currently impossible with how I've set up the
numbers - you lose and the background turns black. Nothing fancy - no special screens, animations, or anything - but it's in
working state!! Still no roadblocks, but now is just what I think is the longest, but fun part - making all the drawings. 
I still think I can keep to the plan!

I did, however, catch a minor glitch: When the player hits the end of one screen, I try to have the screen change it's background
color, so I can tell that the screen transitioned. It doesn't always do this. It's like a 50/50 chance whether it will work or
not. I think it's because if I keep holding down on the right arrow key, it skips that part of the function while it is loading
everything else. And everything else works - you fight the correct stick figure, the right examine message plays, and so on. 
I'm not worried right now - it depends on how the background turtle reacts once I start working on that. If there's still a
problem, I'll cross that bridge when I get to it. I have a few alternative solutions in mind, anyway, like calling the bgcolor
change outside of the function - but I have other concerns right now.

My updated milestone list - like yesterday, either the old items are checked off or not, or I add new items when I think of them.
I'm hoping that I can finish everything on this list, and then make some progress on my stretch goals.

Tomorrow's goals:
Start working on all the drawings!

Weekend goals:
Organize everything into modules, and add lots of comments
Files............

In other words, by next class, I want everything on my milestone list checked off.

Then, stretch goals in order:
Implement time functions (pretty easy to do, it's just testing over and over to see what works best)
Unique monster strategies, programmed in (will probably take the longest, but be the most rewarding)
You can select the color and name of your character when you create them
Explore the environment: find treasures when you examine different places. Higher difficulty level = you can find traps, too, but the treasures are better as well
Create more monsters, which are randomly chosen in the three that you fight
More character custom options: things that change how many turns you get in a battle, how strong you are, etc.

I'm not breaking down the stretch goals until I'm satisfied with everything else, and know what I'll be able to do for my
project.

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
- [ ] Battle functions (all of these have been done, just put them in a module)
- [ ] Out of battle functions (all/most of these have been done, just put them in a module)
- [ ] Variables and dictionaries (all/most of these have been done, just put them in a module)
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
- [ ] NEW: just have spell animation play when you cast the spell
- [ ] monster attack animation (probably just an explosion-looking drawing)
- [ ] monster 1
- [ ] monster 2
- [ ] monster 3
- [ ] random person
- [ ] treasure chest
- [ ] background 1
- [ ] background 2
- [ ] background 3
- [ ] background 4
- [ ] background 5 (aka yay you win screen)

Files:
- [ ] you can save your progress, even though the game is so short!
- [ ] it will save: difficulty, the monsters you have defeated
- [ ] NEW: as part of setup, allow user to reload file

--- 
layout: post
author: chausuble
title: "Erin's Final Project Part 2: Update 1"
---

Final project update 1

<iframe src="https://trinket.io/embed/python/6ce8789d4a" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

So far so good. Almost all of the basics have been completed. I don’t have a lot of time to work on this between now and tomorrow’s class, so my to-do list is pretty simple. There aren’t any roadblocks I can think of beyond…just doing the whole thing! I feel like the stretch goals are ambitious enough, and looks like I can at least complete all the basic parts of the project.

I’ve kept the old items in my todo list, checking off the ones I have done, or just breaking up the ones that I haven’t 100% completed yet.

Today to Tomorrow plan:
Set up the lose sequence - flip over character on back, print “game over,” placeholder for allowing player to load an old save
Convert the scattered monster programs and turtles into individual monster classes, and make them into modules (skip monster dictionaries for the most part; dictionary will be for the spells instead)
Copy in the spell animations from my first turtle, stick them in a module
Make the entries in the spell dictionary - placeholders, at least

Thursday plan:
Brainstorm monster strategies

Plan for the weekend:
Do the art for the game itself
File stuff since I hate working with them
If that really isn’t working, just pull the text for examine functions from a file and complete the requirement

Milestones:

Basics:
- [x] User can move character by pressing left or right keys
- [x] When the character moves, their picture/.shape() changes so they look different.
- [x] Introduction can include instructions, which can also be accessed with "h" in or out of battle
- [ ] Make instructions optional as a part of setup
- [x] You can examine environment by pressing the X key at any time outside of battle to get a textual description of location, or talk to at least one person in the game
- [x] You can enter a battle at specific locations - through tracking player X coordinate. When the player reaches a certain X coordinate, a battle will begin.
- [ ] In a "while" loop, the player first types an action in the battle: fire, lightning, ice, and other moves. When the player types in a spell, an animation will play, and when it is done, the monster will take damage. Then, the monster will take an action, an animation will play, and the user will take damage. The battle continues until the user or the monster's health reaches 0. Then, you will win or lose.
- [x] NEW: Battle loop has been done; it's just the fancy stuff that needs to be finished
- [ ] NEW: To do for the above: lose sequence, attack animations, placeholder spell dictionary.
- [x] During battle, the character should not be able to move around the screen when you hit arrow keys. When you win the battle, you can move again.
- [x] If you move to specific location and the monster is defeated, you advance to next area. Turtles are cleared and a new background is drawn.
- [x] When you defeat all monsters and move into the last area, you open the treasure chest and you win the game.
- [x] When the whole thing is working, then start organizing things into modules.

Modules:
- [ ] Battle functions
- [ ] Out of battle functions
- [ ] Variables and dictionaries
- [ ] NEW: monster classes

Variables, Lists, Classes, and Dictionaries:
- [ ] Spellbook dictionary: keys for spell name, (possibly?) spell animation/function, the amount of damage the spell normally does (can I do a range function in a dictionary? Or just the range values?)
- [ ] NEW: Monster Object/Classes: functions for monster name, health, attack names, attack damage. Better than a dictionary of dictionaries!
- [x] Player health
- [x] battle_is_finished (for battle loop)
- [x] player_turn_is_finished (for battle loop)
- [x] monster_turn_is_finished (for battle loop)
- [x] "name".Turtle() for each character (player, 3 monsters (NEW note: should be handled under classes), 1 random character, treasure chest, background drawings) 
- [x] A list for the main character's walking animation - it can switch between two images so it looks like they're moving

Art:
- [x] wizard
- [ ] spell animations (pull from original turtle?)
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

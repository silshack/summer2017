--- 
layout: post
author: chausuble
title: "Erin's Final Project Part 4: Update 3"
---

Trinket was really on and off this weekend for me. I didn't get as much accomplished as I wanted to, but I did get a lot done.

<iframe src="https://trinket.io/embed/python/ca3895d313" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

Some quick reflections: A lot of the weekend, where I couldn't program, was spent making the art for the characters. That's worked
out fine; I just need to implement the last of my images, and that will be all set. For the most part, the rest of the program
is debugging weird stuff that comes up - sometimes, arbitrarily, the player will have to fight two monsters at once, while
most of the time it's just one monster. Sometimes the backgrounds will change properly, sometimes they will not. I think I'll
be able to resolve these problems before the deadline. Wish me luck!

My goals to accomplish by the end of Tuesday...!
- [ ] Figure out what on earth is going on with the save file function!
- [ ] What's going on with backgrounds? Can I fix them?
- [ ] Toggle the angles for the spells so they hit the monster right
- [ ] Make the dictionary key for attack power into an integer
- [ ] Fully implement the strategies against the monsters
- [ ] Draw the win screen (do this last so I feel all satisfied when I finish the game)
- [ ] Mess around with time.sleep() to touch up the battle loop

Some of the above are requirements, others are stretch goals, but for now, the above are my goals, period.

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
- [ ] monster attack animation (probably just an explosion-looking drawing) (finished, not implemented yet)
- [ ] monster 1 (second illustration to be implemented)
- [x] monster 2
- [x] monster 3
- [x] random person
- [x] treasure chest
- [x] background 1
- [x] background 2
- [x] background 3
- [x] background 4
- [ ] background 5 (aka yay you win screen)

Files:
- [ ] you can save your progress, even though the game is so short!
- [ ] it will save: name, the monsters you have defeated
- [x] as part of setup, allow user to reload file

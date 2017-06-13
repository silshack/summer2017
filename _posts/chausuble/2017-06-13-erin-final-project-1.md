--- 
layout: post
author: chausuble
title: "Erin's Final Project Part 1"
---

My project idea is for a game, and I figure it can be based on the original turtle we made at the beginning of the class, with the wizard and the monster. In this idea, you’d be able to walk around a simple landscape, encounter three monsters, and when you beat them all, you get a treasure chest and beat the game. During the encounters, you and the monster can accrue a specific amount of damage through magic spells or attacks. If the monster takes too much damage, you win the battle! If you take too much damage, you lose the game. You and the monster would each take turns attacking.

Milestones:

Basics:
- [ ] User can move character by pressing left or right keys
- [ ] When the character moves, their picture/.shape() changes so they look different.
- [ ] Introduction can include instructions if user types "yes" or something similar, which can also be accessed with "help" in or out of battle
- [ ] You can examine environment by pressing the X key at any time outside of battle to get a textual description of location, or talk to at least one person in the game
- [ ] You can enter a battle at specific locations - through tracking player X coordinate. When the player reaches a certain X coordinate, a battle will begin.
- [ ] In a "while" loop, the player first types an action in the battle: fire, lightning, ice, and other moves. When the player types in a spell, an animation will play, and when it is done, the monster will take damage. Then, the monster will take an action, an animation will play, and the user will take damage. The battle continues until the user or the monster's health reaches 0. Then, you will win or lose.
- [ ] During battle, the character should not be able to move around the screen when you hit arrow keys. When you win the battle, you can move again.
- [ ] If you move to specific location and the monster is defeated, you advance to next area. Turtles are cleared and a new background is drawn.
- [ ] When you defeat all monsters and move into the last area, you open the treasure chest and you win the game.
- [ ] When the whole thing is working, then start organizing things into modules.

Modules:
- [ ] Battle functions
- [ ] Out of battle functions
- [ ] Variables and dictionaries

Variables, Lists, and Dictionaries:
- [ ] Spellbook dictionary: keys for spell name, (possibly?) spell animation/function, the amount of damage the spell normally does (can I do a range function in a dictionary? Or just the range values?)
- [ ] Monster dictionary: keys for monster name, health, attack names, attack damage. Perhaps a dictionary of dictionaries? Oh my!
- [ ] Player health
- [ ] battle_is_finished (for battle loop)
- [ ] player_turn_is_finished (for battle loop)
- [ ] monster_turn_is_finished (for battle loop)
- [ ] "name".Turtle() for each character (player, 3 monsters, 1 random character, treasure chest) 
- [ ] A list for the main character's walking animation - it can switch between two images so it looks like they're moving

Art:
- [ ] wizard
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
- [ ] optional: will save new spells, and - gulp! - customization options?!

If the above is done, we have a basic game we can play, which should satisfy the basic requirements. The rest below is what will make it fun.

Monsters:
- [ ] a unique “strategy” for each: monster would have different attacks, and there is an ideal approach to defeating each monster quickly. (I think on a harder difficulty mode, you would not be able to recover your strength after each battle, so you would need to be more strategic in your decisions. Maybe even the monster can disrupt strategy on the hardest difficulty, but let’s see what I’m actually capable of doing, first!)
- [ ] strategy for monster 1
- [ ] strategy for monster 2
- [ ] strategy for monster 3
- [ ] optional: if implementing difficulty levels gets too hectic, have the monsters be the increasing difficulty levels

Extra ideas (elaborate on IF I complete the basics):
- [ ] User can move character by pressing up and down keys, allowing for more exploration
- [ ] Implement "time" functions for good pacing through battles and animations, etc
- [ ] In environment, you can open up treasure chests that will give you more options in battle: such as alternate spells, or objects you can throw at the monster, or things like that
- [ ] Therefore: Extra spells (probably can be found/used on higher difficulties to allow for more flexible strategies)
- [ ] More than three monsters
- [ ] Change color of character (with a limited choice of colors)
- [ ] You can choose something to concentrate in: if you’re fast, you will get more chances to have a turn in battle (use += to player_turn or something like that - when player_turn =  multiple of 10 (arbitrary number), you get to go) - in exchange, you get hurt very easily and your attacks aren’t as powerful, but you can do things like put up a shield and immediately attack afterward to make up for it. If you have strong magic, your attacks will do a lot of damage and maybe accrue extra damage during the fight (like, it sets the monster on fire or something), but you are slower, but still have a good amount of health to make up for it. It really all depends on what the final strategies are for each monster.

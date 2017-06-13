--- 
layout: post
author: chausuble
title: "Erin's Final Project Part 1"
---

My project idea is for a game, and I figure it can be based on the original turtle we made at the beginning of the class, with the wizard and the monster. In this idea, you’d be able to walk around a simple landscape, encounter three monsters, and when you beat them all, you get a treasure chest and beat the game. During the encounters, you and the monster can accrue a specific amount of damage through magic spells or attacks. If the monster takes too much damage, you win the battle! If you take too much damage, you lose the game. You and the monster would each take turns attacking.

Milestones:

Basics:
- [ ] Character can walk around
- [ ] Introduction can include instructions, which can also be accessed with "help" in or out of battle
- [ ] You can examine environment at any time to get a textual description of location, or talk to at least one person in the game
- [ ] You can enter a battle at specific locations - through tracking player X coordinate
- [ ] In a loop, character attacks, monster attacks, until one loses (ex. while battle_is_finished == False…)
- [ ] If you move to specific location, you advance to next area. Turtles are cleared and a new background is drawn.

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

Extra ideas:
- [ ] Implement "time" functions for good pacing through battles and animations, etc
- [ ] In environment, you can open up treasure chests that will give you more options in battle: such as alternate spells, or objects you can throw at the monster, or things like that
- [ ] Therefore: Extra spells (probably can be found/used on higher difficulties to allow for more flexible strategies)
- [ ] More than three monsters
- [ ] Change color of character (with a limited choice of colors)
- [ ] You can choose something to concentrate in: if you’re fast, you will get more chances to have a turn in battle (use += to player_turn or something like that - when player_turn =  multiple of 10 (arbitrary number), you get to go) - in exchange, you get hurt very easily and your attacks aren’t as powerful, but you can do things like put up a shield and immediately attack afterward to make up for it. If you have strong magic, your attacks will do a lot of damage and maybe accrue extra damage during the fight (like, it sets the monster on fire or something), but you are slower, but still have a good amount of health to make up for it. It really all depends on what the final strategies are for each monster.

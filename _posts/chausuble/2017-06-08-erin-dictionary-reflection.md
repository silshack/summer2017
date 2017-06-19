--- 
layout: post
author: chausuble
title: "Erin's Dictionary Reflection"
---

My understanding of dictionaries is that they are essentially lists, and you can call the items in the list using strings, which are called “keys.” These items in the strings can use further strings to call upon other attributes held within those items. Essentially, you use these to make more complicated lists, and you wouldn’t have to make a really oversized list of lists. If that’s the case, then I think I understand dictionaries better than lists of lists.

Right now, with the really small scope of my understanding, I’m not sure when and how I would use them. My project ideas are still really simple - lists are easier to work with and understand. Whatever I use them for in my final project, I think I’ll just have to force it in. The in-class exercise does give me a better idea:

```
# mydeck = { "Ace of Hearts" : { "numberical_value": 1, "filename" : "aceofhearts.png", "number_remaining" : 8}, "Two of Hearts" : 2}
```

But would you call on all attributes of the “ace of hearts” at once? Call upon them one at a time? I tried to do this for a little while, but I couldn’t get it to work. I did something like this:

```
print(mydeck[“Ace of Hearts”[number_remaining”]])
```

But no dice. We went over it in class, but I didn’t quite keep up. Maybe the textbook will clarify this.

For what it's worth, here's my take on the first part of the in-class dictionary exercise:

```
# Build a dictionary containing each state and the number of transactions that happened in it

state_number_of_transactions = {}

#for each line in the table…
for line in sales_table:
	#since states are in the seventh line, cut down to that line
	state = line[6]
	#if state isn’t in the dictionary, put it in; it =1 because it is first instance
	if state not in state_number_of_transactions:
		state_number_of_transactions[state] = 1
	#otherwise, add one to the total value
	else:
		state_number_of_transactions[state] += 1
print(state_number_of_transactions)
```

It worked - it wasn't pretty, but it worked.

I definitely want to see what exact examples we can use dictionaries for. If our weekend exercise covers this, hopefully we can get away from the .csv tables - working with them makes my head spin! Thankfully we have the weekend to work on this, and that we went over them together in class, because there is no way I would have been able to accomplish these exercises overnight. 

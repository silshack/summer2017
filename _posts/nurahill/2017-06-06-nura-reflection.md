So far i feel like we've covered a lot of material, as expected for a summer class. I've enjoyed so far the process of creating things with turtle and designing things the most. I like making things look cool, so when I learned that I can make shapes of things, likes stars, i got really excited: 
```
#Stars
ninja.penup()
ninja.goto(140,120)
ninja.pendown()
ninja.fill(True)
ninja.color("medium purple")
for i in range(10):
    ninja.forward(50)
    ninja.right(144)
ninja.fill(False)
ninja.penup()
ninja.goto(0,0)    
turtle.done()
```
Most of the time when we have something due, I spend a lot of time thinking about things and feeling puzzled/freaking out about it because I am confused :/ . At the end of it, i am not a hundred percent sure whether I actually know what i am doing, or if I was just lucky that I got it to work. I am just not really sure I am fully internalizing it. One thing that I’ve notices is that I might be able to make the problems work, but when I have to reapply them in a different situation, I have a hard time doing that. I am actually glad I am turning this after today’s class, because today you showed us how to do list, loops, and how to do .join, etc. The way that you showed us how to do everything was super beneficial for me. The best way for me to learn this stuff is by seeing others use it and then for me to repeat it right after, and maybe adding my own variations to it. the act of watching someone do it and the act of watching it happen in action and redoing it, really helps. The part of the class that I find most difficult is when we do the pair ups. I feel so not confident about what I know, that having to think about things critically on the spot, is really challenging. So I just spend that whole time worried about how much I don’t know and how much my peers know. When I do my work on my own, it takes me a long time but I eventually get there…sometimes. Im just better at thinking about thing to myself. Some of the problem solving strategies that work for me are looking things up online and then trying many different things to make it work. Walking away from my code helps as well. 
This one for example took me a long time to figure out:
```
for line in file:
  if line.startswith('X-DSPAM-Confidence'):
    colon = line.find(":")
    #grab everything starting 2 spaces after the colon. 
    spam_con = line[colon + 2:]
    spam_con_float = float(spam_con)
    total += spam_con_float
    count += 1
    #print("Average spam confidence: " + spam_con)

print("Average equals: " + str(total / count))
```



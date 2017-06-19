---
layout: post
author: nvola
title: "Natasha's Web Dictionaries"
---

Here's my remixed code: 

<iframe src="https://trinket.io/embed/python3/ff4d06ecb7" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>


This was so incredibly frustrating to do. I started by trying to alter the existing code to try to get different values, but that didn't really work out for me. So after a few unsuccessful attempts at that I literally wrote down the entire results section on a piece of paper to be able to make sense of where each key ended a new key began, and when sub-dictionaries started and ended, etc. That really helped becasue looking at it on the screen make it impossible to make sense of how the data were organized. Once I did that and figured out the structure it was a lot easier to pull specific data. I thought the viewport coordinates might be interesting to present in a table, and that address components might be interesting, so I pulled those. Since the amount of address components can vary depending on the specificity of the user input, I used a try/except block and a for loop to loop through the maximum possible number of entries, and of course the information that actually existed is what's presented to the user. See my try/except block below:

```
  try:
    admin_levels = []
    for i in range(5):
      try:
        line = js["results"][0]["address_components"][i]["long_name"]
        admin_levels.append(line)
      except:
        None
    print(", ".join(admin_levels))
    print("-"*40)
  except:
    None 
  ```

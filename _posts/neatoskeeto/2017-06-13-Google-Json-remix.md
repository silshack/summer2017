---
layout: post
author: neatoskeeto
title: "Matt's Exercise with Google Geo API JSON"
---
First, my trinket:
<iframe src="https://trinket.io/embed/python3/c4d6457bed" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

I had quite a bit of trouble with this one. I kept mixing up the lists and dictionary indexes. When I wanted to find the country values, I first tried to make a list of all the "types" in address_components and then use a for loop to find the dictionary keys with those types in the list. It was a mess. I kept commenting out blocks and blocks of code until I finally figured out that I can use an 'in' statement to find the corresponding values:
```
#prints the country (if applicable)
for i in range(len(js['results'][0]['address_components'])):
      if 'country' in js['results'][0]['address_components'][i]['types']:
        print ('Country:',js['results'][0]['address_components'][i]['long_name'])
```
It is so ugly, I'm sure there's a way to clean it up, but I was so relieved to just get it working! The code already printed a bunch of relevant info, so I wasn't sure what else to put in there. I added a statement that says if the location is a natural features like the Grand Canyon. I cleaned up the output and called it a night. 

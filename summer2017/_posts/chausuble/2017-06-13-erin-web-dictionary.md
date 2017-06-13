--- 
layout: post
author: chausuble
title: "Erin's Web Dictionary Exercise"
---

This won’t actually work on my trinket. What I recommend is copy the code below into our homework trinket, which I hope I embedded right:

<iframe src="https://trinket.io/embed/python3/a5172b4281" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

The code:

```
import urllib.request, urllib.parse, urllib.error
import json

serviceurl = 'http://maps.googleapis.com/maps/api/geocode/json?'

while True:
    address = input('Enter location: ')
    if len(address) < 1 : break

    url = serviceurl + urllib.parse.urlencode(
        {'sensor':'false', 'address': address})

    #print('Retrieving', url)
    uh = urllib.request.urlopen(url)
    data = uh.read().decode()
    #print('Retrieved',len(data),'characters')

    try:
        js = json.loads(data)
    except:
        js = None

    if not js or 'status' not in js or js['status'] != 'OK':
        print('==== Failure To Retrieve ====')
        #print(data)
        continue
    
    #most relevant pieces of data...
    #place id/location data, formatted address, lat and long, location type?
    
    #print(json.dumps(js, indent=4))
    if len(js["results"]) > 1:
      print("Too many results - please be more specific!")
    else:
      print("This is what we know about this location:")
      location = js['results'][0]['formatted_address']
      print("Address: ", location)
      try: 
        lat = js["results"][0]["geometry"]["location"]["lat"]
        lng = js["results"][0]["geometry"]["location"]["lng"]
        print('Latitude and Longitude: ',lat,", ",lng)
        try:
          location_type = js["results"][0]["types"][1]
          print("Type of Location:", location_type)
        except:
          print("Error! Type of location not found.")
        try:
          ID = js["results"][0]["place_id"]
          print("ID: ", ID)
        except:
          print("Error! Place ID not found.")
        print("\n")
      except:
        print("Error! Latitude and Longitude not found.")
        print("\n")
```

It looked really intimidating at first, but as soon as I ran the program for myself, I realized it really was not that bad - just a lot to read through. It took some experimenting to figure out where I could get all the different location types of data. Originally, I was going to look for the address, state, zip code, and place ID, since my application for this would be to find mailing addresses. Instead, most of the time, if I looked for the address of a specific location, it would give all of that to me from the start! So instead, I just added whatever I think I could add, like longitude and latitude, play ID, and type of location. I’m really impressed that Python can pull information from the web. I won’t be able to use it for my project, but I had no idea that Python was that powerful by itself!

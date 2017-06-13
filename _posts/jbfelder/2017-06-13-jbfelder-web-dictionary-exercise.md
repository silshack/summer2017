---
layout: post
author: jbfelder
title: "Justyn Felder's Web Dictionary Exercise"
---
</br>
<strong>Embedded Code:</strong>
<iframe src="https://trinket.io/embed/python3/4cc3c5af52" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>
</br>

</br>
</br>
<strong>Reflection:</strong>
</br>
At first, I was very confused as to how I was supposed to change the code to alter the output. I spent at least thirty minutes looking throughout the code with little success. Then I decided to run it and look at the output. That's when I noticed how all the data looked like a dictionary filled with multiple list that were spaced apart. From Line 28 (on my embedded code), I cut out the 

```
indent = 4
```

part of the code and had it just print

```
json.dumps(js)
```

From there I could see how all the data was organzied and where it was located. Using code based on the work preestablished on Lines 30 - 34:

```
lat = js["results"][0]["geometry"]["location"]["lat"]
lng = js["results"][0]["geometry"]["location"]["lng"]
print('lat',lat,'lng',lng)
location = js['results'][0]['formatted_address']
print(location)
```

I crafted my own code to allow the user to see the location of the zipcode they inputted:

```
try:
      address = []
      for i in range(5):
        try:
          line = js["results"][0]["address_components"][i]["long_name"]
          address.append(line)
        except:
         None
      print(", ".join(address))
      print("-"*40)
    except: 
      None
```

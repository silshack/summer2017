---
layout: post
author: businessowl
title: "Aaron Plocharczyk's dictionaries post"
---
The following explanation of dictionaries should be sufficient to complete the first, in-class dictionary assignment.
<br/>
<br/>
Dictionaries are ways of keeping lists that use keys as indexes instead of numerical indexes. Keys are unique strings that are referenced to get a value. If I wanted to give numerical strings a value of an integer, I could do that as follows:
```
mydict = {"one": 1, "two": 2, "three": 3}
```
If you want to get the value associated with a key, you could do that as follows:
```
myvalue = mydict["two"]
# now myvalue == 2
```
If you wanted to get all the keys in the dictionary, you could do that as follows:
```
mykeys = mydict.keys()
# now mykeys == ['one', 'two', 'three']
```
If you wanted to get all the values in the dictionary, you could do that as follows:
```
myvalues = mydict.values()
# now myvalues == [1, 2, 3]
```
You can alter the value associated with a current key as follows:
```
mydict = {"one": 1, "two": 2, "three": 3, "four": 0}
mydict["four"] = 4
# now mydict == {"one": 1, "two": 2, "three": 3, "four": 4}
```
And you can add a new key/value pair to a dictionary the same way, as follows:
```
mydict = {"one": 1, "two": 2, "three": 3}
mydict["four"] = 4
# now mydict == {"one": 1, "two": 2, "three": 3, "four": 4}
```
If you want to check if a key is in a dictionary, you could do that as follows:
```
keyisindict = "one" in mydict
# keyisindict == True
```
And of course, you can check if a value is in a dictionary as follows:
```
valueisindict = 1 in mydict.values()
# valueisindict == True
```
If you want to loop through the keys of a dictionary, you can do so as follows:
```
for key in mydict:
  print("KEY: " + key)
  value_of_key = mydict[key]
  print("VALUE: " + str(value_of_key))

# Prints the following:
# KEY: one
# VALUE: 1
# KEY: two
# VALUE: 2
# KEY: three
# VALUE: 3
```
You can nest list in other lists as follows:
```
# put two dictionaries (i.e. firstdict and seconddict) into another dictionary (i.e. dictionary_of_dictionaries)
dictionary_of_dictionaries = {"firstdict": {"one": 1}, "seconddict": {"two": 2}}

# you can access a dictionary as follows:
firstdict = dictionary_of_dictionaries["firstdict"]

# and you can then operate on that dictionary as with a normal dictionary
```

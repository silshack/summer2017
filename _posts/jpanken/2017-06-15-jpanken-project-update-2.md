---
layout: post
author: jpanken
title: "Jaffa's Project Update #2"
---


<iframe src="https://trinket.io/embed/python3/dbad5d9e83" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>


Since my last post, I have compiled a help dictionary that serves as a glossary for understanding the dataset.  I had a hard time getting error management to work on the help menu.  Whenever I would enter bad input, the dictionary wouldn’t find the entry and would return 0 as the value.  Since it didn’t trigger an error message, the “except” message wouldn’t print so it thought that it had worked.  Instead, I set it up this way:
```python
def get_help(a_dict): #help menu connects to help_dict
    get_divide()
    help_num=input("""Which data would you like to know more about?
1 - goal
2 - pledged
3 - deadlines
4 - launched_at
5 - backers
6 - locations
7 - categories
8 - create_to_launch
9 - launch_to_deadline
Enter the number of your choice:""")
    if help_num=='1':
      help_choice='goal'
      help_answer=a_dict.get(help_choice, 0)
      get_divide()
      print(help_choice,'is the', help_answer)
      get_divide()
    elif help_num=='2':
      help_choice='pledged'
      help_answer=a_dict.get(help_choice, 0)
      get_divide()
      print(help_choice,'is the', help_answer)
      get_divide()
```
…and so on.


I thought that it was undesirable for the user to import the actual name of the data type because there were so many possible errors.  Instead, I used a number input menu.  The code is very long and I’m going to work on making it more concise.  First, I will run the problem by my group members and see if they have any suggestions.


For the weekend, I want to get the option menus set and start connecting them to the data.  In addition, I would like to work on creating a class that helps me structure the presentation of the data.  I think that might already be functions called “format” so maybe call it class Style.  It may not be a class, but just a function.  I’ll have to experiment and see what I come up with.


###Milestones
- [x] Import clean data files into program
- [x] Compile each column in list for ease of use
- [x] Offer a help dictionary in all of the options menus
- [x] Provide additional information about datasets and types of data
- [ ] Present help menu in an elegant way
- [ ] Create a class Style to keep user interface and output organized
- [ ] Options menus with 2-3 layers
- [ ] Divide data into logical subsets for the options menus
- [ ] Develop error management
- [ ] Settle on format for data visualization

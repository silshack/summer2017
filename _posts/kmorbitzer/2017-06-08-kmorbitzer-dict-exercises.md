---
layout: post
author: kmorbitzer
title: "Kathryn's dictionary exercises post"
---

Below is the code that I used:
```python
file_name = input("What file do you want to use?")
# Open our data and store the output
with open(file_name) as f:
  sales_lines = f.readlines()

# Build a list of lists data structure
sales_table = []
for line in sales_lines:
  # Append the line, but split into a list on each ','
  sales_table.append(line.split(","))
  
sales_table.pop(0)


# Build a dictionary containing each state and the number of transactions that happened in it
state_table = []
dictionary_table = []
counter = 0
while counter < len(sales_table):
  state_table.append(sales_table[counter][6])
  counter = counter + 1
  
counter = 0
trans_count = 0
total_trans_count=0


temp_state_name = 'xx'
while len(state_table) > 0:
  trans_count = state_table.count(state_table[0])
  temp_list = []
  total_trans_count=total_trans_count+trans_count
  temp_list = [state_table[0], trans_count]
  dictionary_table.append(temp_list)
  temp_state_name = state_table[0]
  while temp_state_name in state_table:
    state_table.remove(temp_state_name)

# Print an alphabetized table of each state and its # of transactions, separated by tabs
dictionary_table.sort()
counter = 0
while counter < len(dictionary_table):
  dictionary_table[counter][1] = str(dictionary_table[counter][1])
  counter = counter + 1
  
  
counter = 0
while counter < len(dictionary_table):
  print("\t".join(dictionary_table[counter]))
  counter = counter + 1

# Build a dictionary containing a dictionary for each state containing 
# number of transactions and total transaction value (the sum of Prices
# of all transactions that happened in that state)
counter = 0
dictionary_table2 = []
while counter < len(dictionary_table):
  temp_list = [dictionary_table[counter][0], dictionary_table[counter][1], 0]
  dictionary_table2.append(temp_list)
  counter = counter + 1
  

state_table_new = []
dictionary_table_new = []
counter = 0
while counter < len(sales_table):
  state_table_new.append(sales_table[counter][6])
  counter = counter + 1
  

trans_count = 0
temp_state_name = 'xx'
while len(state_table_new) > 0:
  trans_count = state_table_new.count(state_table_new[0])
  temp_list = []
  
  temp_list = [state_table_new[0], str(trans_count),0]
  dictionary_table_new.append(temp_list)
  temp_state_name = state_table_new[0]
  while temp_state_name in state_table_new:
    state_table_new.remove(temp_state_name)
  

counter=0
counter2=0
while counter < len(dictionary_table_new):
    counter2=0
    while counter2 < len(sales_table):
        if dictionary_table_new[counter][0] == sales_table[counter2][6]:
            dictionary_table_new[counter][2] = str(int(dictionary_table_new[counter][2]) + int(sales_table[counter2][2]))
        counter2=counter2+1
        
    counter=counter+1


# Print an alphabetized table of each state, the number of transactions in the 
# state, and the total value of all transactions in the state, separated by tabs
counter = 0
while counter < len(dictionary_table_new):
  print("\t".join(dictionary_table_new[counter]))
  counter = counter + 1

# Modify your program to let the user choose between sales.csv and homes.csv.
# If the user chooses homes.csv the program should print out correct tables as above.
# Code for this part of the assignment will likely be at the top of your program.
```

Here is my reflection:
I originally tried doing this exercise over the weekend.  That was before I really knew about the dictionary data structure, so doing it was more difficult than what we did in class because I tried doing it with lists.  Therefore, it took a long time to get it to work.  I was having trouble with the original sales data table and getting multiple occurrences of states added up correctly in my own list. From the code performed in class, I can see that it’s easier using a dictionary data structure.  

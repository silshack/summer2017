---
layout: post
author: jbfelder
title: “Justyn Felder’s Final Project”
---
</br>
<strong> Final Project Code: </strong>
</br>
<iframe src="https://trinket.io/embed/python3/2999432753" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>
</br>
</br>
<strong> Final Reflection: </strong>
</br>
For my project, I created a weather app that pulls data from a certain location using the Open Weather API and outputs it to you by giving you 1) Today’s Forecast, 2) Tomorrow’s Forecast, 3) Current Weather, 4) Bar Chart of Five Day Forecast Maximum Temperature, 5) Bar Chart of Five Day Forecast Minimum Temperature, and 6) The Raw Data of the Five-Day Forecast. My idea for the creation of this app stems from my hatred of the iPhone stock weather app. I would say that 50% of the time, the app gives the wrong weather. This annoyance is what drove most of my work as I attempted to use as much data as I could to mimic their structure.
</br>
</br>
To start off this project, I searched for different weather API’s that had free subscriptions and enough data that I could pull from. In the end, I chose the Open Weather API. This API allowed me different amounts/types of data that I could work with. I used the “5 Day / 3 Hour Forecast” data to begin my work. While I wanted to jump right into the code, I needed to understand how the API worked and how to integrate it into my program. Open Weather API has a useful document that shows how to different API calls as well as how to modify the calls to your liking. I chose to modify my API call so that it took in a city’s name as well as the country it is located. I also changed the call so the data would be return in a JSON format, instead of XML, and all data would be returned in Fahrenheit, instead of Celsius. From these modification, I allowed the city and country to be inputted by a user, which was then taken in and added to the API call in the correct format. This returned a proper API call that I tested in my Google Chrome browser for its success. Once I was positive it would work without fail, I moved on to actually coding my program.
</br>
</br>
To start my program, I created modules for all the different information I would need or create. One module handles creating the API call, another uses the call to establish access to the API and pull its data, the third creates the information I wish to show, and the last is my Main where the bulk of the code would handle the calls and integration. 
</br>
</br>
Using the code I had already created for testing the API calls, I simply added the call creation into its own module and made it a Class. I created this class as all locations are different, but share similar properties so using a class would be the most efficient way to handle it. From there, I had to find out how to establish access to the API using Python/Trinket. As I have never worked with this before, I checked Stack Exchange for help and saw that I needed to import the json and urllib libraries. From there I followed instructions on how to open up a connection, decode its data, output its data to a local variable, and finally close the connection while returning the data. When looking at the data returned, it was a dictionary of lists of dictionaries where all different yet similar. Using the pprint function, I saw that the data I called was exactly what I wanted. Weather information about five different days being report every three hours. As much as I wanted to move on, I still had trouble understanding dictionaries. So instead of trying to work around it or look for help online, I asked my group members for help and went over the chapter of our reading that went over dictionaries. After I spent about two days doing that, I tested pulling out different types of information from the data. I tested using code such as:

```
specific_name = raw_api_dict[‘city’][‘name’]
```

that returned the exact city that I had input, but with proper spelling and grammar.
</br>
</br>
Know that I wanted specific weather stats about each day and data was stored for every three hours, I knew that I needed to find a way in which I could go through all data but only store the top results for each day. Not knowing how to do this, I tried many methods. I tried a For Loop inside of another For Loop that would check the date and then the time. This did not work. I tried to store all the data in a dictionary and select what I would need out of there. However, this did not work as my data is constantly changing and for me to get this code to run successfully I would need to go in and change I every three hours. Stuck, I went to one of our project updates and asked my group members for help. They too were confused as to how in could be done successfully. It was then that I got up, went to the whiteboard, and tried to whiteboard code it out. I wrote down test data, how data is formatted, and how I imagined it could work. With this sample in mind, I asked Elliot for help and we walked through step by step on how I could get this data traversing to work. Once he finished helping me, I sat down and made sure I completely understood what each piece of the code did. Then, I implemented in the module I set up to show different types of information. Using the code we worked on, here is a small snippet of how I configured it:

```
def get_max_temps(raw_api_dict): #Get dict of min temps
  day_max_stats = {} #Empty dict
  for i in range(len(raw_api_dict['list'])): #Iterates through all the data
    date_string = raw_api_dict['list'][i]['dt_txt'][:10] #Slices just the date part of the date-time string
    if date_string in day_max_stats: #Checks if it is in the dict
      current_max = day_max_stats[date_string]#If so, its (key) current value is equal to current_max
      new_temp = raw_api_dict['list'][i]['main']['temp_max'] #Any string that matches up with the date will have its max temp taken
      if new_temp > current_max: #If new_temp is greater than current_max
        day_max_stats[date_string] = new_temp #The new_temp is the current max
      else:
        continue #If not then move on
    else:
      day_max_stats[date_string] = raw_api_dict['list'][i]['main']['temp_max'] #If the date in not in the dict, it will be added with its current max temp value
  return day_max_stats #Returns the max temp dict
```

From here, I used this code as a blueprint for how I could take other types of data. By creating new dictionaries and variables, changing the ones in the pre-established code, and calling the right data I was able to get dictionaries for not just max temperatures but minimum temperatures, humidity, and wind speed.
</br>
</br>
Having the data that I wanted to show and display, I needed to find a way to find data for specific dates. For this I returned to Stack Exchange where I learned how to use the datetime library to create “today’s date” and format it so that it matched the date assigned to the data pulled from the Open Weather API. From there, all I had to do was iterate through each dictionary and pull the values where “today’s date” matched the key dates. To show all of this data off, I simply created a variable that had a long String assigned to it that had the way I wanted to the data to be displayed as well as the values I called from the dictionaries. I would then simply print the variable. The reason I assigned such a String to the variable is due to the fact that I wanted to implement a file-saving function that would simply save the variable to the file. Knowing that I also wanted to take in weather information about the next day, all I need to do was simply add one to “today’s date” and have that date iterate through the different dictionaries in a way that copies “today’s date”.
</br>
</br>
To create a data visualization, I wanted to use bar charts that would show off the different maximum temperatures as well as the different minimum temperatures. For this part, I imported the Pygal library and used Trinket’s sample Pygal chart as well as Pygal’s own sample bar chart in order to create my own charts. To add data to these charts, I simply iterated through all the keys and values in the maximum temperature and minimum temperature dictionaries and added each one into their respective charts. One problem that I encountered and had to work around is that I am not able to establish a sorted legend as my data is constantly changing. To combat this, I just added the date and hoped that it would be enough.
</br>
</br>
Having finished all requirements for the project, I wanted to go back and add something else. Even though I wanted to add the text-to-speech function, that was a struggle to have done by the deadline so I opted another route. I decide to use the Open Weather API to call in different data. This time I called in current data. To do this, I copied all my pre-existing code for API call creation and using the call. To compensate for this, I differentiated between the different functions by stating which ones were for the five-day forecast and which ones were for the current weather. The data for current weather was easier to understand as there is only one version of everything and the dictionary of dictionaries that contained all the data was much smaller. This made calling the data as simple as assigning a value to a variable. As I did with calling “today’s date” information, I assigned a long String to a variable and printed the variable while giving the user the option to save their data. 
</br>
</br>
From here, all I did set each of these different ways of pulling data to progress when certain conditions were met with IF Statements. These conditions were different options the user could choose from, and all options were described if the user typed in ‘help’. I also implemented all this under a WHILE Loop that allows the user to pick another location once they finished pulling all the data from one location.
</br>
</br>
Creating this final project really challenged me as while the code may seem very simple, there was numerous things I had to use that I had never worked with before. I honestly plan on finishing the text-to-speech function and adding on to this app to make it even better. Once I do all that I can, I plan on uploading to “finished” project to my own personal GIT account. 
</br>
</br>
<strong>Final Milestones:</strong>
</br>

Completed:

- [x] Setup API and API-Key so data may be taken from a location
- [x] Find out how to establish API connection and pull data
- [x] From the location inputted, show all available data that Open Weather has
- [x] Create user input so user is able to decide on location while program is running
- [x] From the location the user inputted, show all available data that Open Weather has
- [x] Find way to establish current date
- [x] Find way to establish tomorrow’s date
- [x] Show all available data from a certain date
- [x] Make program inform (print) out the next day’s forecast
- [x] Show all available data from a range of dates
- [x] Allow the user to commit non-stop searches until they choose to quit
- [x] From a certain range of dates (date of day is the key), take the temperature (current, max, and min) from each day and store it in a dictionary
- [x] Use text based interface such that Options can give back different types of weather information
- [x] Create help menu
- [x] From the temperatures given for a certain day (day is the key), take the temperature (current, max, and min) and store them in either a list or dictionary (dictionary would work better)
- [x] Create a file saving system.
- [x] From all data available, show only temperature (current, max, & min) from the entire day as well as description of current sky
- [x] Visualize data so max and mins are shown as a graph
- [x] Allow user to select a new location when finished
- [x] (Optional) Print out recommendations of what the user should wear tomorrow
- [x] (Stretch) Pull from secondary API
- [x] (Stretch) Get all weather data from real time






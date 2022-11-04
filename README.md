# fb_data_analyzer
Jupyter Notebook for analyzing Facebook news statistics

![ss](https://user-images.githubusercontent.com/113773292/200026027-332e1c22-7705-479e-bd60-977b830dd0c3.png)

## Packages needed:
 pandas (>=1.4.4)
 seaborn (>= 0.12.0)

 ## How to download the data?

Instructions for collecting Facebook data are available from many sources on the Internet (for example, [here](https://www.facebook.com/help/212802592074644).) 

For this script, you need to download a file in JSON format (for data from the entire time period, the message package is usually the smallest possible).

## How to run this script?

Paste the messages_*.json file into the directory where the program is located and execute the Jupyter Notebook file.

## Functions

all_time - function that prints the number of messages, the number of words and the average number of words in the message (for each participant in the conversation)

average_response_time - a function that prints out the average response time for each participant in the conversation in minutes (calculated from all the given data)

the script also allows you to draw graphs divided into different time intervals:
years, months, specific months (e.g. Aprils), specific days of the week, specific hours

to do this you need to write

`bash
sns.countplot(x = df[time interval that interest you])]
```

when you add to the above function parameter

`bash
hue = df['sender_name']
```
The script will draw graphs by individual conversation participants

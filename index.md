# Digital History Exploration Exercise 

Greggory Elton - 101038024

## Investigation Statistics for the Canadian Armed Forces

### Background 

This dataset was is part of the [Open Canada Dataset collection](https://open.canada.ca/data/en/dataset/402358f9-2808-44f7-99b3-58f6f5f95b1f) in which the data explains its tracking of military police incidents and convictions known as the Security and Military Police Information System (SAMPIS). The data collected is between Jan 1, 2014 and March 31, 2019. This represents the number of investigations that took place during the above mentioned period.

Below is the data in it's regular CSV form. Note: I have removed the original column B as it was the french version of column A. 

![CAF](https://github.com/gregelton44/DH-Exploration-Exercise/blob/main/CAF.PNG?raw=true)


### Beginnings
To start this whole shebang off a quick and dirty wget is needed to get the file - "caf-investigations-od-2018.csv" from the interwebs onto my local machine. Once this was done, I wanted to take a quick look in excel just to see what the headers were and what the data initially was about. 

In CS I previously used Wget for simple uses such as downloading a file onto a virtual machine and so on but I never really understood how useful it would be when it comes to archives and historical data. Imagine having thousands or millions of text files, wget can make this a breeze (a long breeze, but we take what we can get). I feel like those who use wget for small things fail to appreciate the beauty of it.  

I used Excel to clean up the data, and generate some basic statistics as well as an all encompassing graph that displays the number of types of calls and crimes reported by year. 
Finally I threw that CSV into Gephi and watched what happened to my screen! It was quite beautiful, but a little scary. 

### Analysis

#### WGET 
To kick things off, I needed to get the data stored on my system so I used the command `wget https://open.canada.ca/data/en/dataset/402358f9-2808-44f7-99b3-58f6f5f95b1f --limit-rate=100k` and made sure to specify the download rate should not exceed 100k, because we don't want to overwhelm the Government of Canada servers (they already can't handle much). 

#### Excel
Next step in my process was to open the csv file in excel and poke around at the data. This is when I noticed that there was an extra column that was in French that simply described the category of the reported crime. I removed this so that other programs like Gephi didn't think there was two sets of headers or categories. 

![CAF](https://github.com/gregelton44/DH-Exploration-Exercise/blob/main/CAF.PNG?raw=true)

Taking a look at the raw data, I noticed right off the bat that the number of calls was trending upward meaning that each year from 2014 to 2019, there has been more crime or reported crime taking place. If we compare years 2014 to years 2019 we can see that close to 10,000 more calls were reported in 2019. Crimes such as criminal harassment and Extortion seemed to plateau around 2015-2016 and fall back down in recent years. 

Some observations that I have come across when using Excel for data parsing and analyzing especially in the CSV format, is that sometimes the encoding can cause issues with software. For example, if I have french characters like an accented a, the enconding in excel seems to mess up that character. Because of this I was forced to remove the french column. Typically, you wouldn't want to modify the data as it sometimes cannot give you the true picture. 

Next, I made a bar chart to visualize some of the data in order to see a clear picture of what crimes took place the most. 

![ExcelGraph](https://github.com/gregelton44/DH-Exploration-Exercise/blob/main/excelgraph.png?raw=true)





It reads [markdown](https://www.markdownguide.org/) and turns it into html.

![gif ftw](https://media.giphy.com/media/nXxOjZrbnbRxS/200w_d.gif)

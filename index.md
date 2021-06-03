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
To kick things off, I needed to get the data stored on my system so I used the command `wget https://open.canada.ca/data/en/dataset/402358f9-2808-44f7-99b3-58f6f5f95b1f --limit-rate=100k` and made sure to specify the download rate should not exceed 100k, because we don't want to overwhelm the Government of Canada servers (they already can't handle much). In this case, the data was already in a single CSV file but had it been in different archives or separated files, WGET would make downloading and archiving these files into a folder incredibly easy.

#### Excel
Next step in my process was to open the csv file in excel and poke around at the data. This is when I noticed that there was an extra column that was in French that simply described the category of the reported crime. I removed this so that other programs like Gephi didn't think there was two sets of headers or categories. 

![CAF](https://github.com/gregelton44/DH-Exploration-Exercise/blob/main/CAF.PNG?raw=true)

Taking a look at the raw data, I noticed right off the bat that the number of calls was trending upward meaning that each year from 2014 to 2019, there has been more reports of crime taking place. If we compare years 2014 to years 2019 we can see that close to 10,000 more calls were reported in 2019. Crimes such as criminal harassment and Extortion seemed to plateau around 2015-2016 and fall back down in recent years. 

Some observations that I have come across when using Excel for data parsing and analyzing especially in the CSV format, is that sometimes the encoding can cause issues with software. For example, if I have french characters like an accented a, the enconding in excel seems to mess up that character. Because of this I was forced to remove the french column. Typically, you wouldn't want to modify the data as it sometimes cannot give you the true picture. 

Next, I made a bar chart to visualize some of the data in order to see a clear picture of what crimes took place the most. 

![ExcelGraph](https://github.com/gregelton44/DH-Exploration-Exercise/blob/main/excelgraph.png?raw=true)

This graph shows what was reported crimes were reported the most in 2014 - 2019. 


#### Voyant Tools
 <figure class="video_container">
  <iframe style='width: 637px; height: 493px;' src='https://voyant-tools.org/tool/Cirrus/?visible=500&corpus=2cdb8c497e46151a825c47d290406638'></iframe>
</figure>

Interstingly taking a look at represenation above, we can see that the terms "Sexual" and "Assault" appear the most in the file. By using something like Voyant tools you can see where the military has the most compliants and what the nature of those compliants are. Ideally, if I was part of the military and saw this I would think "why is sex and assault related crimes the most common?, Do we need to look at our own policies and behaviours in the military to address these issues? and how can we support these victims?". 

Data analysis and science can be so impactful, not just from the numbers but also what kind of social change can happen. 


#### Gephi

I took my CSV that had been cleaned up and put it into Gephi. Now, being honest here I am a bit puzzled on how to read the graph that Gephi produced. 

![Gehpi](https://github.com/gregelton44/DH-Exploration-Exercise/blob/main/gephi.PNG?raw=true) 

You can see that there are arrows pointing at the bottom left hand corner as its area of focus. I am not truly sure what this means however I do believe that it is showing the relationship between the number of calls in relation to the different crimes. This would make sense because in order for there to be a crime reported, you would need to call. 
Gephi is a very powerful tool and I haven't even touched a sliver of its potential but it is one of the technologies that I will continue to look into and get better at. 

#### Gitting Good with GitHub
Honestly, I love github. It has saved me so much headache when trying to develop software especially part of a team project. Its version and revision history single handidly saved me from failing a second year course. But the code aspect of it is just one of the great benefits of GitHub. The most intriguing part of github that I learned in this class are the static pages and the great implementation it has with markdown. You can literally spin up a good looking and simple website in seconds, without the need for HTML, CSS, JS, etc. It makes the whole process a lot more easier especially for documentation. What you are reading right now has been made with a template provided by GitHub and some simple markdown written by me. By using Pages, I can put images or scripts into this repository and link them in this markdown text. (this is where all my pictures and diagrams are stored)

In fact GitHub pages is so helpful, I have used them at my work to document code and features that are being added.

### Going Further
This analysis can be greatly improved and filtered down to see relationships between minute details. For example, with more refinement and graphing we would be able to see the following indicators:

  1. Are there more crimes being commited each year?
  2. What are the nature of these crimes that are increasing? 
  3. Does the military have to address internal issues that these crimes stem from? (Ex. Sexual Misconduct being overlooked, or not providing mental health resources)

These are just a few of them however the deeper you analyze the more specific answers you will find. I really think that using the Gephi tool would definitley be able to show you a more in depth relation between this information. 

If there is more analysis that is done on this we could really gain an better understanding on why crimes take place amongst military personnel. This can also help support mental health services that the military so desperately needs. 

It is important that this data is not manipulated or framed in a way the distorts the significance and impacts of doing this research as the resutls will be heavily skewed.


### Reflection

#### Learning Curve and Difficulties
Overall I think this course tutorials and lab work has relatively smooth. For me, I felt right at home in the weekly work on Git, Wget, terminal/CMD and python as I have used these a lot in the past. What was new to me was more of the analysis tools such as R, Point Map, Voyant, and Gephi to name a few. I found these weren't to tricky to actually work with but I can more difficulty understanding what they were displaying. 

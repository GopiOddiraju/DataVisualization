# HW 4 - CS 625, Fall 2023

Gopi Oddiraju  
Due: October 27, 2023



I've chosen dataset 2 for this Homework. I have manipulated the given data to some extent for convenience. At first, I removed the header and footnotes. I deleted the rows that showed the deaths for the U.S, Puerto Rico, Virgin Islands, Guam, American Samoa, and Northern Marianas. I've created two new columns; '**Deaths due to diseases**' and '**Deaths due to Accidents,Injury,Assault**'. I entered the total number of deaths from all diseases into the newly formed column 'Deaths due to Diseases'. Similarly, I added values from the columns 'Total Accidents', 'Injury by firearms', 'Intentional self-harm', and 'Assault (Homicide)' to the column 'Deaths due to Accidents,Injury by firearms,Assault'. Though the dataset says these are death rates, as mentioned in the notes, these were age-adjusted rates per 100,000 population, we can add them directly. After that, I made a few other minor changes such as formatting the cells. Finally, I saved the file as a CSV format. Both the Original(10s0118.xls) and modified files(10s0118.csv) have been uploaded to this repository. I have read the data from CSV and as data frames using Seaborn. The collab link is provided below.



## Q1:


### Question###: Which states had the highest death rates over all causes in 2006?



<img src="Q1.png" alt="Alt Text" height="800"/>



https://colab.research.google.com/drive/1bjCUKy2nAgOTzdkuqQtH39Iq7PtRrneO#scrollTo=TZBK_qry14H5



Plotting a bar chart between the states and death rates over all causes helps to find out which states had the highest death rates over all causes in 2006. I believe a bar chart is more suitable to answer this question than other options because It is effective for comparing the deaths across different states. each bar represents a state, and the length of the bar corresponds to the deaths allowing for a clear visual comparison. Bar charts are easy and simple to understand. A bar chart based on sorted values would provide more clear insights as well. I've considered a horizontal bar chart in this case to accommodate longer category names and for better readability.




### Idiom: Bar Chart / Mark: Bar
| Data: Attribute | Data: Attribute Type  | Encode: Channel | 
| --- |---| --- |
| Death rate | value, Quantitative | horizontal spatial region (x-axis) |
| State | key, categorical | vertical position on a common scale (y-axis) |


I decided to plot a horizontal bar chart for better readability. I've plotted the bar chart using the data sorted by total death rates over all causes so that we can easily compare among states. Death rates were represented on X-axis and the states were represented using Y-axis. I've decreased the font size for the label on the y-axis to make sure the states' names do not overlap with each other. 


Top 5 fives states with highest death rates in 2006 were Mississippi, Alabama, West Virginia, Louisiana, and Oklahoma. The lowest death rates were observed in states Hawaii, Minnesota, California, New York, and Utah with Hawaii being the lowest.



## Q2:


###Question: Is this ordering different if you compare deaths due to disease vs. deaths due to accident, injury, and assault? In other words, which states are more hazardous to your health vs. which states are the most dangerous?



<img src="Q2.png" alt="Alt Text" width="800"/>


https://colab.research.google.com/drive/1bjCUKy2nAgOTzdkuqQtH39Iq7PtRrneO#scrollTo=TZBK_qry14H5



Plotting a diverging bar chart would be best option answer this question. At first, I considered stacked bar charts and multiple bar charts. However, I prefered a diverging bar chart because it makes comparing the death rates due to both causes easier. A multiple bar chart can compare as well but it will take a lot of space for 50 states and may look congested. Then, I've had a look at subplots where we will have two separate bar charts for each cause. But, I believe we need to plot a single chart to represent this. After considering all factors, I thought a diverging bar chart is the best option, as we can plot both causes on either side of the one axis and we can represent the states on other axis. I've considered a horizontal bar chart in this case to accommodate longer category names and for better readability.




### Idiom: Diverging Bar Chart / Mark: Bar
| Data: Attribute | Data: Attribute Type  | Encode: Channel | 
| --- |---| --- |
| Death rate | value, Quantitative | horizontal spatial region (x-axis) |
| State | key, categorical | vertical position on a common scale (y-axis) |
| Death cause | key, categorical | Hue (differentiating multiple causes) |


I've plotted the diverging bar chart using the data sorted by total death rates due to Accidents,Injury by firearms,Assault as these values were very close to each other in all the states and can be compared easily when sorted. Death rates were represented on the X-axis and States were represented on the Y-axis. Death rates due to Diseases were represented using the purple bars and Death rates due to Accidents,Injury by firearms,Assault were represented using green bars. I've changed the axis labels. To be able to identify the values easily, I've made the value of each bar appear next to the bar. 


To answer the question 2, Yes, The ordering is different when I compared the death rates due to Diseases and Death rates due to Accidents,Injury by firearms,Assault from the ordering when compared the death rates over all causes. Although, Mississippi remains at top when considered all causes and when considered only Diseases. When we consider the death rates due to Accidents,Injury by firearms,Assault, the top 5 states were New Mexico, Mississippi, Louisiana, Wyoming, and Alaska and the states with lowest death rates were New York, Massachusetts, Hawaii, New Jersey, and Connecticut with New York being the lowest. When we consider the death rates due to Diseases, the top 5 states were Mississippi, Alabama, Oklahoma, Kentucky, and Louisiana and the states with lowest death rates were Hawaii, Utah, Minnesota, Colorado, and Arizona with Utah being the lowest.

Even after considering the death rates due to only Diseases instead of all causes, The states Mississippi, Alabama, Oklahoma and Louisiana found to be in top5. It seems these states along with Kentucky are more hazardous to our health. Similarly, when considered death rates due to only Accidents,Injury by firearms,Assault, The states Mississippi, Louisiana were found in top along with New Mexico, Wyoming, and Alaska. These states are more crime prone and dangerous.


## Further questions:


What are the specific factors contributing to higher death rates in states like Mississippi, Alabama, Oklahoma, and Lousiana. Are there any other common factors or a combination of health and safety factors?

Are there regional patterns of states with similar health and safety profiles?

Have there been any public health polocies in states with lower death rates which can be used in other states?

Are the states with higher death rates due to crime lacking enough education and employment opportunities? 



## References:
https://s3.amazonaws.com/assets.datacamp.com/blog_assets/Python_Seaborn_Cheat_Sheet.pdf
https://stackoverflow.com/questions/43214978/how-to-display-custom-values-on-a-bar-plot
https://www.geeksforgeeks.org/how-to-show-values-on-seaborn-barplot/



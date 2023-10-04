# HW 3 - CS 625, Fall 2023

Gopi Oddiraju  
Due: October 04, 2023


## BarChart

### Data
I have taken a simple dataset that shows the population of each continent from 1970 to 2020, from Table 1330 from section 30 Population, Households.
https://www.census.gov/library/publications/2011/compendia/statab/131ed/international-statistics.html

I have manipulated the given data to some extent for convenience. At first, I removed the header and footnotes. I removed the percent distribution data and considered the population from the years 1970 to 2020 only. After that, I made a few other minor changes such as renaming columns and formatting the cells. Finally, I saved the file as a CSV format. Both the Original(12s13330.xls) and modified files(12s1330.csv) have been uploaded to this repository.


### Visualization Idiom
Idiom: Bar Chart / Mark: Bar
| Data: Attribute | Data: Attribute Type  | Encode: Channel | 
| --- |---| --- |
| Year | key, categorical | horizontal position on a common scale (x-axis) |
| Continent | key, categorical | Hue (differentiating multiple positions) |
| Population | value, quantitative | vertical position on a common scale (y-axis) |


![alt text](barchart.png)

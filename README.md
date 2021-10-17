# Kickstarting with Excel

## Overview of Project 
The purpose of this project is to continue helping Louise draw conclusions from past kickstarter campaigns so that she can make informed decisions. She is particularly interested in understanding the success of the campaigns in relation to their launch dates and funding goals. 

## Analysis and Challenges
I conducted the analysis following the steps outlined in the module and challenge instructions. The initial steps were focused on adding conditional formatting and clear cell text formats (such as for the dates) to allow me to more easily understand and look at the data. Here is a list of example functions that I used to set up the sheet: 
- `=IFERROR()`
- `=(((J2/60)/60)/24)+DATE(1970, 1, 1)`
- `=YEAR()`
- Conditional Formatting: Graded Color Scale 
### Deliverable 1 - Analysis of Outcomes Based on Launch Date 
The goal of this deliverable was to visually show data patters for theater outcomes by launch date. To do this, I practiced creating and using pivot tables to create a line graph. I wanted to show how many campaigns were successful, cancelled, and failed by month of the year. I made sure to apply filters for 'Parent Category = theater' and 'Years = all'. The final pivot table can be seen below: 
![Pivot Table](https://github.com/andreabassetti/kickstarter-analysis/blob/main/png/Pivot%20Table.png)

I then followed simple steps to insert a line graph based on the pivot table. The final line graph can be seen below: 
![Theater_Outcomes_vs_Launch](https://github.com/andreabassetti/kickstarter-analysis/blob/main/png/Theater_Outcomes_vs_Launch.png)
### Deliverable 2 - Analysis of Outcomes Based on Goals
The goal of this deliverable was to visually show data patters for outcomes for plays based on goals. Instead of creating a pivot table with existing data, I created my own table and inserted functions to find the relevant information. I only used the `=COUNTIFS()`, `=ROUND()`, and division. The final table can be seen below:
![Table 2](https://github.com/andreabassetti/kickstarter-analysis/blob/main/png/Table%202.png)

I then followed simple steps to insert a line graph based on the table. The final graph can be seen below: 
![Outcomes_vs_Goals](https://github.com/andreabassetti/kickstarter-analysis/blob/main/png/Outcomes_vs_Goals.png)

### Challenges
There were two main areas where I encountered issues. The first was pivot tables and the second one was asking the `=COUNTIFS()` function to count between a certain range. Regarding the pivot table, my main challenge was around understanding which column title should go in which box to create the pivot table. Since this is my first encounter with pivot tables, I believe this is just a question of practice to become more familiar with how they work. Regarding the ranges in the `=COUNTIFS()` I was attempting to edit the criteria incorrectly. I was originally attempting to define the criteria by writing it like this: `1000>Kickstarters!D:D>=4999` as if it were a range. I noticed this did not work in the question, and instead I wrote two different conditions under which it had to count and it looked like this: `Kickstarters!D:D,">=1000",Kickstarters!D:D,"<4999"`.

## Results

- **What are two conclusions you can draw about the Theater Outcomes by Launch Date?**
I can conclude that May was the month with the most successful number of campaigns. Not only by count but also by percentage since it is one of the two only months that had a success rate higher than 50% (the other month being June). I can also conclude that May, June, July, August and October all have a similar amount of failed campaigns. We also know that there were less total campaigns as the months go by, so we can conclude that from May to October (September being an exception) by the rate of successful campaigns in proportion to total campigns decreases. 

- **What can you conclude about the Outcomes based on Goals?**
I can conclude that kickstarter campaigns for plays are more than 50% successful if the goal falls between these five brackets: less than 1000, 1000 to 4999, 5000 to 9999, 35000 to 39999, and 40000 to 44999. 
I can also conclude that all the kickstarter campaigns for plays that have a goal between 45000 and 49999 have a 100% failure rate. 

- **What are some limitations of this dataset?**
The data in the Kickstarter sheet only has complete information on kickstarter campaigns in the theater category from 2014-2016.Looking at these three years individually, the data and therefore line graphs, look drastically different. I believe a limitation of this data is that we do not have enough historical data. Additionally, the arts industry has been hit very hard by COVID-19. The ability to have performances is going to impact the likelyhood of campaigns meeting their goals. This impact may be either positive or negative. We do not have recent data that would help Louise make a more informed decisions on how todays events may skew the patters we see in the data. 

- **What are some other possible tables and/or graphs that we could create?**
I would create two more tables and graphs to help Louise have a full picture of kickstarter campaigns in the past. The first graph I would like to create would represent the length of the campaign vs the outcome. I believe the analysis of this graph could give some important insights into how to structure her campaign. I would also like to create a table to identify the number of backers per campaign, the average donation, and if there are any outliers in each campaign. This may help eliminate any campaign that reached its goal because of individual backers, if Louise does not have pre committed backers these data points should be looked at with a different lens.

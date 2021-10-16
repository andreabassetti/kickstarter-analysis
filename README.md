# Kickstarting with Excel

## Overview of Project 
The purpose of this project is to continue helping Louise draw conclusions from past kickstarter campaigns so that she can make infromed decisions. She is particularly interested in understanding the success of the campaigns in relation to their launch dates and funding goals. 

## Analysis and Challanges
I conducted the analysis following the steps outlined in the module and challange instructions. The initial steps were focused on adding conditional formatting and clear cell text formats (such as for the dates) to allow me to more easily understand and look at the data. Here is a list of example functions that I used to set up the sheet: 
- `=IFERROR()`
- `=(((J2/60)/60)/24)+DATE(1970, 1, 1)`
- `=YEAR()`
- Conditional Formatting: Graded Color Scale 
### Deliverable 1 - Analysis of Outcomes Based on Launch Date 
The goal of this deliverable was to visually show data patters for theater outcomes by launch date. To do this, I practiced creating and using pivot tables to create a line graph. I wanted to show how many campaigns were successful, cancelled, and failed by month of the year. I made sure to apply filters for 'Parent Category = theater' and 'Years = all'. The final pivot table can be seen below: 
![Pivot Table](https://github.com/andreabassetti/kickstarter-analysis/blob/main/png/Pivot%20Table.png)
I then followed simple stemps to insert a line graph based on the pivot table. The final line graph can be seen below: 
![Theater_Outcomes_vs_Launch](https://github.com/andreabassetti/kickstarter-analysis/blob/main/png/Theater_Outcomes_vs_Launch.png)
### Deliverable 2 - Analysis of Outcomes Based on Goals
The goal of this deliverable was to visually show data patters for outcomes for plays based on goals. Instead of creating a pivot table with existing data, i created my own table and inserted functions to find the relevant information. I only used the `=COUNTIFS()`, `=ROUND()`, and division. The final table can be seen below:
![Table 2](https://github.com/andreabassetti/kickstarter-analysis/blob/main/png/Table%202.png)
I then followed simple steps to insert a line graph based on the table. The final graph can be seen below: 
![Outcomes_vs_Goals](https://github.com/andreabassetti/kickstarter-analysis/blob/main/png/Outcomes_vs_Goals.png)

### Challenges
There were two main areas where I encountered issues. The first was pivot tables and the second one was asking the `=COUNTIFS()` function to count between a certain range. Regarding the pivot table, my main challange was around understanding which column title should go in which box to create the pivot table. Since this is my first encounter with pivot tables, I believe this is just a question of practice to become more familiar with how they work. Regarding the ranges in the `=COUNTIFS()` i was attempting to edit the criteria incorrectly.I was originally attempting to define the criteria by writing it like this: `1000>Kickstarters!D:D>=4999` as if it were a range. I noticed this did not work in the question, and instead i wrote two different conditions under which it had to count and it looked like this: `Kickstarters!D:D,">=1000",Kickstarters!D:D,"<4999"`.

## Results

- What are two conclusions you can draw about the Theater Outcomes by Launch Date?
May was the month with the most successful campaigns
May june july august and october all have a similar amount of failed campaigns 

- What can you conclude about the Outcomes based on Goals?
I can conclude that kickstarter campaigns for plays are more than 50% successful if the goal falls between these four brackets: less than 1000, 1000 to 4999, 35000 to 39999, and 40000 to 44999. 
I can also conclude that all the kickstarter campaigns for plays that have a goal between 45000 and 49999 have a 100% failure rate. 
I can conclude that kickstarter campaigns for plays are more than 50% failed if the goal falls between these four brackets: 25000 to 29999, 30000 to 34999, 45000 to 49999, and greater than 50000. 

- What are some limitations of this dataset?
Theter outcomes based on launch date only has complete information for 3 years, if you look at the three years separately the graphs look drastcially differet. i would want to see data for more years before making any decisions on my plans. Also, data from prcovid can be tricky because we do not know how the pandemic can change these numbers. i think this is particularly relevant because theater is an industry that has been hit very hard during covid due to the nature of the indoor preformances. you could look at how other similar industries did since there is data on similar ones. 

- What are some other possible tables and/or graphs that we could create?
The length of the campaign 
number of backers 

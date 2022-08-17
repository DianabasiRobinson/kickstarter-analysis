# AN ANALYSIS OF KICKSTARTER CAMPAIGNS
## **PROJECT OVERVIEW AND PURPOSE**
This project aims at Performing an analysis of Kickstarter data to uncover trends in a theater-based crowdfunding campaign.

Louise, who is the primary requester wants to start a crowdfunding campaign to finance her play “Fever” with an estimated budget of over $10,000. She is keen to understand the outcomes of the launch dates and funding goals from previous theater-based campaigns.

The source data was an excel file of a theater-based Kickstarter campaign with a table of 4114 campaigns between 2010 and 2017 which was spread across 4115 rows and 13 columns (A – M) after data mining. The tools used are pivot tables, breakout tables of subsets of data, charts of various criteria, and other statistical functions. 

In other to reveal the trends and provide useful insights about their launch dates and funding goals, we have to analyze and visualize the two outcomes so as to influence Louise’s campaign plan by determining factors that will impact the campaign positively.
## **ANALYSIS AND CHALLENGES**
### Analysis of Outcomes Based on Launch Date
1. From the Line Chart, the three lines (Green, Red, and Yellow) denote Successfully, Failed, and Canceled outcomes for the theater-based campaign based on their launch date. 
2. It can be fairly seen that there is an increase in outcomes in May and June for successful campaigns.
There is a continuous fall in the outcome of successful campaigns from November, December, and January.
### Analysis of Plays Outcomes Based on Goals
1. We can deduct from the chart that the percentage of successful campaigns is 76% when the goal is <$1000, and 73% when the goal falls between $1000 and $5000.
2. The chart also shows that campaigns whose goals fall under $20,000 have a promising chance of success, compare to campaigns with goals of over $20,000 that were likely to fail. Thus, with higher goals, the percentage of success is lower, and the percentage of failure is increased. 
3. 	From our worksheet, the total number of successful campaigns is at maximum (388) when the goals are <$5000. 
4. 	Moving further, we can notice a small increase for campaign goals between $35,000 to $45,000, but then, that has 6 successful campaigns and a total of 9 campaigns which skews up its percentage.
### Challenges and Difficulties Encountered
The table of Outcome Based on Goals was populated using the **COUNTIFS()** function for the Number Successful, Number Failed, and Number Cancelled columns. On my first attempt, I got a false value because I filtered the subcategory to have only the plays on the Kickstarter table with the following **COUNTIFS()** 
code `= COUNTIFS(Kickstarter!D:D,">=50000",Kickstarter!F:F,"Successful")`. I ignored the criteria for the plays in the formula which gave me a number of the successful outcome of 322 for a goal of <1000.

I troubleshot to understand the right criteria which required adding the plays as criteria In the COUNTIFS()  formula;`=COUNTIFS(kickstarter!D:D,"<1000",kickstarter!F:F,"Successful",kickstarter!R:R,"Plays")`, and that populated the correct values for the columns on the Outcome based on Goals table. 

## **RESULTS**

### Conclusions about the Theatre Outcomes by Launch Date
The following conclusions are drawn from the Outcome Based on the Launch Date.
1.	Campaign launch in May and June tends to have more success rate.  This trend is in concurrence with the summer break when schools are closed.
2.	Campaign launch in November, December, and January are less successful.

### Conclusion about the Outcomes based on Goals
Most successful campaigns have goals of less than $5000. Considering Louise’s goal of $10,000 which is twice our findings for the most successful goals. Louise should review her goal to have a successful play campaign.

### Limitations of the dataset
1.	Lack of data for the backers for successful theater-Based campaigns which would give Louise an idea of the target population. 
2.	The data set for this analysis was limited to a few years, and a few campaign categories and subcategories, thus, some of the results are not statistically relevant given the small sample size. Sufficient data coverage would give more detailed and reliable results than the already used data.

 ### Recommended tables and/or graphs
It will be pertinent to create a new table for the Successful, Fail and Cancel columns using statistical calculations for the Analysis of Outcome Based on Goals to help us determine the spread of the data. Also,table for country and goals Outcome will be a useful tool to show goals outcome for all countries.
The following chart can be considered useful in this analysis.
Bar chart: for Analysis of Outcomes based on Goals.
Dot-plot chart or Map Chart: to show the differences in the project’s success across countries.
Bar plot: to show how the duration of the project influences the project’s success.
Box and Whisker chart: to show the outliers



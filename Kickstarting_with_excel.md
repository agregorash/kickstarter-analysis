# Kickstarting with Excel

## Performing analysis on Kickstarter data to uncover trends

### Purpose

Prior to launching a fundraising campaign for her play *Fever*, our client Louise asked us to analyze a dataset of Kickstarter campaigns in order to determine the key variables forlaunching a fundraising campaign.  Now that she has launched her campaign she would like to know how similar campaigns performed with these key factors in mind.  Through our initial analysis of the compiled data we concluded that launch date and funding goals are two critical variables that determine whether a fundraising campaign will be successful or not.  In order to help analyze trends we vizualized the data with charts from our pivot table of campaign outcomes based on launch date, and statistical analysis of campaign outcomes based on the fundraising goal amount. 

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

In order to see whether any trends existed for the outcome of Kickstarter campaigns based on the launch date, we set out to organize this data in a pivot table and visualize it through a line chart.  

(https://github.com/agregorash/kickstarter-analysis/blob/master/Resources/Theater_Outcomes_vs_Launch.png.png)

The three outcomes analyzed were successful, failed, and canceled. Live campaigns were later filtered out of the outcomes column.  Parent category and years were used as the two filters in our pivot chart so the data could be filtered to show specifically theater campaigns.  Next we used outcomes as the column value and date created as our row value, and then grouped the row labels to show the month of the year, so that we could quickly see the amount of successful, failed, and canceled campaigns based on the month of the year they were launch.  The outcomes column was then filtered in descending order to further clean the data and show successful campaigns first, then failed, and then canceled respectively.  A line chart with dots is used to show the number of outcomes on the y-axis, based on the month the campaign was launched on the x-axis.

### Challenges and Difficulties Encountered

The first deliverable was completed with little to no challenges.  A potential challenge that could've been encountered in grouping the "Row Labels" column to show months of the year, however my Excel program automatically grouped the data. 

### Analysis of Outcomes Based on Goals

The second analysis performed was to explore whether outcomes were effected by the goal of the fundraising campaign.  The data was organized in an 8x12 sheet with Goal, Number Successufl, Number Failed, Number Canceled, Total Projects, Percentage Successful, Percentage Failed, and Percentage canceled across the top header, and funding goals in $5000 increments starting with less than $1000 and finishing with greater than $50,000.

(https://github.com/agregorash/kickstarter-analysis/blob/master/Resources/Outcomes_vs_Goals.png)

The first three columns were calculated using the COUNTIFS function, with the outcomes, goal, and subcategory play as a consistent filter.  The outcomes and goal criteria were changed based on the outcome result in the column and the goal result in the row.  The sum of all campaigns in each funding increment was calculated in the Total Projects column by adding the three outcome values.  Percentages of each outcome were then calculated by dividing the Successful, Failed, and Canceled campaigns by the Total Projects value and formatting the values as percentages.  The data in the final three columns was then vizualized with a line chart, with percentage on the y-axis and the goal amount on the x-axis.  

### Challenges and Difficulties Encountered

A couple difficulties were experienced in the second deliverable.  First, I had a little trouble figuring out how to establish a range in the COUNTIFS function but realized that I just needed to add another criteria range.  The other difficulty I experienced was creating the line chart from the data. I left out the fuding amount value originally, so the chart looked correct, but there were no values on the x- axis.  After messing around with the line chart filters I realized I had to use the full data set and then filter out the 'Number of' columns so that it was showing only the percentage values on the y-axis.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

First, we can conclude that the launch date does indeeed have an effect on the outcome of successful Theater Kickstarter campaigns.  May and June are the two ideal months to launch a fundraising campaign in the Theater field.  We can also conclude that the launch date does not have much effect on the amount of failed campaigns.  There does not seem to be much variation in the amount of failed campaigns throughout the year, especially with consideration of the total amount of campaigns that were launched in each given month.

- What can you conclude about the Outcomes based on Goals?

We can conclude that campaigns with fundraising goals of less than $5000 are the most successful.  As the fundraising goal increases the percentage of successful campaigns seems to trend downward, with a couple exceptions.

- What are some limitations of this dataset?

The most prevalent limiting factor of this dataset is the lack of a significant sample size of campaigns with fundraising goals over $25,000.  This causes some irregularity in the general downward trend of successful campaigns exceeding a goal of $5000, which is evident in the two ranges of $35,000 to $39,999 and $40,000 to $44,999.

- What are some other possible tables and/or graphs that we could create?

Using the data we already have in Outcomes Based on Launch Date sheet, we could calculate the percentage of outcomes based on launch date so that we could further analyze the trends.  We could also create a pivot table to analyze the outcomes based on the parent category or subcategory of the fundraising campaign, in order to see whether different campaign types are more successful than others.

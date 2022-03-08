# Kickstarting with Excel

## Overview of Project
This project is to showcase how Louise who is very passionate towards plays can achieve her goal of fundraising successfully. The main objective is to give her an idea on how different theatre campaigns are fared with respect to their launch dates and funding goals considering all the outcomes(successful/fail/canceled) which will help Louise to decide.



### Purpose
To Visualize the campaign outcomes based on their launch dates and their funding goals

## Analysis and Challenges
Project consists of two technical analyses.
1. Outcomes Based on Launch Date
2. Outcomes Based on Goals 



### Analysis of Outcomes Based on Launch Date
1. In "Kickstarter_Challenge.xlsx",the launched date which is in the UNIX timestamp format is first converted into desire date format. <br><br> ![unix To Date Conversion](https://github.com/ashwinihegde28/dataAnayticsBootcampExcelProject/blob/main/resources/unixToDate.PNG) <br><br> 
2. "Years" column is created using the "=YEAR()" .<br><br> ![YEAR FUNCTION](https://github.com/ashwinihegde28/dataAnayticsBootcampExcelProject/blob/main/resources/functionYEAR.PNG) <br><br>
3. Pivot table is created from the “KickStarter” worksheet and placed in a new sheet "Theater Outcomes by Launch Date". Pivot table is based on Date Created (launched date) and outcomes.
   - Table "Parent Category" will be filtered on theatre data only and "Years" should be grouped into months to show different outcomes. Like the image below
    <br><br> ![groupYearsToMonths](https://github.com/ashwinihegde28/dataAnayticsBootcampExcelProject/blob/main/resources/groupYearsToMonths.PNG) <br><br>
   - Outcomes will be filtered only on successful, failed and canceled but not on live. Also campaign outcomes will be in descending order so that "successful" is listed at the top.
   - Finally represent the pivot table data in the form of line chart as below.  ![Theater_Outcomes_vs_Launch](https://github.com/ashwinihegde28/dataAnayticsBootcampExcelProject/blob/main/resources/Theater_Outcomes_vs_Launch.png) <br> Theater Outcomes vs Launch



### Analysis of Outcomes Based on Goals
1. Create a new sheet by the name “Outcomes Based on Goals". 
2. The goal amount are specified in different range starting - less than 1000 to greater than 50000 in "Goal" Column. The different outcomes successful, fail and canceled are populated and placed in "Number Successful," "Number Failed," and "Number Canceled" columns respectively using the "COUNTIFS()" function with the Subcategory chosen as "plays" as the criteria. <br><br> ![Number of Successful](https://github.com/ashwinihegde28/dataAnayticsBootcampExcelProject/blob/main/resources/goalsForSuccessful1.PNG)<br>Number of Successful<br><br>  <br><br> ![Number of Failed](https://github.com/ashwinihegde28/dataAnayticsBootcampExcelProject/blob/main/resources/goalsForFailed.PNG)<br>Number of Failed <br><br> <br><br> ![Number of Canceled](https://github.com/ashwinihegde28/dataAnayticsBootcampExcelProject/blob/main/resources/goalsForCancelled.PNG)<br>Number of Canceled<br><br>
3. "SUM" function is used to the "Total Projects" column with the number of successful, failed, and canceled projects for each row. <br><br> ![Calculation Of Total Projects](https://github.com/ashwinihegde28/dataAnayticsBootcampExcelProject/blob/main/resources/totalProjectsCalculation.PNG)<br>Total Projects<br><br>
4. The percentage of successful, failed, and canceled projects for each row will be mentioned in the columns “Percentage Successful”, “Percentage Failed” and “Percentage Canceled” respectively.<br><br> ![Percentage Successful](https://github.com/ashwinihegde28/dataAnayticsBootcampExcelProject/blob/main/resources/percentageSuccess1.PNG)<br>Percentage Successful<br><br>  <br><br> ![Percentage Failed](https://github.com/ashwinihegde28/dataAnayticsBootcampExcelProject/blob/main/resources/percentageFailed1.PNG)<br>Percentage Failed<br><br>  <br><br> ![Percentage Canceled](https://github.com/ashwinihegde28/dataAnayticsBootcampExcelProject/blob/main/resources/percentageCancelled1.PNG)<br>Percentage Canceled<br><br>
5. Final phase is to visualize the outcomes in the form of a line graph using the goals and the percentage of different outcomes in "Outcomes_vs_Goals.png" like the images below ![Outcomes_vs_Goals](https://github.com/ashwinihegde28/dataAnayticsBootcampExcelProject/blob/main/resources/Outcomes_vs_Goals.png) <br> Outcomes vs Goals



### Challenges and Difficulties Encountered
   1. Module challenge had minor details to be considered especially filters which is achieved after reading the challenge few times and understanding. 
   2. The "Kickstarter_Challenge.xlsx" sheet consists of huge data set and needed few basic operations like formatting and conversions for few columns.
   3. The second part of the challenge was to use the “COUNTIF” function, this took little a while to understand, and the hint provided really helped a lot to implement.
   4. Manually writing the formula for different columns/rows was time consuming. Making static row and column using “$” sign made calculation easier.




## Results

- Outcomes based on Launch Date
   - Campaign launched in the months of MAY and June displays higher chances of success which is the good period to consider.
   - Campaign launched in December and January have very low success rates and even there are higher possibilities of cancellation. Hence this period must be avoided.

- Outcomes based on Goals
   - The theatre plays are successful when goal amount is less than 5000.
   - Plays above 14,999 are dipping down but has picked up between 35,000 - 45,000.
   - Theatre campaign in the range between 45,000 to 45,999 have all failed.

- Limitations of this data set
   - The data set provided is huge and contains many raw data and few column are never used in the campaign.
   - The data looks older or not updated.
   - There is no inclusion for which country the campaign is for this challenge.
   - The goal amount is in different currencies.


- Possible tables and/or graphs that could be created
   
   - The analysis of outcomes for different subcategories based on launch date and goal. Similar to theater as subcategory with line graph.
   - Number of US/any country Kickstarter campaigns that were pledged US dollar/corresponding country currency amount in different ranges shown in Pledged column for desired subcategory and visualizing it in a line graph.
   - The combination of plays hosted for the year range and spotlighted, represented by bar graph.
   - For particular play calculating average donation, duration and backers in a table and visualizing in bar graph. 
      






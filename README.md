# Kickstarting with Excel

## Overview of Project
This project analyzes 4,115 Kickstarter campaigns from 2009 to 2014 to show the relationship of a campaign's success with their funding goals and launch dates. The data includes the name of the campaign, it's description, origin location, funding goals and pledges, number of pledges, category and subcategory, launch and end dates, and overall outcome.  

### Purpose
The client is looking at the viability of Kickstarter to raise funds to stage a play. The purpose of this project is to analyze Kickstarter campaigns in the "theater" category and "plays" subcategory to provide funding goal and launch date recommendations to the client.  

## Analysis and Challenges
Our analysis focuses on two key metrics for successful campaigns; the campaigns launch timing and the overall fundraising goal.

First, a the category/subcategory column was separated using a built in excel feature. Then a filter for the parent category "theater" isolates campaigns similar to the client's proposal. According to the chart below, US-based campaigns in the "theater" category have a 58% success rate on their funding goals.
***Insert Parent category bar chart here

The analysis continues to show the if there are commonalities for "successful" funding camapaigns.

### Analysis of Outcomes Based on Launch Date
Using a pivot chart of launch date and outcome data separated by month, a time-series chart shows there is a seasonality to successful campaigns.

***Insert outcomes by launch date chart here

The chart shows the most successful theater campaigns launched in May and June during for campaigns in 2009-2014. Additionally, there is seemingly no correlation with timing for failed or canceled campaigns, implying that launch date timing alone is not responsible for campaign's failure.

### Analysis of Outcomes Based on Goals
The second part of the anaylsis focuses on the overall funding goal's effect on it's success. Using a COUNTIFS statement, buckets of funding goals for "plays" campaigns were created and separated by success, failure, and canceled. Out of the 1,047 campaigns in the analysis, none were canceled. The isolation of the successful and failed campaigns relative to their funding goals is shown below.

***Insert goals based chart here

The chart above shows campaigns with funding goals under $5,000 are typically more successful than those with higher goals. Additionally, it shows that as campaign goals are set higher than $5,000 they progressively become less successful. The data points for funding goals higher than $20,000 are limited.

### Challenges and Difficulties Encountered
One challenge impacting the analysis is the conversion of the launch and deadline dates from Unix timestamps to a readable date format so launch date data could be understood more easily. The solution was using the UNIX date conversion. The biggest analysis challenge is identifying and isolating campaigns similar to the client's propsal to analyze more relevant data points. This was solved by separating the category and subcategory into distinct columns and filtering for the "theater" category and the "plays" subcategory.

## Results
The results of the "Outcomes based on Launch Date" chart show the best month for launching the client's "theater" campaign would be May. The months to avoid would be the first and last 3 months of the year. Timing for desirable campaigns can be more succesful in May through July, however, campaign timing does not correlate with success as there is no correlation with timing with respect to failed campaigns.

The results of the "Outcomes based on Goals" chart show the budget for the client's project should remain under a $5,000 fundraising goal. Requests for a funding above that amount are less likely to succeed. Success at higher funding levels cannot be directly attributed to the funding goals as the chances of success are more related to other features of the campaign. The market may not exist at these larger funding goal amounts, hence the lack of data.

Funding goals above for plays above $15,000 is sparse, so we would need more data to correctly evaluate the efficacy of setting a funding goal higher than that amount. Our cata set is limited to the Kickstarter platform from 2009-2014. For a more accurate conclusion we would want to pull data from other competing platforms to discover differences in success or failure based on platforms. One specific platform might have users more aligned to the client's need. Additionally the timeframe on the data is outdated and should be updated to include more a more contemporary timeframe. The data is also limited in it's granularity when it comes to location. Shows take place in a specific location, therefore having data to more granularly target the client's expected debut location would be more relevant than what is in the current dataset. The data is also limited to the overall pledged amount and the number of pledges allowing us to find the mean of the pledges, however, it would be useful to look at individual donation data.

To further our analysis we should look at the length of the successful campaigns to find if there is a correlation with the campaign duration and success. To find out where the client would have the most success, it may be useful to show a hot spot map of donors for plays based on their location to understand where donors will be the most engaged. Because launch date and goals have shown no direct correlation to success, we may want to look into the content of the "blurbs" to see if there are any thematic or lexical similarities among the successful campaign descriptions.

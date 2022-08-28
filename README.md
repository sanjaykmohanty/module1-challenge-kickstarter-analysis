# Kickstarting with Excel

## Overview of Project

### Purpose
Louise wants to start a crowdfunding campaign to fund her play, *Fever*. She has estimated a budget of over $10,000 for this initiative. The purpose of this project is to analyze the data in the Kickstarter file to understand campaigns from start to finish and create an analysis report that would help Louise to set up her crowdfunding campaign to success. 

Excel is used for the data analysis in this project.   

## Analysis and Challenges
### Study the Data
The data in the Kickstarter file has the following fundraiser attributes:
- id	
- name	
- blurb	 
- goal 	
- pledged	
- outcomes	
- country	
- currency	
- deadline	
- launched_at	
- staff_pick	
- backers_count	
- spotlight	
- Category and Subcategory

In total, there are 4145 records in the Kickstarter file. Columns containing dates are not in a readable format which are converted to make them readable. Information in the Kickstarter file was broken down for analysis as mentioned below:
- The Goal column stores how much money each campaign will need to succeed
- The Pledged column stores how much each campaign actually made
- The Outcomes column stores if the campaign met its goal
- The Country column stores the country in which the campaign was started

### Analyze Funding Goal
Louise has estimated that her play will cost $12,000. Data from pledged column was used to research projects with similar monetary goal. Many of the campaigns missed their goal amount by a small margin. The deficit was calculated, and the information was stored in "Percentage Funded" column. Information in "Percentage Funded" column was reviewed to determine how close a campaign came to reaching or exceeding its funding goal.

To determine how much money people have pledged to campaign historically, the average donation by the backers was calculated and the information was stored in "Average Donation" column.

### Break Down of Data
Louise is interested in starting a campaign for theater. Category/Subcategory column was used to break down the data to keep only "theater" category and exclude all other categories. Data was broken down further to include only "Plays" subcategory and exclude all other subcategories under "theater" category. Search functionality was used to pinpoint the projects that are similar in scope and type as Louise's project.

### Outcome Based on Launch Date
Data was organized to check the outcomes of the campaigns based on launch date. 

![Pivot_Outcomes_vs_Launch](https://user-images.githubusercontent.com/31812730/187046370-43f60e6b-bfed-4374-939e-db0f51593b8b.png)

A line chart titled "Theater Outcomes Based on Launch Date" was created as shown below to visualize the relationship between outcomes and launch month.

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/31812730/187045819-91cd5a24-84fd-4a63-bbb3-91bb621673bb.png)

### Outcome Based on Funding Goal
Based on the funding goal and actual amount pledged information, projects are categorized under outcomes as successful or failed. In few cases the projects were cancelled as well. In order to visualize the percentage of successful, failed, or cancelled plays based on funding goal amount, the data was organized as shown below.

![Pivot_Outcomes_vs_Goals](https://user-images.githubusercontent.com/31812730/187046950-018d87e4-1287-415b-85da-a0b0d65015a3.png)

A line chart titled "Outcomes Based on Goal" was created to visualize the relationship between the goal-amount ranges and the percentage of successful, failed, or canceled projects.

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/31812730/187051017-94cc8e28-9549-4708-9982-2a52143c65a2.png)

### Challenges

While calculating the average donation, it was observed that not every campaign has backers. Average donation calculation was failing for those projects. A conditional error handling technique was used, and average donation was set to zero for the campaigns with no bakers.  

    =IFERROR(ROUND(E671/L671,2),0)

Initially, organizing data based on funding goal was a bit tedious as the formula used to retrieve data required different values in each cell for the conditional data retrieval. 

    =COUNTIFS(Kickstarter!F:F,"=successful",Kickstarter!D:D,">=0",Kickstarter!D:D,"<1000",Kickstarter!R:R,"=plays")

However, using the absolute cell reference technique eased the pain to a great extent.  

    =COUNTIFS(Kickstarter!F:F,"="&$K$3,Kickstarter!D:D,">="&M3,Kickstarter!D:D,"<"&N3,Kickstarter!R:R,"="&$L$3)

## Results
### Conclusion - Theater Outcomes Based on Launch Date 
May, June, and July months are the best time of the year to launch a theater campaign. The "Teater Outcomes Based on Launch Date" chart clearly highlights the campaigns launched during these months are more successful.

December is not a good month to launch a theater campaign. The "Theater Outcomes Based on Launch Date" chart clearly calls out that there is only a 50% chance that the outcome of the theater campaign will be successful if the theater campaign is launched in December.

### Conclusion - Theater Outcomes Based on Funding Goal
Theater campaigns with a funding goal below $10,000 have the higher success rate at more than 70% successful. 

### Limitations
The smaller volume of data available in the dataset may not provide enough insight, larger volume of data is beneficial to get more insight.

Although the dataset contains historical data, current data which is a critical element for data analysis is missing in the dataset. 

### Recommendations
There are several attributes in the dataset can be considered to extend the analysis further. For example, data can be organized to check in which country the theater campaign was more successful based on backer count and pledge amount.

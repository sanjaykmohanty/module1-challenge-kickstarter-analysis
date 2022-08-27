# Kickstarting with Excel

## Overview of Project
### Louise wants to start a crowdfunding campaign to fund her play, *Fever*. She has estimated a budget of over $10,000 for this initiative.
### The purpose of this project is to anlyze the current site data to understand campaigns from start to finish and create an anlysis report that would help Louise to set up her crowdfunding campain to success. 
### Excel is used extensively as the tool for data the anlysis in this project.   

## Analysis and Challenges
### The data in the Kickstarter file has the following fundraiser attributes:
- ### id	
- ### name	
- ### blurb	 
- ### goal 	
- ### pledged	
- ### outcomes	
- ### country	
- ### currency	
- ### deadline	
- ### launched_at	
- ### staff_pick	
- ### backers_count	
- ### spotlight	
- ### Category and Subcategory
### In total, there are 4145 records in the Kickstrter file. Columns containing dates are not in readable format which were converted to make them readable. Information  in the Starter file was broken down for analysis as mentioned below:
- ### The Goal column tells us how much money each campaign will need to succeed
- ### The Pledged column tells us how much each campaign actually made
- ### The Outcomes column tells us if the campaign met its goal
- ### The Country column lists the country in which the campaign was started
### Louise has estimated that her play will cost $12,000. Data from pledged column was used to research frojects with similatr monitary goal. Many of the campaigns missed their goal amount by a small margin. The deficit was calculated and the information was stored in "Percentage Funded" column. Information in the "Percentage Funded" column was reviewed to determine how close a campaign came to reaching or exceeding it's funding goal.
### To determine how much money people have pledged to campaign historically, the average donation by the backers was calculated and the information was stored in "Average Donation" column. While calculating the average donation, it was observed that not every campaign has backers.   
### Louise is interested in starting a campaign for theater. Category/Subcategory column was used to break down the data to keep only theater category and exclude all other categories. 

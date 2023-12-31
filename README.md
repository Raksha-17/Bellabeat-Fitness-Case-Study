# Bellabeat-Fitness-Case-Study
Analyze smart device usage data in order to gain insight into how consumers use the non-Bellabeat smart devices which would subsequently, help influence Bellabeat marketing strategy.
Course: [Google Data Analytics Capstone: Complete a Case Study](https://www.coursera.org/learn/google-data-analytics-capstone)
## Introduction
In this case study, I will be working in the capacity of a junior data analyst to identify key business tasks following the six(6) data analysis procedures namely : Ask, Prepare, Process, Analyze, Share, Act. In order to answer the key business questions, I will follow the steps of the data analysis process: __[Ask](https://github.com/Raksha-17/Bellabeat-Fitness-Case-Study/blob/main/README.md#ask), [Prepare](https://github.com/Raksha-17/Bellabeat-Fitness-Case-Study/blob/main/README.md#prepare), [Process](https://github.com/Raksha-17/Bellabeat-Fitness-Case-Study/blob/main/README.md#process), [Analyze](https://github.com/Raksha-17/Bellabeat-Fitness-Case-Study/blob/main/README.md#analyze), [Share](https://github.com/Raksha-17/Bellabeat-Fitness-Case-Study/blob/main/README.md#share), and [Act](https://github.com/Raksha-17/Bellabeat-Fitness-Case-Study/blob/main/README.md#act)__.

## Background
### BellaBeat Fitness 

Urška Sršen and Sando Mur founded Bellabeat, a high-tech company that manufactures health-focused smart products. Sršen used her background as an artist to develop beautifully designed technology that informs and inspires women around the world. Collecting data on activity, sleep, stress, and reproductive health has allowed Bellabeat to empower women with knowledge about their own health and habits. Since it was founded in 2013, Bellabeat has grown rapidly and quickly positioned itself as a tech-driven wellness company for women. 
The five(5) products produced by Bellabeat are :

**Bellabeat app:** The Bellabeat app provides users with health data related to their activity, sleep, stress, menstrual cycle, and mindfulness habits. This data can help users better understand their current habits and make healthy decisions. The Bellabeat app connects to their line of smart wellness products.

**Leaf**: Bellabeat’s classic wellness tracker can be worn as a bracelet, necklace, or clip. The Leaf tracker connects to the Bellabeat app to track activity, sleep, and stress.

**Time**: This wellness watch combines the timeless look of a classic timepiece with smart technology to track user activity, sleep, and stress. The Time watch connects to the Bellabeat app to provide you with insights into your daily wellness.

**Spring**: This is a water bottle that tracks daily water intake using smart technology to ensure that you are appropriately hydrated throughout the day. The Spring bottle connects to the Bellabeat app to track your hydration levels.

**Bellabeat membership**: Bellabeat also offers a subscription-based membership program for users. Membership gives users 24/7 access to fully personalized guidance on nutrition, activity, sleep, health and beauty, and mindfulness based on their lifestyle and goals.

This dataset has been originally generated by respondents to a distributed survey via Amazon Mechanical Turk and contains personal fitnesss tracker of thirty (30) eligible fitbit users. The dataset used for the purpose of this analysis is available on Kaggle [FitBit Fitness Tracker Data](https://www.kaggle.com/datasets/arashnic/fitbit) [accessed on 10/01//23]  

### Scenario

I will be working in the capacity of a junior data analyst at marketing analyst team at Bellabeat, a high-tech manufacturer of health-focused products for women. I have been asked to focus on one of Bellabeat’s products and analyze smart device data to gain insight into how consumers are using their smart devices. The insights I discover will then help guide marketing strategy for the company. I will present my analysis to the Bellabeat executive team along with my high-level recommendations for Bellabeat’s marketing strategy.

## Ask
### Business Task
The key business task of this analysis is to analyze smart device usage data in order to gain insight into how consumers use the non-Bellabeat smart devices which would subsequently, help influence Bellabeat marketing strategy. 

### Analysis Questions:

1. What are some trends in smart device usage?
2. How could these trends apply to Bellabeat customers?
3. How could these trends help influence Bellabeat marketing strategy?

## Prepare
### Data Source
The prepare step generally provides adequate information on data source.

The dataset used for this analysis is publicly available on Kaggle [FitBit Fitness Tracker Data](https://www.kaggle.com/datasets/arashnic/fitbit), and is stored in eighteen(18) csv. files which consists of daily activities such as; steps, calories, heartrate, sleep, etc.
The data, which contains personal tracker was submitted and consented to by 30 eligible fitbit users.
Most of the csv. files are stored in long format while some are stored in narrow format.
To test the integrity of the data; the dataset is expected to be **ROCCC** which stands for **Reliable, Original, Comprehensive, Current , Cited** respectively.

**Reliable**- the reliability of the dataset can be contested as there are some limitations. For instance, the sample size,(personal tracker details of only 30 users was provided) which may lead to sampling bias. Similarly, the gender of the 30 users is completely unknown and it is a fact that Bellabeat as a wellness company is majorly focused on the wellness and fitness of women.

**Original**- the dataset cannot be said to be original as it was provided by a third party(Amazon Mechanical Turk).

**Comprehensive**- the dataset can be said to be comprehensive enough as the whole of the 18 csv files contains adequate information about the users’ activity ranging from heartrate, sleeptime, intensities, calories burnt, weight etc.

**Current**- For a dataset that was collected and last updated since 2016, and is being used for an analysis in 2022, the dataset cannot be said to be current.

**Cited**- the dataset has been properly cited as a third party data and is available in the public domain.

### Data Organization

 The dailyActivity_merged , weightLoginfo_merged and sleepDay_merged csv files have been selected to carry out this analysis as the former contains all tracker details of users on a daily basis. All 3 files were migrated into one workbook but different sheets and saved as an excel workbook.
 
 ## Process
 The process of data cleaning, transformation and visualization will be carried out in GoogleSheets and Pivot table and Charts.

**Data Cleaning and Transformation**

![1_page-0001](https://github.com/Raksha-17/Bellabeat-Fitness-Case-Study/assets/146487383/de6a5caf-5624-4486-b546-4994208d9921)
An overview of the daily_activity_merged dataset

![2_page-0001](https://github.com/Raksha-17/Bellabeat-Fitness-Case-Study/assets/146487383/ea91d476-770b-4542-9100-bb810e4b8b6c)
An overview of the SleepDay_merged dataset

![3_page-0001](https://github.com/Raksha-17/Bellabeat-Fitness-Case-Study/assets/146487383/a2d6038d-5898-410e-8752-42cad917be64)
An overview of the weight_loginfo dataset

I converted the workbooks from csv files into Google Sheets workbooks in order not to lose part data while working in csv file.


The date column of the Weight_Loginfo comprises of both date and time, so I used the power query to split column by the space delimiter, used the Text to columns function under the data tab to format the date into “ddmmyyyy” format and created named ranges for the column headers. I then used the TEXT function to extract the Days and Month in the date -

=TEXT(D2,"ddd") , =TEXT(D2,"mmm")

![Screenshot 2023-10-09 8 41 56 AM](https://github.com/Raksha-17/Bellabeat-Fitness-Case-Study/assets/146487383/2295714f-67dc-41e0-b723-ae183d4b3ef2)
An overview of the sleepDay_merged after transformation



All these being done, I now have my dataset in one worksheet where I continued my data transformation by ;

* converting the dataset into tables

* creating named ranges with the top row (column headers)

* using the formula =UNIQUE(B2:B1000) to ascertain how many users are contained in the dataset. Here, we found out that there are 33 unique IDs as opposed to the 30 users expected.

* with this formula =UNIQUE(D2:D1000) I was able to know that only 8 users logged their weight details, which means we will be working with weightinfo for 8 people as against the 33 unique users.

* using formula =SUM(O2+P2+Q2+R2) to create a new column named Total_minutes.

* formatting the date columns into dd-mm-yyyy format using the date option in Text to columns too , then used the function =TEXT([C2,”dddd”) to extract the day from the date.

* using the formula =CONVERT(H12,"mn","hr") to convert minutes TotalMinutesAsleep to TotalHoursAsleep and lastly,

* formatting the numbered columns into two(2) decimal places. Below is a view of all columns in the dataset after cleaning and transformation;



![Screenshot 2023-10-09 8 49 37 AM](https://github.com/Raksha-17/Bellabeat-Fitness-Case-Study/assets/146487383/43087d09-a074-498b-a26c-24c4da06e3eb)
The dataset after cleaning and transformation 1


![Screenshot 2023-10-09 8 52 18 AM](https://github.com/Raksha-17/Bellabeat-Fitness-Case-Study/assets/146487383/3dd0d5a8-0fbf-41f7-83a1-6073a9d1b717)
The dataset after cleaning and transformation 2

It is also important to note that only 24 users have their daily sleep records logged and this was determined using the formula- =UNIQUE(B2:B1000).

Now, I have my dataset in 20 columns and 941 rows(including headers) for my dailyActivity dataset, with 11 columns and 411 rows(including headers) for the sleepDay dataset and the WeightLoginfo consists of 13 columns and 68 rows(including headers). This marks the completion of my data cleaning and transformation process. It is time to start my analysis to derive certain insights which leads us to the analyze phase.

## Analyze

As mentioned earlier, all analysis process(using pivot tables), as well as visualization will be carried out in GoogleSheets.

The dailyActivity table has logged info for a total of 33 users, the weightLoginfo has a total number of 8 users, while the sleepday table has a total number of 24 users.

I created a pivot table to illustrate the average total steps of users across all days of the week, and visualized using a stacked column chart.


![Screenshot 2023-10-09 9 12 01 AM](https://github.com/Raksha-17/Bellabeat-Fitness-Case-Study/assets/146487383/5fa3d264-1f3b-4532-b5c9-d726a19c00d0)
Pivot table for average total steps by ID and Day.

![Average total Steps by day of the week per user](https://github.com/Raksha-17/Bellabeat-Fitness-Case-Study/assets/146487383/386ffa77-a2a4-4bc0-91e2-e368fde50075)


Similarly, it can be deduced from the bar chart below that users take more steps Saturdays and Tuesday with least steps on Sundays and Thursdays.

![AVERAGE of TotalSteps per Day (1)](https://github.com/Raksha-17/Bellabeat-Fitness-Case-Study/assets/146487383/c3f86741-8b77-4228-8eef-cd9930a271c4)


![Avg of TotalMinutesAsleep and TotalTimeinBed](https://github.com/Raksha-17/Bellabeat-Fitness-Case-Study/assets/146487383/446ab1df-449e-4679-a1f0-b999fd65123c)

I used the convert function to convert the TotalMinutesAsleep and TotalTimeInBed into hours.


![AVERAGE of TotalHoursAsleep and AVERAGE of TotalHoursInBed](https://github.com/Raksha-17/Bellabeat-Fitness-Case-Study/assets/146487383/5e7bae1f-a18c-4550-8901-4d75a06f6550)


We can see from the above diagram that the user spend an average of 7 hours or 419minutes on sleep and an average of 8hours or 456 minutes in bed. It also shows that users get more sleeptime on Sundays. Users get more sleep on Sundays.

![AVERAGE Calories Burnt per Day](https://github.com/Raksha-17/Bellabeat-Fitness-Case-Study/assets/146487383/a9fe6f2b-6d1c-42ff-8823-1863ee487c22)

Comparing the average total steps chart illustrated above with this average calories burnt chart, it can be established that the daily steps have a positive correlation with the calories burnt, that is, the higher the steps taken, the higher the calories burnt. More calories are burnt on Saturdays and Tuesdays while least calories are burned on Sundays and Thursdays.

![Percentage of Minutes in Different Categories](https://github.com/Raksha-17/Bellabeat-Fitness-Case-Study/assets/146487383/ba245914-6056-4602-ab28-a55490efff38)

Above is a pie chart which shows the percentage of time users spent in various activity category. Users spend 81% of their time Sedentarily. This can also be seen in the column chart below;

![Total Minutes Category per User](https://github.com/Raksha-17/Bellabeat-Fitness-Case-Study/assets/146487383/ca192ad2-760d-4538-a186-c2459fd749d1)

This brings us to the end of the analysis phase. Its is time to move on to the share phase where we pitch/share our insights and visuals (in an organized format) from the analysis carried out to the stakeholders.

## Share

The share phase as stated above is all about sharing our findings to the primary / secondary stakeholders of the business. I have been able to deduce the following from the analysis I carried out;

**Insights**

* A total of 33 users provided their daily steps and calories over a period of 31 days each. About 88% of users were able to track their daily steps/calories burned for 25days and more while the remaining 12% did less than 25 days.
  
* 8 users provided their their daily weight report, out of which only 2 users were able to track their daily weight for 24–31 days while the remaining 6 users tracked for 5 days or less.
 
* 24 users provided their daily sleep minutes and minutes in bed, out of which 42% was able to track their sleep data for 25–31 days while 58% only tracked their sleep for less than 25days.
 
* The number of steps taken per day has a positive correlation with calories burned.
  
* Users take an average of 7,637 steps in a day while burning a total of 2,303 calories on the average.
  
* Users spend about 81% of their time in sedentary.
  
* Users tend to spend and average of 419 mins-which is approximately 7hours- on sleep, while they spend about 458 minutes-which is approximately 8hours in bed, while spending more time in bed and getting more sleep on Sundays.
  
* Users tend to take more steps on Saturdays and Tuesdays with least steps on Sundays and Thursdays.

Below is the visualization dashboard I created for this analysis;

![dashboardd](https://github.com/Raksha-17/Bellabeat-Fitness-Case-Study/assets/146487383/9e7acad3-abff-45a5-9d8d-d821dcbd87a3)

## Act
Bellabeat wellness company is a health technology company that focuses on providing high-tech wellness/fitness product for women, but as a limitation, there was no demographic to connote that the data provided was collected from women which may result in sampling bias. It is recommended that the company focuses on primary data sources for future analysis other than collecting third party data.

Other Recommendations to the stakeholders are;

* Utmost priority should be given to products that allow users track their daily activity such as steps and calories burned as users are more interested this, which will in turn increase revenue.
* Launch a campaign to create awareness to more women about the importance of health monitoring, tracking and keeping fit.
* Provide incentives (e.g membership upgrade, bonus points, rewards/awards) to users who do not renege on the daily monitoring/tracking of activities which will encourage more sedentary/inactive users to put in the work.
* Occasionally rollout health tips/articles which keeps users educated on how to do better.
* Infuse high-tech features into all products which sends a notification to the user after a considerable amount of time of inactivity.
* Lastly, ensure that that products are 99.9% effective (in terms of battery hours, flexibility, user experience) in order to avoid lapses in capturing of user’s activity, because about 61% of manual reporting was done by users who kept track of their daily weight.

The purpose of this project was to explore a dataset from an online store Ice that sells video games all over the world. The intent was to gather data to inform their 2017 marketing campaign using predictive analysis of data from previous years.

# Ice Video Game Sales Analysis Project

## Overview

This project simulates a real-world data science activity by analyzing video game sales data for Ice, an online store selling games worldwide. The analysis identifies patterns that determine a game's success, aiding in spotting potential big winners and planning advertising campaigns for 2017.

## Project Summary

The project encompasses data review, preparation, analysis, user profiling by region, hypothesis testing, and general conclusions leading to actionable marketing recommendations.

## Table of Contents
1. [Project Introduction](#project-introduction)
2. [Step 1: Reviewing the Dataframe](#step-1-reviewing-the-dataframe)
3. [Step 2: Preparing the Data](#step-2-preparing-the-data)
4. [Step 3: Analyze the Data](#step-3-analyze-the-data)
5. [Step 4: Create a User Profile for Each Region](#step-4-create-a-user-profile-for-each-region)
6. [Step 5: Testing the Hypotheses](#step-5-testing-the-hypotheses)
7. [Step 6: Write a General Conclusion](#step-6-write-a-general-conclusion)

## Project Introduction

The project involves simulating a real-world data science task where I act as an analyst for Ice, an online store that sells video games globally. I will analyze the provided dataframe (games.csv) to identify patterns determining a game's success, enabling strategic advertising campaigns.

## Step 1: Reviewing the Dataframe

Initial review of the dataframe to understand the data and identify necessary corrections, alterations, or adjustments prior to analysis.

*   **Columns**: Name, Platform, Year_of_Release, Genre, NA_sales, EU_sales, JP_sales, Other_sales, Critic_Score, User_Score, Rating
*   **Entries**: 16715
*   **Missing Data**: Name (2), Year_of_Release (269), Genre (2), Critic_Score (8578), User_Score (6701), Rating (6766)
*   **Duplicates**: None
*   **Data Types**: Object (5), Float64 (6)

## Step 2: Preparing the Data

Data cleaning and preprocessing steps include:

*   Converting column names to lowercase.
*   Changing data types to appropriate formats.
*   Handling missing values.
*   Creating a total sales column.

### Data Type Conversion

*   `year_of_release` to Int64
*   `genre` to category
*   `user_score` to float64
*   `rating` to category

### Handling Missing Values

*   Dropped missing values in the `name` and `genre` columns.
*   Left missing values in `critic_score` and `user_score` unchanged.
*   Filled missing `rating` values with 'unknown'.

### Total Sales Column

Created a `total_sales` column by summing regional sales (`na_sales`, `eu_sales`, `jp_sales`, `other_sales`).

## Step 3: Analyze the Data

### Games by Years

*   Most games were released in 2008 and 2009.
*   Peak game creation occurred between 2006-2011.
*   Game production began decreasing in 2012.

### Sales by Platform

*   Top 5 platforms by total sales: PS2, X360, PS3, Wii, DS

### Last 10 and 5 Years Analysis
*   Created new dataframes for the last 10 years (2007-2016) and the last 5 years (2012-2016) to focus on relevant trends.
*   Analyzed platform sales for these periods to identify growing and shrinking platforms.

### Top Platforms (Last 5 Years)

*   PS4, 3DS, PC, XOne, and WiiU

### User Data and Professional Reviews Analysis on PS4

*   Analyzed correlation between critic scores, user scores, and sales for the PS4 platform.
*   Critic score had a weak correlation with sales, while user score showed little to no correlation.

### Game Sales across Platforms

*   Compared sales of top games across platforms to determine the most popular platforms for specific titles.

### Games by Genre

*   Action, Sports, and Shooter were the top-selling genres overall.

## Step 4: Create a User Profile for Each Region

### Market Share by Platform (Last 5 Years)
*   **NA**: X360, PS4, PS3, XOne, 3DS
*   **EU**: PS4, PS3, X360, XOne, 3DS
*   **JP**: 3DS, PS3, PSV, PS4, WiiU

### Market Share by Genre (Last 5 Years)
*   **NA**: Action, Shooter, Sports, Role-Playing, Misc
*   **EU**: Action, Shooter, Sports, Role-Playing, Racing
*   **JP**: Role-Playing, Action, Misc, Simulation, Fighting

### ESRB Ratings (Last 5 Years)
*   **NA**: M, E, Unknown, E10+, T
*   **EU**: M, E, Unknown, E10+, T
*   **JP**: Unknown, E, T, M, E10+

## Step 5: Testing the Hypotheses

*   **Hypothesis 1:** The average user ratings for the xOne and PC platforms are the same.
    *   Failed to reject the null hypothesis
*   **Hypothesis 2:** The average user rating for the action and sports genres is different.
    *   Rejected the null hypothesis.

## Step 6: Write a General Conclusion

### Data Cleaning

*   No duplicate values were found.
*   Missing values in the name and genre columns were removed.
*   Missing values in the critic_score and user_score columns were left unchanged.
*   Missing values in the rating column were replaced with "unknown."

### Data Analysis

*   PS4 was the most popular platform in the NA, EU, and Other regions.
*   3DS was the most popular platform in the JP region.
*   Action, shooter, and sports games were the most popular genres in the NA and EU regions.
*   Role-playing games were the most popular in the JP region.
*   Critic_score was a better predictor of a game's success than user_score.

### Hypothesis Testing

*   Failed to reject the null hypothesis that the average user ratings for the xOne and PC platforms were the same.
*   Rejected the null hypothesis that the average user rating for the action and sports genres were the same.

### Recommendations for the 2017 Marketing Campaign

*   Focus on the PS4 platform as it is the most popular platform in most regions.
*   Consider the XOne platform in the NA region and the 3DS platform in the JP region.
*   Target action and shooter games, as these are the top genres.
*   Consider role-playing games for the JP region.
*   Focus on games with M and E ratings, as these were the most popular.

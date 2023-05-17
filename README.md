# Recipes and Ratings: Quality over Quantity?
by Tauhid Noor (tnoor@ucsd.edu)

## Introduction
This report is based on the data collected over recipes and people's interactions with them. The original dataset that will be used has over 200,000 rows and 15 columns, but I will add several columns during the data cleaning and exploratory process. The columns that are relevant to answering my question are `rating`,and `calories`.`rating` column is the data of how the people ranked the recipe from 1 to 5 (worst to best).`calories` column (which originally came from the `nutrition` column) tells us how many calories the recipes contain. My question asks if higher rated recipes tend to be less caloric than lower rated recipes. I think this question is worth investigating because it could spur a health beneficial report for those who want to lose weight without having to suffer duller food. 

**Question:** Do higher rated recipes have fewer calories than lower rated recipes?

## Cleaning and EDA
Here are a few values of dataframe with the two most important columns.
|    |   rating |   calories |
|---:|---------:|-----------:|
|  0 |        5 |       95.3 |
|  1 |        5 |      143.5 |
|  2 |        5 |      182.4 |
|  3 |        5 |      182.4 |
|  4 |        4 |      658.2 |

Here are the steps I took in the the data cleaning process:

1. The rating values which are 0 have been changed to 'nan' value since if a rating hasn't been given, its default value would be 0. In order to tackle this issue, it's best to replace 0 with the value 'nan' to indicate the missingness of the rating data.

2. It's important to clean the data even further to make it more readable and concise for the purpose of convenience. Hence, I will remove the redundant column 'id' since 'recipe_id' is already there, and change the `nutrition` column into multiple ones (calories column included) where the different values within a list will be allocated to their own respective columns so that it's easier to know what those values mean.

3.I will now create two columns where one looks at the age of the submitted recipe and the other looks at the age of the interaction. We will hold the latest year to be 2023. In total, we will now have 25 columns.

4. After cleaning the data, it's time to create data visualisations to observe any trends or patterns that we can then investigate and help answer our question that may or may not change.

With the data cleaning process, I was able to analyze more columns (calories, sugar, protein, etc) to see if there were trends. Hence, I was able to come up with my question that looked to investigate the relationship between calories and ratings. Here are some of the trends I looked at: 

## Assessment of Missingness

## Hypothesis Testing
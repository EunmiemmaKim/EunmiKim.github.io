---
header:
  overlay_image: /assets/images/research/header.jpg
  caption: "Photo credit: [**Roman Mager**](https://www.unsplash.com)"
permalink: /portfolio/Accident_analysis/
date: 2020-11-01
toc: true
toc_label: "Contents"
---

# **UK ACCIDENT ANALYSIS**

*(Code for this project is available on [GitHub][1].)*

## **Executive summary**

There are many accident casualties recorded on Britain’s road. 46% of those fatal road accident victims were car occupants which cause the fatal injury. According to the World Health Organization, more than 1.25 million people die each year as a result of road traffic crashes. Injuries from road traffic accidents are the leading cause of death among people aged between 15 and 50 years of age. Traffic accidents are one of the events in life that anyone would at least encounter once. We would like to prevent severe accidents from happening. From this analysis, we will understand which key contributors affect the accidents.

We will create awareness that which area, time, day, speed limit, and, weather condition the accidents happened mostly from the data. Regulations can be framed by insights like we can set some signs on that areas where the accidents happened the most and tighten regulations on speed limit to prevent the accidents. At last, we will prevent loss of life and property. 



## **PROJECT DESCRIPTION**

Through exploratory analysis, data pre-processing, and creating machine learning models utilizing Python, the goal of our project was to uncover patterns that might be hidden in data and gain insight into possible predictors of fatal traffic accidents.

The reason for choosing this topic was twofold; we felt that the dataset was sufficiently complex enough to make a purposeful project and further the skills that we learned in class, and secondly, if we were to make certain discoveries about the nature of fatal accidents, those discoveries could have meaning beyond the class room.  Driving is a daily task with risks that are no secret to anyone who gets behind the wheel but if we could somehow mitigate that risk through what we learned, we could not only be safer ourselves but share that knowledge to a broader audience.


## **DATASET DESCRIPTION**


Our dataset was obtained from the Department for Transport of the UK government and it covers detailed road safety data about traffic accidents in Great Britain.  The target variable in our analysis was whether a traffic accident was fatal or not fatal.  Our dataset covered 10 years of accidents from 2005 - 2015  and contained over 1 million records. 

Our final dataset used in analysis was a combination that we derived from two separate sources of data, one pertaining to vehicle information and one pertaining to accident specific information.  Unfortunately we were limited in the scope of our analysis by the way the two datasets were created; for instance, both datasets use the same primary key to index the same accident but because the vehicle information dataset uses the same primary key for multiple vehicles and our target variable was in another dataset, it was impossible to decipher which party had the fatality or not.

The combination dataset that we created contained 37 different accident related attributes.  Because of the methodology that the Department of Transport used to obtain their information (collecting information from standardized police reports) most of the variables were categorical which makes sense if an officer is referencing a standardized form.  Examples of the types of variables that were collected are weather conditions, speed limit, road surface conditions, and the age of the driver.  

Because many of our variables were categorical we had to create a large dataset containing mostly dummy variables.  In retrospect, after learning what we have from this project we would have preferred to work with data that contained more attributes that were continuous variables because our data limited the scope of our analysis.



## **METHODOLOGIES**

**1.	Exploratory Analysis**

a.	Cluster Map - To find the peak hours and days of major accidents<br>
b.	Bar Plots - To check the skewness of fatal v/s non-fatal accidents<br>
c.	Pie Charts - To find the road type and junction that are prone to maximum accidents

**2.	Data pre-processing**

a.	Removed nulls and unknown records<br>
b.	Removed duplicates with Vehicle Reference<br>
c.	Manual encoding to highlight weekday/weekend rush hours<br>
d.	One-hot encoding to run regression model<br>
e.	Manual sampling/random shuffling to address imbalanced target variable

**3.	Machine Learning Models**

a.	Logistic Regression<br>
b.	Decision Tree<br>
c.	Random Forest<br>
d.	Naive Bayes

## **RESULTS**

**1.	ROC Curve**

The accuracy score of all ML models were compared using ROC Curve. Random Forest model had the highest accuracy score (0.72), followed by Logistic Regression (0.70), Decision Tree (0.69) and Naive Bayes (0.67)
 
**2.	Classification Report Comparison**

Used stacked bar chart to compare precision, recall, F1 score and accuracy of all models. The weighted scores for each of these metrics ranked highest for Random Forest followed by Logistic Regression, Decision Tree and Naive Bayes. This validated our findings from ROC curve.



## **IMPLICATIONS**

Random Forest being the most accurate ML model with highest precision, recall and F1 score was used in determining the significant predictors of accident severity. Below are the Top 10 significant predictors derived with the help of Random forest feature importance:

1.	Number of Vehicles

2.	1st of Impact (Front)

3.	Engine Capacity (CC)

4.	Vehicle type (Motorcycle 50cc and under)

5.	Vehicle type (Motorcycle over 500cc)

6.	Vehicle manoeuvre (Waiting to go)

7.	Number of casualties

8.	Junction detail (Roundabout)

9.	Vehicle manuoeuvre (Slowing or stopping)

10.	Sex of driver (Female)


**SOURCES**
•	www.kaggle.com
•	www.analyticsvidhya.com
•	www.towardsdatascience.com
•	www.stackoverflow.com
•	www.researchgate.com 

	
[1]: https://github.com/EunmiemmaKim/UK_Accidents_project



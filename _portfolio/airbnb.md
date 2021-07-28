---
header:
  overlay_image: /assets/images/research/header.jpg
  caption: "Photo credit: [**Roman Mager**](https://www.unsplash.com)"
permalink: /portfolio/airbnb/
date: 2019-03-01
toc: true
toc_label: "Contents"**
---

# **Airbnb_NY_project**

 (The code is publicly available [on GitHub][1].)

## Context
Since 2008, guests and hosts have used Airbnb to expand on traveling possibilities and present more unique, personalized way of experiencing the world. This dataset describes the listing activity and metrics in NYC, NY for 2019. This data file includes all needed information to find out more about hosts, geographical availability, necessary metrics to make predictions and draw conclusions.

## Data description 
This public dataset is part of Airbnb, and the original source can be found on this website. AB_NYC_2019.csv include the information of Airbnb hosts- detailed listings data showing 48895 hosts in the dataset. Some of the attributes used in the analysis are room_id (categorical), host_id(categorical), neighborhood (categorical), room_type (categorical), price (continuous),
minimum_nights (continuous), number_of_reviews (continuous), reviews_per_month (continuous), host_listings_count(continuous), availability_365(continuous) among others.


## Inspiration
•	What can we learn about different hosts and areas? <br>
•	What can we learn from predictions? (ex: locations, prices, reviews, etc) <br>
•	Which hosts are the busiest and why? <br>
•	Is there any noticeable difference of traffic among different areas and what could be the reason for it? <br>
The inspiration for my analysis are the questions below <br>
•	Which are the famous neighborhoods and neighborhood groups among the listings? <br>
•	What is the price range of the listings? <br>
•	What are the mst common words used in the description? <br>
•	Which room types are usually busy ? Is the trend different in different neighborhoods? <br>
•	How are the reviews distributed? <br>

## **Pre-processing**
Many reviews are missing. There are 10052 missing values in last_review and reviews_per_month out of 48895. Since id and host_name are not the important variables, so I decide to delete two variables. Also, last_review variable is deleted because it has many null values in it and the number of reviews is more significant to find out information.

## **Exploratory Data Analysis**
In this section, we will detail our analysis to the questions of interest mentioned in the introduction and gain preliminary insights through exploratory data analysis and visualization. We have divided it into four subsections that aim to answer the questions through a variety of different visualization.
- Correlation Analysis
- Spatial Data Analysis
- Wordcloud Analysis

### **1. Correlation Analysis**
Correlation is a bivariate analysis that measures the strength of association between two variables and the direction of the relationship. There is no correlation between variables in this dataset. 
<center>
<img src="{{ "/assets/images/correlation_airbnb.png" | absolute_url }}"
 width="80%" height="80%"  align="center">
</center>


### **2. Spatial Data Analysis**

**1) How many airbnb are in different areas?**

Most of airbnb houses are gathered in Brookly and Manhattan.
<center>
<img src="{{ "/assets/images/airbnb.png" | absolute_url }}"
 width="80%" height="80%"  align="center">
</center>


**2) Price differences in areas**

Manhattan area has the most expesnsive rental fee on airbnb. The mean of house rental fee reaches around $ 200. Leading on top of Brooklyn, Staten Island,Queens,and Bronk. The site's highest growth of tourists for that week didn't coming from Manhattan, or even Brooklyn - It came from Queens. But still Manhattan and Brooklyn are the busier areas than others. We can see the range of price in areas.

**3) Number_of_reviews**

Let's see The number of reviews between Mahattan and Staten island. The retan fee in Staten island is far lower than in Manhattan but the average reviews Airbnb hosting owners have got in Staten island is higher than in Manhattan. It seems that the more expensive the rental fee is the less reviews they get.

Neighbourhood_group   | Number_of_reviews | 
-------|------|
Manhattan  |    20.98  | 
Brooklyn  | 24.2  |   
Bronx  | 26    | 
Queens |   27.7   | 
Staten Island |   31   | 

**4)Availability** 

The crowded and popular areas tend to have lower availability customers can use. Overall Brooklyn and Manhattan are the shorter available days customers make a reservations for.

<center>
<img src="{{ "/assets/images/airbnb2.png" | absolute_url }}" 
width="80%" height="40%" align="center">
</center><br>

**5) Neighbourhood_group& Room type**

In Manhattan, there is more types of entire home or apartments than other types, private room and shared room. Airbnb host in other areas post the type of private rooms more than other types.

<center>
<img src="{{ "/assets/images/airbnb3.png" | absolute_url }}"
 width="80%" height="80%"  align="center">
</center>

**6) Top 20 densely populated area**

This showing that the top 20 neighbourhoods which have the rental houses on airbnb among 221 neighbours in New york.
<center>
<img src="{{ "/assets/images/top20_airbnb.png" | absolute_url }}"
 width="80%" height="80%"  align="center">
</center><br>
This below picture express the geographical distribution of top 20 neighborhood which are densely populated.It gives the overall sense of how the top 20 airbnb neighborhood are distributed. In the top 20, Manhattan contains more the populated neighborhoods than others. However, the populated neighborhoods in Staten Island have the more expensive rooms than others. 
<center>
<img src="{{ "/assets/images/top20_2_airbnb.png" | absolute_url }}"
 width="80%" height="80%"  align="center">
</center>

**7) Distribution**

It gives the overall sense of how the listings are distributed across neighborhood. 
<center>
<img src="{{ "/assets/images/spatial_airbnb.png" | absolute_url }}"
 width="80%" height="80%"  align="center">
</center>

Price is the important factor Map shows the price range of rooms in this 5 areas. Now it is obvious that the highly pulated location would also tend to be costly. There are more tourist in Manhattan than other areas.
<center>
<img src="{{ "/assets/images/spatial_airbnb2.png" | absolute_url }}"
 width="80%" height="80%"  align="center">
</center>

This map follows from our previous analysis. The listings with entire rooms in Manhattan are listed the most. It means that the entire rooms rent cost more than the shared room and the private room. 
<center>
<img src="{{ "/assets/images/spatial_airbnb3.png" | absolute_url }}"
 width="80%" height="80%"  align="center">
</center>


### **3. Wordcloud Analysis**

The wordcloud analysis shows that which words are used more. Mostly, the room type and location words are used. Also, the words including beautiful, luxury, charming, quiet can be used to lure customers. 

<center>
<img src="{{ "/assets/images/wordcloud.png" | absolute_url }}"
 width="80%" height="80%"  align="center">
</center>



<!------------------------------------ FOOTER -------------------------------->
	
[1]: https://github.com/EunmiemmaKim/Airbnb_NY_project/blob/master/Airbnb%20Project.ipynb

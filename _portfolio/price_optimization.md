---
header:
  overlay_image: /assets/images/research/header.jpg
  caption: "Photo credit: [**Roman Mager**](https://www.unsplash.com)"
permalink: /portfolio/price_optimization/
date: 2020-01-01
toc: true
toc_label: "Contents"
---

# **Price Optimization**
 (The code is publicly available [on GitHub][1].)

## **Context**

Country Beeristan, a high potential market, accounts for nearly 10% of Stallion & Co.’s global beer sales. Stallion & Co. has a large portfolio of products distributed to retailers through wholesalers (agencies). There are thousands of unique wholesaler-SKU/products combinations. In order to plan its production and distribution as well as help wholesalers with their planning, it is important for Stallion & Co. to have an accurate estimate of Sales at SKU level for each wholesaler.
Content
•	The dataset was obtained from Kaggle.com. 
•	The dataset contains Average population, Average yearly household income, Promotion, Price, Sales, and Weather.
•	We are going to compile and bind them to collect the important information for our analysis. 

### **Data**
**Pricesalespromotion.csv**: ($/hectoliter) Holds the price, sales & promotion in dollar value per hectoliter at Agency-SKU-month level<br>
**Historicalvolume.csv**: (hectoliters) Holds sales data at Agency-SKU-month level from Jan 2013 <br> **Dec 2017 Weather.csv**: (Degree Celsius) Holds average maximum temperature at Agency-month level <br>**Industrysodasales.csv**: (hectoliters) Holds industry level soda sales <br>
**Eventcalendar.csv**: Holds event details (sports, carnivals, etc.)<br>
**Industry_volume.csv**: (hectoliters) Holds industry actual beer volume<br>
**Demographics.csv**: Holds demographic details (Yearly income in $)

## **Project description**

We are going to find price elasticity estimation to see when price goes up, consumption goes up or down and execute pricing optimization for different SKUs to maximize operating profit. Also, we can see the effect of promotion and weather on sales. 

## **Purpose**

This data contains sales information for each SKU level for each wholesaler, promotional event and weather. From this data, we are going to measure how demand changes in response to a price change. This can be helpful for the company to maximize their revenue. To maximize revenue, we are going to find optimization prices for each SKU level. In addition, we can make a promotion strategy to maximize revenue considering each promotional event. To do so, the company can determine how customers will respond to different prices for its different SKUs and different promotional event. Furthermore, we can investigate how external factor such as weather affect this price optimization result. As the result of this project, the company can reduce their operating costs, inventories, and etc. They can benefit from price elasticity estimation and pricing optimization to determine the best price for each SKUs.



	
[1]: https://github.com/EunmiemmaKim/Price_optimization-/blob/master/Price_optimization%20.R


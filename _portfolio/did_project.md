---
header:
  overlay_image: /assets/images/research/header.jpg
  caption: "Photo credit: [**Roman Mager**](https://www.unsplash.com)"
permalink: /portfolio/did_project/
date: 2019-11-01
toc: true
toc_label: "Contents"
---

# **MSRP Analysis using Stata**

## **Project Summary** 
Predicted the price of cars with features including make, model, year, engine, and other properties of the car comparing the price of cars before and after the electronic car was released

Electronic cars are introduced to market in 2008-2009, we’d like to use two cross-section data to investigate the impact of electronic cars on the MSRP of sedans (with the pickup as a control group).

We decided to use Different in Different investigate two cross sections of MSPR before and after the electric vehicles such as tesla come into the market, which is around 2009-2010 and use these two cross sections to determine whether the introduction of electric cars to the market had an impact to the price of the competitors with internal combustion engines.

**Applied Skills**: DID with pooling cross-section data, Logit Model, Exploratory Analysis

## **Data**

This set of data is retrieved from Kaggle.com

<img src="{{ "https://user-images.githubusercontent.com/53354807/128274748-ee917dc0-619a-4307-824c-15131d455380.png" | absolute_url }}"
width="50%" hspace="20" align="right">

It originally contains 16 attributes, 11914 records. It contains specification and MSRP (Manufacturer Suggested Retail Price ) of different models in the US market from 1990 to 2017.

The introduction of electric vehicles (sedan/SUV) comes into the market around 2009-2010. So the cross section we decided to pick is 2008 and 2016.

After narrowing down the scope, 350 records of 2008 and  2157 records of 2016 remained in the dataset.

## **Data Pre-processing**

- Year:2009, 2017
- Record: 350+ 2157
- Omitting records with missing values
- Omitting Electric and Hybrid Cars
- Omitting and Combine attributes
- Omitting Outliers


## **Model Creation** 

Where Log(msrp) is the natural logarithm of manufacturer suggested retail price, γt is a vector of dummy variables for each observed year, Treat is a dummy variable which equals 1 if car belongs to the conventional car (hatchback,sedan,SUV) otherwise it equals to zero (pickup,van).

<img width="815" alt="did_car-Copy1" src="https://user-images.githubusercontent.com/53354807/128274710-12a1bf9c-c1a8-491a-abf6-330e44d5bea0.png">

**Step 1:** <br> 

Electronic cars are introduced to market in 2008-2009, we’d like to use two cross-section data to investigate the impact of electronic cars on the MSRP of sedans (with the pickup as a control group).
At first, we estimate the regression model. <br><br>
**Log(msrp)= β0 + β1γt + β2γt ∗Treat + β3Treat + u**<br><br>
Where Log(msrp) is the natural logarithm of manufacturer suggested retail price, γt is a vector of dummy variables for each observed year, Treat is a dummy variable which equals 1 if car belongs to the conventional car (hatchback,sedan,SUV) otherwise it equals to zero (pickup,van).<br><br>
Then we plot the estimate of β2 (with 95% confidence interval) for each observed year. As we can see, prior to 2008, sedans trend appears to closely follow the trend of pickup MSRP. From 2008, the coefficient estimates are positive onward and increase significantly when the Electronic cars are introduced to market, indicating a huge effect of electronic cars on conventional cars MSRP. From 2015, the difference becomes decreasing.We select 2009 and 2017 data to make a prediction.

![다운로드](https://user-images.githubusercontent.com/53354807/128274917-fce34ae3-90ab-4fc5-9da6-c59d06214603.png){: width="700px",hight="300px" }  

**Step 2: DID**

![다운로드](https://user-images.githubusercontent.com/53354807/128274715-cfac9713-3525-4495-aeea-502cd2ba0370.png){: width="700px",hight="300px" } <br> 

We can see the price of sedan is decreasing from 2009 to 2017 with the electronic cars introduced to the market.

![다운로드](https://user-images.githubusercontent.com/53354807/128274716-632597bb-398d-441b-9a70-55920c66aa7d.png){: width="700px",hight="300px" } 

### **Regression with all the variables**

Then we delete all the collinearity variables and variables which P-value are larger than 0.05.
Then we regress the selected variables again and get the result below. Including more variables in the DID model brings a larger R-squared .875 and a significant t-statistic for y2017_treat which means this estimate is statistically different from zero. 

### **Regression without all the collinearity variables**

<img src="{{ "https://user-images.githubusercontent.com/53354807/128274717-0175414b-f285-40fb-868d-99b013d0b3f9.png" | absolute_url }}" align="center">

Then we regress the selected variables again and get the result below. Including more variables in the DID model brings a larger R-squared .875 and a significant t-statistic for y2017_treat which means this estimate is statistically different from zero. 

**Step 3:**

### **Use log(msrp) to get an approximate percentage effect of DID**

<img src="{{ "https://user-images.githubusercontent.com/53354807/128274718-b701cb62-5257-419b-a672-4ba9bb3456e5.png" | absolute_url }}"
 align="center">

The coefficient on y2017_treat (-0.25) implies that, because of the introduction of electronic cars, sedans lost about 25% in market value. The t-statistic is also significant, which means this estimate is statistically different from zero. 

	
[1]: https://github.com/EunmiemmaKim/UK_Accidents_project



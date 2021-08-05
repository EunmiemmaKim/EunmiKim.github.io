---
header:
  overlay_image: /assets/images/code.jpg
  caption: "Photo credit: [**Marcus Spiske**](https://unsplash.com)"
permalink: /portfolio/ebola_virus/
category: machine_learning
date: 2018-01-05
toc: true
toc_label: "Contents"
---

# **Ebola Virus Analysis**

## **Summary**

A Shiny app present the distribution of Ebola virus over time. The code is publicly available [on GitHub][1].

## **Introduction**

In this project, I created a Shiny app that summarizes information about the Western African Ebola virus epidemic. Ebola virus disease (EVD), formerly known as Ebola haemorrhagic fever, is a severe, often fatal illness affecting humans and other primates.

The virus is transmitted to people from wild animals (such as fruit bats, porcupines and non-human primates) and then spreads in the human population through direct contact with the blood, secretions, organs or other bodily fluids of infected people, and with surfaces and materials (e.g. bedding, clothing) contaminated with these fluids. 

“ebola_2014_2016.csv” contain each row in this data set contains a report from each region or location for each day. Each column represents the number of cases reported from each country or region
One possibility would be to create a dashboard that would include the following information, among others:
1. The spread of the virus over time
2. The distribution of the virus across countries on a map
3. The fatality and recovery rate of those infected by the virus

## **Preprocessing**

Pre-processing was carried out to display the Ebola virus incidence rate by country by time.


## **Project**

The dashboard include some graphs to check the distribution of Ebola virus outbreaks over time.
I am going to explain the graphs and metrics. There are 3 Metircs, Total number of cases, Total number of death,and Mortality rate at the specific time. It shows how serious is ebora virus around the world. The first two graphs in the middle show that Ebola virus of total cases and total death can be viewed as cumulative results. The next table shows the number of confirmed cases, the number of deaths, and the fatality rate by country, in order of severity.

The map shows the distribution of Ebola virus, and when clicked, the number of each case and number of deaths is displayed. Also, There are the graphs of the moratarity rate and the recovery rate around world. The last graph presents the five most serious countries with the number of the confirmed case.

![ebola-Copy1](https://user-images.githubusercontent.com/53354807/128275251-1eb683cd-119d-4818-acca-a180a19389c2.png)

[1]:https://github.com/EunmiemmaKim/Ebola_shiny/blob/master/Ebolavirus_shiny.R
<br>
<br>
<br>
<br>



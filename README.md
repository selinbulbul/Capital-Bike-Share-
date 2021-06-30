# Capital Bikeshare
Performance evaluation of "Capital Bike Share" bike-sharing system

<div align="center">
<img src="/images/Capital%20Bike%20Share_introduction_photo_1.jpg" width="800px"</img> 
</div>

## Table of contents

* [Introduction](https://github.com/10409/Capital-Bike-Share-/edit/main/README.md#Introduction)
  * [Motivation](https://github.com/10409/Capital-Bike-Share-/edit/main/README.md#Motivation)  
  * [Data](https://github.com/10409/Capital-Bike-Share-/edit/main/README.md#Data) 
    * [Files Description](https://github.com/10409/Capital-Bike-Share-/edit/main/README.md#Files-Description)  
    * [Programming Languages](https://github.com/10409/Capital-Bike-Share-/edit/main/README.md#Programming-Languages) 
* [Empowering the business](https://github.com/10409/Capital-Bike-Share-/edit/main/README.md#bikesharing---Empowering-the-Business)
  * [Growing ridership](https://github.com/10409/Capital-Bike-Share-/edit/main/README.md#Growing-ridership)
    * [Users and time profiles](https://github.com/10409/Capital-Bike-Share-/edit/main/README.md#Users-and-time-profiles)
  * [Users’ preferences and behaviors](https://github.com/10409/Capital-Bike-Share-/edit/main/README.md#Users’-preferences-and-behaviors)
    * [Features and model performance](https://github.com/10409/Capital-Bike-Share-/edit/main/README.md#Features-and-model-performance)
  * [Supply and demand analysis](https://github.com/10409/Capital-Bike-Share-/edit/main/README.md#Supply-and-demand-analysis)
  * [Pollution effect on bike demand](https://github.com/10409/Capital-Bike-Share-/edit/main/README.md#Pollution-effect-on-bike-demand)
* [KPIs](https://github.com/10409/Capital-Bike-Share-/edit/main/README.md#KPIs)
* [Summary](https://github.com/10409/Capital-Bike-Share-/edit/main/README.md#Summary)
* [Data sources](https://github.com/davidellavalle/Capital-Bikeshare/blob/main/README.md#data-sources)
* [Legal Terms](https://github.com/davidellavalle/Capital-Bikeshare/blob/main/README.md#legal-terms)

## Introduction

Micromobility in US shows big increase from 2010. Increasing population, and traffic in cities bikes are giving much more flexibility to people than cars. In 2019 the e-bikes, and scooters riders increased 60% more than 2018, and took 40 million trips on station-based bike share systems (pedal & e-bikes). The largest bike share systems in the bikesharing business are Bay Wheels, Biki, Capital Bikeshare, Citi Bike NYC, Divvy. Riders took 17% more trips on these systems than in 2018. 
 
> “The growth of bike share shows no signs of stopping.” NACTO, National Association of City Transportation Officials, reported in 2017

### Motivation
The aim of this project based on analyzing the data of the “Capital Bikeshare” empower their business. Based on Washington DC Capital bikeshare provides bikeshare system, with more than 4,300 bikes available at 500 stations. Bikes are available 24 hours a day, 7 days a week, 365 days a year.  We were asked firstly to provide some proofs of how and which features has an effect on demand of bikes and secondly measuring KPIs to ensure that one can accomplish the business objective. We are expected to understand how pollution effects the demand of bikes and the most popular bike stations. The **project challenges** include finding the right features correlated with the bike demand through proofs with visualization and machine learning, finding model fits the best to the dataset, and predicting business growth with time series analysis. 

### Data
We were provided with a dataset containing hourly and daily count of rental bikes (2011-2012), as well as data (2021) from capital bikeshare website obtained to analyze the request of the complains about the non-availability of bikes. 

<div align="center">
<img src="/images/Github_2.png" width="500px"</img> 
</div>


<div align="center">
<img src="/images/Github_3.png" width="500px"</img> 
</div>

#### Files Description


#### Programing languages
The programming language used was Python 3.7.7 64-bit. The following packages were used: pandas, numpy, seaborn, matplotlib.pyplot, scikit-learn, statsmodels, plotly, datetime, holidays, prophet. 

## Empowering the business   
To be able to reach our aim three performance evaluation groups were investigated: 

### Growing ridership (LINK TO THE FILE) (TIME SERIES ANALYSIS) 
Daily count rider bikes was taken account for the ridership analysis: 
#### Users Profile   
   1) Registered customers demand is 4 x more than casual in 2011-2012
   2) Both users show increase in 2012 compared to 2011

#### Time Profile
#####   **Hourly Profile** 
   1) Holiday time/weekend preferred time (12:00-17:00)
   2) During the week time rush hour (7:00-09:00 / 17:00-19:00) is most demanding 
   3) Casual users demand is throughout the day (09:00-19:00)
#####    **Weekly Profile**
   5) Registered users use more during the week whereas casual users prefer during the weekend
#####    **Monthly/Seasonal Profile**
   7) the most demand is on 6th and 9th months
   8) 2 years show similar seasonal pattern , 2012 shows higher demand
#####    **Yearly Profile**
   9) Demand increased by 63% in 2012 compared to 2011  

### User preference and behaviour (LINK TO THE FILE) 
#### Features 
##### Correlation Matrix (LINK) 

A correlation matrix is a table showing which features (independent variables) have the most influence on aiding determination of the dependent variable. It is a useful tool when it comes to choose from multiple models. Correlation matrix has been used to understand which feature is more correlated to the demand. Features of 'season', 'yr’, ‘hr, mnth, 'temp', weather, 'hum' has been chosen for furher investigation. 

##### Plots (LINK)

   1) Demand increases with the increase in temperature. Temperature is higher in summer season. 
   2) Humidity increases with rain/snow declines the demand 
   3) Not comfortable weather (rainy, snowy)= lower demand 

#### Model Performance (LINK)

We can use regression analysis to understand the relationship between one or more independent variables and a dependent variable. To check how well a regression model fits a dataset one way would be to calculate the root mean square error (RMSE). RMSE is a metric providing the square root of the average of squared distance between the prediction  from the model and the actual values in the dataset. Using the selected features "Random Forest Regressor" showed the best fit to the dataset. 

## Supply and Demand (LINK)

Capital Bike Share holds 599 stations in Washington DC. 

**Registered Users**: The report of April 2021 shows registered bike riders’ number is 118024. According to the data only 4% of the registered bike riders are returning their bikes to the same station. To be able to understand which stations are used to most used stations divided into four categories. Red and orange categories are particularly important since the usage of the bikes are higher in these categories. Only 3% of the bike stations show particularly used by registered riders. This result indicates we can improve the numbers of the bikes inside of these categories. Further investigation would be analysing how many of our bikes are already in the bike stations before the registration. Especially this information would be important for us to track so that at rush hours we can provide more bikes since 80% of the registered riders are daily workers.  Therefore, rush hour/ traffic/weather analysis can be crucial to check. We only know 4% of the bikes are coming back to the start station. The next analysis will be how many of the bikes are going to red and orange category stations. If we know the number of the bikes that would be help us to estimate how many bikes we need to support on these stations. 80% of the registered riders are salaried employees and they usually tempted to leave their bikes to another station (explains 4%) close to their works. 

**Casual Users**: The report of April 2021 shows casual bike riders’ number is 99449. 13.7 % of the casual bike riders are returning their bikes to the same station.

## Pollution effect on bike demand 

## KPIs

**Growing ridership: 
1) 49% increased in casual, 67 % increased in registered next year 
PHOTO
2) Casual users demand is throughout the day (09:00-19:00), whereas registered riders demand peaks at rush hours. 
PHOTO 
**User preference and behaviour:
3) Demand increases with temperature, whereas decreasing with humidity and cold weather
PHOTO
**Supply and Demand: 
4) Most demanding bike stations for registered and casual 
PHOTO
5) Casual users average ride duration is 3x longer than registered users 
PHOTO

## Summary

## Data sources

## Legal Terms













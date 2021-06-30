# Capital Bikeshare
Performance evaluation of "Capital Bike Share" bike-sharing system

<div align="center">
<img src="/images/Capital%20Bike%20Share_introduction_photo_1.jpg" width="800px"</img> 
</div>

## Table of contents

* [Introduction](https://github.com/10409/Capital-Bike-Share-/edit/main/README.md#Introduction)
  * [Motivation](https://github.com/10409/Capital-Bike-Share-/edit/main/README.md#Motivation)  
  * [Data](https://github.com/10409/Capital-Bike-Share-/edit/main/README.md#Data) 
    * [Files Description](https://github.com/10409/Capital-Bike-Share-/edit/main/README.md#Data)  
    * [Programming Languages](https://github.com/10409/Capital-Bike-Share-/edit/main/README.md#Data) 
* [Empowering the business](https://github.com/10409/Capital-Bike-Share-/edit/main/README.md#bikesharing---the-domain)
  * [Growing ridership](https://github.com/10409/Capital-Bike-Share-/edit/main/README.md#exploratory-analysis)
    * [Users and time profiles](https://github.com/10409/Capital-Bike-Share-/edit/main/README.md#exploratory-analysis)
  * [Users’ preferences and behaviors](https://github.com/10409/Capital-Bike-Share-/edit/main/README.md#exploratory-analysis)
    * [Features and model performance](https://github.com/10409/Capital-Bike-Share-/edit/main/README.md#exploratory-analysis)
  * [Supply and demand analysis](https://github.com/10409/Capital-Bike-Share-/edit/main/README.md#exploratory-analysis)
* [KPIs](https://github.com/10409/Capital-Bike-Share-/edit/main/README.md#timeseries---facebook-prophet)
* [Summary](https://github.com/10409/Capital-Bike-Share-/edit/main/README.md#building-a-flask-app)
* [Data sources](https://github.com/davidellavalle/Capital-Bikeshare/blob/main/README.md#data-sources)
* [Legal Terms](https://github.com/davidellavalle/Capital-Bikeshare/blob/main/README.md#legal-terms)

## Introduction

Micromobility in US shows big increase from 2010. Increasing population, and traffic in cities bikes are giving much more flexibility to people than cars. In 2019 the e-bikes, and scooters riders increased 60% more than 2018, and took 40 million trips on station-based bike share systems (pedal & e-bikes). The largest bike share systems in the bikesharing business are Bay Wheels, Biki, Capital Bikeshare, Citi Bike NYC, Divvy. Riders took 17% more trips on these systems than in 2018. 
 
> “The growth of bike share shows no signs of stopping.” NACTO, National Association of City Transportation Officials, reported in 2017

### Motivation
The aim of this project based on analyzing the data of the “Capital Bikeshare” empower their business. Based on Washington DC Capital bikeshare provides bikeshare system, with more than 4,300 bikes available at 500 stations. Bikes are available 24 hours a day, 7 days a week, 365 days a year.  We were asked firstly to provide some proofs of how and which features has an effect on demand of bikes and secondly measuring KPIs to ensure that one can accomplish the business objective. The **project challenges** include finding the right features correlated with the bike demand through proofs with visualization and machine learning, finding model fits the best to the dataset, and predicting business growth with time series analysis. 

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

### Growing ridership (LINK TO THE FILE)
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
##### Correlation Matrix 

Features of 'season', 'yr’, weather, ‘hr, mnth, 'temp',  'hum' 








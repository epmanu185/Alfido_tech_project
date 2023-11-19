# Alfido_tech_project

## Table of contents

1. [Project overview](#Project-overview)
2. [Data sources](#Data-sources)
3. [Tools used](#Tools-used)
4. [Data cleaning / preparation](#Data-cleaning-/-preparation)
5. [Exploratory Data Analysis](#Exploratory-Data-Analysis)
6. [Data analysis](#Data-analysis)
7. [Results / Findings](#Results-/-Findings)
8. [Recommendations](#Recommendations)
9. [Limitations](#Limitations)
10. [References](#References)

### Project overview

This data analysis project aims to provide insights into weather data (2012), Uber data & Inventory data. By analyzing various aspects of the weather data, Uber data & Inventory seperately, we seek to identify trends, make data-driven recommendations, and gain a deeper understanding of these factors.

### Data sources

The primary dataset used for this analysis are
 - Weather data: [kaggle weather](https://www.kaggle.com/datasets/bhanupratapbiswas/weather-data)
 - Uber data: [kaggle Uber](https://www.kaggle.com/datasets/bhanupratapbiswas/uber-data-analysis)
 - Inventory data: [kaggle inventory](https://www.kaggle.com/datasets/bhanupratapbiswas/inventory-analysis-case-study/data)


### Tools used

- EXCEL - For data cleaning. [Download here](https//:microsoft.com)
- SQL - For data analysing.
- Tableau - For creating reports.

### Data cleaning / preparation

In the initial data preparation phase, we performed the following tasks:
1. Data loading and inspection.
2. Handling missing values.
3. Data cleaning and formatting.

### Exploratory Data Analysis

EDA involved exploring the Weather data to answer key questions, such as:
1. **Weather data**
- What is the overall temperature trend?
- What is the precipitation pattern?
- What is the wind speed trend?
2. **Uber data (2016)**
- what is the most opted trip category and purpose?
- what are top 10 routes?
- which is the most opted route?
- which is the longest travelled route?
- which month has the most number of trips?

### Data analysis

Include some interesting codes or features worked with

**Weather data analysis**

- Temperature trend analysis


``` SQL
SELECT DATE(Date_Time)AS date,ROUND(AVG(Temp_C ),0)AS temp_in_degree_celcius
FROM `weather_datas.weather`
GROUP BY date
ORDER BY date ASC;
```

- precipitation pattern analysis

 ```SQL
SELECT weather,COUNT (Weather)AS weather_count
FROM `weather_datas.weather`
GROUP BY Weather
HAVING COUNT (Weather) >100
ORDER BY weather_count DESC;
```

- Windspeed analysis
  
```SQL
SELECT DATE(Date_Time)AS date,ROUND (AVG (Wind_Speed_km_h),0)AS windspeed_km_hr, ROUND(AVG(temp_C),0)AS temp_in_degree_celcius
FROM `weather_datas.weather`
GROUP BY date
ORDER BY date ASC;
```

**Uber data analysis**

**Inventory data analysis**

### Results / Findings

The analysis results are summarized as follows:
1. The company's sales have been steadily increasing over the past year, with a noticeable peak during the holiday season.
2. Product Category A is the best-performing category in terms of sales and revenue.
3. Customer segments with high lifetime value (LTV) should be targeted for marketing efforts.

### Recommendations

Based on the analysis, we recommend the following actions:
• Invest in marketing and promotions during peak sales seasons to maximize revenue.
• Focus on expanding and promoting products in Category A.
• Implement a customer segmentation strategy to target high-LTV customers effectively.

### Limitations

I had to remove all zero values from budget and revenue columns because they would have affected the accuracy of my conclusions from the analysis. There are still a few outliers even after the omissions but even then we can still see that there is a positive correlation between both budget and number of votes with revenue. 

### References

1. [kaggle.com](https//:kaggle.com)
   

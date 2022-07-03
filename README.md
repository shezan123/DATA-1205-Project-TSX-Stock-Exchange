# DATA-1205-Project-TSX-Stock-Exchange
## Introduction

In this study, we aim to analyze the performance of the Toronto Stock Exchange (GSPTSE) in the years 2019-2021. The market performance is analyzed based on the adjusted closing price and volume (Adjusted Closing Price Definition, 2022). We also included the covid-19 crisis factor in this analysis because of its significant effect on stock prices(Fontaine et al., 2020).The dataset 'finance-stocks canada.zip' had the following three files:
indexData.csv: Unprocessed data with 112457 entries and 2204 null values. 
indexProcessed.csv: Cleaner version of indexData.csv with all null values removed. On further investigation through python, it was found that Korean stock exchange(KS11) data was missing in this file. Leaving us with 104224 data points to analyze. 
indexinfo.csv: This file contained information about the countries, currencies and names of stock exchange indices.
Since we are not using KS11 data in our visualizations, we decided to go ahead with the indexProcessed.csv file for our analysis. Correspondingly, we joined the indexinfo file to the main file on the stock exchange indices using the join() function in python. Therefore, the combined file now had 13 columns. Furthermore, to aid our story around covid-19, an open dataset was obtained from the Health Canada website and connected to the original data through the tableau data source connector. 

## Visualizations
### Close(CAD) vs Date(Month)
The stock market data is a time series and must represent data plotted in continuous intervals(Knaflic,2015,p-45). This visualization aimed to make the user think about the trends and sudden falls and rises in market price over time. Gestalt principle of connection also suggested that we tend to believe physically connected objects as part of a group, and our chart leverages this principle(Knaflic,2015,p-80). We also added annotations to this graph, which helps us highlight the nuances in our story(Knaflic,2015,p-142)
### Volume vs Date(Month)
The idea of this chart was to represent the total number of stocks that changed hands over a month during this period. Vertical bar charts were considered for this visual because it helps the audience to compare the highest and lowest points very easily by comparing the endpoints of the bars(Knaflic,2015,p-50). Furthermore, we added colours to these bars based on whether the stock prices closed in a particular month were higher or lower than the open stock price. The red colour suggested that the open price was higher than the close, and the blue suggested otherwise. These colour combinations were chosen as a pre-attentive attribute to highlight the positive and negative associations(Knaflic,2015,p-121).

### Covid-19 cases vs Date(month)
This graph represents the gradual increase of covid-19 cases over 2020 and 2021. We chose a scatterplot because it allows us to encode data simultaneously on the x-axis and y-axis and represent the data's exponential behaviour (Knaflic,2015,p-44). Likewise, we leveraged an image of the covid-19 virus as the design shape of our plot to draw the audience's attention(Knaflic,2015,p-76). The pre-attentive attribute used for this chart is the size of the point. As the number of cases increases, the size of the virus increases, indicating the scale of data points (Knaflic,2015,p-116)
### Monthly Range table
This table represents the sum of highs, lows and range of stock market prices from 2020-to 2021. We used a table because we intend our audience to be able to see the monthly values and compare them. And also to communicate that one particular row of interest-March 2020 (Knaflic,2015,p-40). The pre-attentive attribute we chose for this visual is the heatmap colour scheme which draws the user's attention to the row of interest(Knaflic,2015,p-117)
### Forecast for 2022
This graphic shows the forecast of covid-19 cases and market value for 2022. Line graphs help us efficiently visualize the forecast by including the range of confidence intervals(Knaflic,2015,p-46)

### Story
We are attempting to tell a story based on how covid-19 cases and stock market value are inversely proportional. It began with the high performance of the stock market in January 2020 when the covid-19 cases were scarce. However, within four months,e in April 2020, the stock market plummeted to an all-time low in the last ten years. The market saw the highest fluctuation in March 2020. Further, from April to June 2020, the market prices did not fluctuate much, and covid-19 cases seemed to be under control. April 2020 to December 2020 saw a steep rise in covid-19 cases; however, it did not affect the stock prices significantly. In February 2021, the stock market prices broke their previous record of January 2020. But in March 2021, there was a substantial dip in the prices due to the exponential rise of covid-19 cases. The forecasting for the next few months suggests that the covid-19 cases will continue to increase, and the inverse relation might bring the prices down.In conclusion, we recommend the government of Canada to take measures to keep the rise of covid-19 cases under control in order to keep the stock prices floating.

![image](https://user-images.githubusercontent.com/90064609/177024638-006e9db4-0687-404b-a946-826b381b2574.png)



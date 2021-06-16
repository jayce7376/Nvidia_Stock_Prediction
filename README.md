# Nvidia_Stock_Prediction
![NVIDIA](images/nvidia_logo.jpg)
**Authors**: [Kibae Kim](mailto:rlqo7376@gmail.com)

Nvidia Corporation, an American multinational technology company designs graphics processing units (GPUs) for the gaming and professional markets, as well as system on a chip units (SoCs) for the mobile computing and automotive market. Its primary GPU line, labeled "GeForce", is in direct competition with the GPUs of the "Radeon" brand by Advanced Micro Devices (AMD)

## Business Problem
***
It is common in financial industry to use time series forecasting to track the price of a stock over time. This can be tracked in the short term, such as the price of a stock in one hour during a business day, or in the long term, such as the price of a stock on the last day of each month. Stock markets are very unpredictable and geopolitical changes can affect the stock trend of stocks in the stock market. Recently, we faced 2020 stock market crash, caused by Covid-19, that began on 20 February 2020 and ended on 7 April. Therefore, it is very difficult to perform reliable trend analysis on with previous time series forecasting.

2021 is called the year of cryptocurrency. Cryptocurrency is a digital currency that can be used to purchase goods and services, but it uses an online ledger with strong encryption to secure your online transactions. Much of the interest in these unregulated currencies is that speculators sometimes trade for profit to increase their prices. The popularity of cryptocurrency caused a shortage in the graphics card market. At the same time, it leads increasing of a grapic card supplier, Nvidia.

I want to build a reliable time series forecasting model that predict Nvidia's stock price after 2020 stock market crash. Therefore, this project aims to provide a updated time series forecasting for investment bankings to predict better Nvidia's future stock price.


## Overview
***
The data for the prediction was collected using [Yahoo Finance](https://finance.yahoo.com/) and [Statista](https://www.statista.com/statistics/274005/market-share-of-global-graphics-card-shipments-since-3rd-quarter-2010/) with support of pandas, numpy, and datetime library of Python. [Nvidia's closing stock price](https://finance.yahoo.com/quote/NVDA/history?p=NVDA) is main dependent variable which predicted in this project, and [AMD's previous day closing stock price](https://finance.yahoo.com/quote/AMD?p=AMD&.tsrc=fin-srch) and [Google trend data](https://trends.google.com/trends/explore?q=nvidia&geo=US) were chosen for exogenous variables. For time series forecasting model, ARIMA, ARIMA with exogenous variables, LSTM, and Prophet were tested on daily closing price of Nvidia.


## Modeling
***
We've tried 3 different models to build COVID-19 classification project. <br>

1. Densely Connected Network Model <br>
![Dense_CF](images/Densley_ConnectedNetwork_confusion_matrix.png)<br>
![Dense_ROC](images/Densely_Connected_Network_Model_ROC_curve.png)<br>

2. Baseline CNN Model <br>
![Base_CF](images/BaselineCNN_Model_confusion_matrix.png)<br>
![Base_ROC](images/BaselineCNN_Model_ROC_curve.png)<br>

3. Weighted CNN Model <br>
![Weighted_CF](images/Weighted_CNN_confusion_matrix.png)<br>
![Weighted_ROC](images/Weighted_CNN_ROC_curve.png)<br>

## Conclusion
***

1. We chose weighted CNN model because this model detect COVID-19 well and also detect normal well.
2. Our weighted CNN model can be useful as a method of COVID-19 detection for hospitals when they don’t have test kit.


## Ideas for Improvement
***
1. See if the model can differentiate COVID X-ray images from other lung disease X-ray images such as pneumonia.
2. See if we can develop new models to detect other diseases using X-ray images.

## Repository Structure

***

```
├── README.md                                      <- The high-level overview of this project
├── COVID19_Detection_project_presentation.pdf     <- PDF version of project presentation
├── COVID19_Detection_Project.ipynb                <- Final_Notebook used for the project
├── images                                         <- Sourced externally and visualizations generated from code
├── data                                           <- All the Image data files used for the notebook.
```

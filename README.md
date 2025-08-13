### Indian Food Price Forecasting: An Exploratory Analysis and Predictive Modelling Approach

#### **Project Overview**
This project aims to address the crucial issue of food price forecasting in India by providing a comprehensive exploratory data analysis (EDA) and developing a robust predictive modeling framework. Accurate food price predictions are vital for policymakers, consumers, and retailers to manage inflation and supply chain dynamics. The project uses a real-world dataset and employs various machine learning and deep learning models to uncover market intelligence and forecast future price trends.

#### **Dataset**
The analysis is based on the `wfp_food_prices_ind.csv` dataset, which contains 165,450 records and 14 features. The dataset includes information on:
* **Date**: The date of the observation.
* **Admin1** and **Admin2**: The first and second administrative divisions (state and district/city).
* **Market**: The specific market where the price was recorded.
* **Latitude** and **Longitude**: Geographical coordinates.
* **Category** and **Commodity**: The food item type and specific item.
* **Unit**: The unit of measurement (e.g., KG).
* **Price** and **USD Price**: The price in Indian Rupees (INR) and its USD equivalent.

#### **Methodology**
The project follows a systematic methodology consisting of three main phases:

1.  **Data Preprocessing**: The raw data was cleaned to ensure it was suitable for modeling. This involved standardizing column names, handling 581 missing values in `Admin1`, `Admin2`, `Latitude`, and `Longitude`, and normalizing inconsistent entries. Outliers were identified and removed using the Interquartile Range (IQR) method to enhance model robustness.

2.  **Exploratory Data Analysis (EDA)**: A variety of visualization techniques were used to explore data patterns. This included time series plots to observe price trends over time, heatmaps to investigate correlations between variables, and box plots to compare price ranges and variability across different food categories.

3.  **Predictive Modeling**: The pre-processed dataset was used to train and test a diverse set of predictive models, which were divided into two main categories:
    * **Traditional Models**: Support Vector Machines (SVM), Random Forest, and XGBoost were applied, with Random Forest and XGBoost showing robust performance for short-term predictions.
    * **Time-Series and Deep Learning Models**: ARIMA, Long Short-Term Memory (LSTM), Gated Recurrent Units (GRU), and a hybrid LSTM+GRU model were used to capture temporal dependencies and long-term trends.

#### **Key Findings**
The analysis revealed significant findings about food price dynamics in India:
* Strong seasonality and regional price differences exist across key food commodities.
* High correlations were found between market demand, seasonal trends, and price variations.
* The deep learning models (LSTM, GRU, and the hybrid LSTM+GRU) outperformed traditional models in capturing long-term sequential patterns and handling price volatility.
* The hybrid LSTM+GRU model delivered the most consistent and accurate results, making it the most suitable for real-world forecasting applications.

#### **Future Work**
Potential enhancements for this project include:
* **Real-time Data**: Integrating real-time data from sources like Agmarknet via APIs for live forecasting.
* **Geographic Expansion**: Incorporating more granular data at the state, district, or mandi level.
* **Macroeconomic Indicators**: Including external variables such as rainfall, fuel prices, and inflation to improve accuracy.
* **Advanced Models**: Implementing more sophisticated models like Transformer-based forecasting.
* **Model Deployment**: Creating a public-facing dashboard to visualize forecasts and trends.
* **Policy Simulation**: Using causal inference techniques to simulate the impact of government interventions on food prices.

This project provides a strong foundation for future work in food price forecasting and supports data-driven decision-making for stakeholders in the food supply chain.

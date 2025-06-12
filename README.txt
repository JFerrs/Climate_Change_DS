Analysis and Prediction of Global Sea Level Rise (1993-2023)

Exploring the relationship between CO2 emissions, global temperature, and sea level rise using linear regression models and advanced forecasting.



--Project Overview--

This project addresses the critical phenomenon of Global Mean Sea Level (GMSL) rise, a key indicator of climate change. Through the analysis of historical data, it seeks to understand the complex interactions between per capita CO2 emissions, global temperature anomalies, and GMSL. The primary objective is to develop and compare robust predictive models for sea level, offering short-to-medium term projections.


--Data Sources--

The data used for this analysis are annual time series spanning from 1993 to 2023:

- Global Temperature Anomalies: Global average temperature data (NASA GISS Surface Temperature Analysis - GISTEMP).
- Annual CO2 Emissions per capita: Data on carbon dioxide emissions per person (Our World in Data).
- Global Mean Sea Level (GMSL mean): Data on the global average sea level height (NASA Sea Level Change).


--Methodology and Approach--
The project follows a structured methodology:

1. Data cleaning, structuring, and visualization.
2. Calculation of correlation between variables to understand their temporal relationship.
3. Simple linear regression models:
	- Model for predicting temperature based on annual CO2 emissions.
	- Model for predicting sea level variation with respect to annual temperature variation.
	- Model for predicting sea level variation with respect to annual CO2 emissions.
4. Explanation of the models developed.
5. Time series model with Prophet.
6. Future prediction for the next 10 years using both the Prophet and linear regression models.

--Key Results and Conclusions--

The developed models demonstrated high predictive power for Global Mean Sea Level:

| Model                                                 | RMSE (mm) | R-squared |
| :---------------------------------------------------- | :-------- | :--------- |
| **Linear Regression (Temp & Year → GMSL)** | **2.371** | **0.913** |
| **Prophet (CO2 as regressor → GMSL)** | **2.740** | **0.884** |
| Linear Regression (CO2 & Year → Temp)                   | 0.158     | 0.963      |
| Linear Regression (CO2 & Year → GMSL)                   | 2.740     | 0.884      |

*Strong Correlation: An extremely high correlation was confirmed between global temperature anomaly and sea level ($r \approx 0.99$), highlighting temperature as a direct and powerful driver of sea level change.

*Linear Model Accuracy: The linear regression model using temperature anomaly and year as sea level predictors showed the most accurate performance on the test set, indicating a direct and robust relationship.

*Robust Prophet Model: The Prophet model also proved highly effective, with comparable performance in sea level prediction. Although slightly outperformed by linear regression in this particular case (possibly due to the high linearity of the temperature-GMSL relationship and the annual nature of the data), Prophet offers the advantage of detecting changepoints in the trend and provides uncertainty intervals, which are valuable for long-term forecasts.

*The Challenge of Multicollinearity: The presence of high correlation between CO2 emissions and the time factor (Year) in linear regression models illustrates how multicollinearity can affect the interpretation of individual coefficients, as observed in temperature prediction.

*Continued Projections: Both models predict a continued rise in Global Mean Sea Level over the next decade, solidifying historically observed trends.



--Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **scikit-learn**
* **Prophet**



--Detailed Technical Report--

For a more exhaustive description of the methodology, a deeper analysis of the results, discussion of limitations, and future work, please consult the complete project report:

**Climate Change DS Report.pdf**


--Contact

* Github: JFerrs 
* Email: jferresgarcia@gmail.com
* LinkedIn: https://www.linkedin.com/in/jferrs/


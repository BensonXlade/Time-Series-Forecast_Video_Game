# Time-Series-Forecast_Video_Game

![](https://i0.wp.com/workingcasual.com/wp-content/uploads/2024/02/PS5-Deep-Earth-DualSense.png?ssl=1)

Project Overview:
This project focuses on forecasting video game sales to help a leading video game developer and reseller align their inventory with fluctuating customer demand. The analysis addresses key business challenges, such as seasonal demand, market competition, and inventory costs, while leveraging advanced forecasting models to predict sales patterns accurately.

Business Problem:
The company faces significant challenges in managing inventory due to:
	•	Seasonal Demand: Sales spikes during holidays and game releases.
	•	Market Competition: Rapid shifts in customer preferences.
	•	Inventory Costs: High storage expenses and potential write-offs.
	•	Uncertainty: Variability in customer behaviour and external factors.

This project aims to build a robust forecasting solution to minimise these challenges and support strategic decision-making.

Data Description:
The dataset contains 264 rows and 8 features representing monthly video game sales from 2002 to 2023. Key attributes include:
	•	Monthly Sales: Total sales per month.
	•	Product Categories: Genres like RPG, FPS, and Sports.
	•	Platform: Platforms such as Xbox, PlayStation, and PC.
	•	Holiday & Promotion Indicators: Binary features to flag months with holidays or promotions.
	•	Day of the Week: Contextual information on sales trends.

Key Insights from Exploratory Data Analysis (EDA):
	1.	Sales Trends: Cumulative sales increased over time, with notable dips in 2008 and 2016.
	2.	Seasonality: Sales peaked during the holiday season (November–February).
	3.	Category and Platform Performance:
	•	Sports games and Xbox platforms performed the best.
	•	RPG games and PlayStation platforms had the lowest sales.
	4.	Holidays and Promotions:
	•	Overall sales were unaffected by holidays or promotions, but specific categories and platforms benefited.
	5.	Day-of-Week Patterns: Sales peaked on weekends, highlighting consumer shopping behaviour.

Methodology

Data Preparation:
	•	Stationarity Testing: ADF and KPSS tests confirmed stationarity of the data.
	•	Seasonality Analysis: Utilised ACF and PACF plots to identify seasonal patterns.
	•	Feature Engineering: Categorical features like holiday and promotion flags were used to enrich the dataset.

Models Used:
	1.	ARIMA (Auto-Regressive Integrated Moving Average):
	•	Best for capturing trends, seasonality, and noise.
	•	Model Order: (2, 1, 2) based on ACF and PACF.
	2.	ETS (Exponential Smoothing):
	•	Suitable for data with strong seasonal components.
	3.	FB Prophet:
	•	Robust to irregular time series data, leveraging external regressors like holidays.

Evaluation Metrics:
	•	RMSE (Root Mean Squared Error) and MAE (Mean Absolute Error) were used to compare model accuracy.
Best Model: ARIMA demonstrated the highest accuracy with the lowest RMSE and MAE values.

Forecast Results:
Using the ARIMA model, forecasted sales for January to April 2024 align with historical trends and seasonal patterns. These insights enable the company to optimise inventory and minimise costs.

Technologies and Tools:
	•	Programming: Python
	•	Libraries: pandas, statsmodels, cmdstanpy, matplotlib, seaborn, scikit-learn
	•	Visualization: Matplotlib, Seaborn
	•	Models: ARIMA, ETS, FB Prophet

How to Use:
	1.	Clone this repository:

git clone https://github.com/BensonXlade/Video-Game-Sales-Forecasting.git
cd Video-Game-Sales-Forecasting


	2.	Install dependencies:

pip install -r requirements.txt


	3.	Explore the data and EDA in notebooks/EDA.ipynb.
	4.	Train and evaluate forecasting models in notebooks/Model_Building.ipynb.
	5.	View final forecasts in results/sales_forecasts.csv.

Key Learnings
	•	ARIMA was identified as the most effective forecasting model for this dataset.
	•	Sales patterns exhibited strong seasonality, providing opportunities for targeted inventory strategies.
	•	Consumer behaviour insights, such as weekend sales peaks, can inform promotional campaigns.

Future Improvements
	•	Incorporate external factors (e.g., economic indicators) to enhance model accuracy.
	•	Test additional models, such as SARIMA and machine learning-based approaches.
	•	Develop a real-time forecasting dashboard for dynamic insights.

Contributors
	•	Abhulimhen Benson
	•	Kehinde Ogundana
	•	Felix Omomah

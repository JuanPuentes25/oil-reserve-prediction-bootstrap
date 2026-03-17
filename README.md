# oil-reserve-prediction-bootstrap
ML project to select the most profitable region for 200 oil wells. Uses Linear Regression to predict reserves and bootstrapping to assess profit and risk. Regions are compared based on expected profit and probability of loss (&lt;2.5%) to support data-driven decisions

🛢️ Oil Well Profit Prediction & Risk Analysis (ML Project)
📌 Project Overview

This project simulates a real-world machine learning task for an oil extraction company (OilyGiant) aiming to identify the most profitable region to develop 200 new oil wells.

Using Linear Regression and Bootstrapping, we:

Predict oil reserves for each well

Select the most promising wells

Estimate potential profits

Evaluate financial risk

🎯 Objective

Select the best region for oil well development based on:

Maximum expected profit

Risk of loss below 2.5%

📊 Dataset Description

Three datasets representing different regions:

geo_data_0.csv

geo_data_1.csv

geo_data_2.csv

Each dataset contains:

id: unique well identifier

f0, f1, f2: features (geological characteristics)

product: oil reserves (in thousands of barrels)

⚙️ Methodology
1. Data Preparation

Load and inspect datasets

Check for missing values and duplicates

2. Model Training

Split data: 75% training / 25% validation

Train a Linear Regression model

Predict reserves on validation set

3. Model Evaluation

Compute:

Mean predicted reserves

RMSE (Root Mean Squared Error)

4. Profit Calculation
Key assumptions:

Budget: $100 million for 200 wells

Revenue per unit: $4500

Break-even point: 111.1 thousand barrels per well

Steps:

Select top 200 wells based on predicted reserves

Compute total reserves

Estimate profit:

profit = (total_reserves * 4500) - 100_000_000
5. Risk Analysis (Bootstrapping)

Perform 1000 bootstrap samples

For each sample:

Select 500 wells randomly

Choose top 200 based on predictions

Compute profit

Metrics:

Average profit

95% confidence interval

Risk of loss (%)

📈 Results Summary
Region	Avg Profit	Risk of Loss	Decision
Region 0	...	...	❌
Region 1	...	...	✅
Region 2	...	...	❌

👉 Final selection is based on:

Risk < 2.5%

Highest average profit among valid regions

🧠 Key Insights

High predicted reserves ≠ low risk

Bootstrapping is essential for realistic uncertainty estimation

Some regions may look profitable but carry unacceptable risk

🛠️ Tech Stack

Python

Pandas

NumPy

Scikit-learn

Matplotlib / Seaborn

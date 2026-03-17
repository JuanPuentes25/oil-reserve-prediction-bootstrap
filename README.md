# oil-reserve-prediction-bootstrap
ML project to select the most profitable region for 200 oil wells. Uses Linear Regression to predict reserves and bootstrapping to assess profit and risk. Regions are compared based on expected profit and probability of loss (&lt;2.5%) to support data-driven decisions

Oil Well Profit Prediction & Risk Analysis

Overview

This project predicts the most profitable regions for oil well development using machine learning and evaluates investment risk through bootstrapping techniques. By analyzing synthetic geological data from multiple regions, the model estimates oil reserve volumes, selects the top wells, and calculates expected profits and financial risk.

Project Objectives
General Objective

Identify the most profitable regions for oil well development by predicting reserve volumes using Linear Regression and evaluating investment risk with bootstrapping.

Specific Objectives

Preprocess and explore geological datasets to ensure data quality and readiness for modeling.

Develop a Linear Regression model to predict oil reserve volumes.

Select the top 200 wells per region based on predicted reserves and estimate potential profits.

Perform bootstrapping to quantify profit variability, compute confidence intervals, and assess the risk of loss.

Compare regions based on expected profit and investment risk to recommend the optimal region for well development.

Visualize predicted volumes, profit distributions, and risk metrics for clear communication of results.

Dataset

Synthetic geological datasets of oil wells in three regions: geo_data_0.csv, geo_data_1.csv, geo_data_2.csv

Each dataset contains 100,000 wells with the following columns:

id — unique well identifier

f0, f1, f2 — geological features

product — volume of oil reserves (in thousands of barrels)

The datasets contain no missing or duplicate values and are ready for analysis.

Methodology

Data Exploration & Preprocessing

Load datasets with Pandas

Verify data integrity

Prepare features and targets for modeling

Model Training

Linear Regression model for predicting reserve volumes

Train-validation split (75:25)

Compute RMSE and average predicted volume

Profit Calculation

Select top 200 wells per region based on predicted reserves

Calculate revenue and profit using REVENUE_PER_UNIT = $4,500 and a budget of $100,000,000

Bootstrapping Analysis

Sample 500 wells with replacement 1,000 times

Calculate distribution of profits, 95% confidence intervals, and probability of loss

Identify the safest and most profitable region

Key Results

Region 1 is the safest and most profitable option:

Average profit: ~$5.15M

Risk of loss: 1%

Regions 0 and 2 have slightly lower expected profits (~$4.3–4.4M) but higher risk (~6%).

Bootstrapping confirms Region 1 as the optimal choice, balancing high expected profit with low investment risk.

Technologies & Tools

Python 3.11

Pandas & NumPy for data handling

Scikit-learn for Linear Regression and metrics

Matplotlib / Seaborn for visualization

Pathlib for project file management

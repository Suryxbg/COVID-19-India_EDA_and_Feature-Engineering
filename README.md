# COVID-19-India_EDA_and_Feature-Engineering

## Objective
The objective of this project is to analyze COVID-19 data across Indian states to uncover patterns, evaluate the impact of the pandemic, and generate meaningful insights. By performing EDA and feature engineering, the project aims to highlight state-wise comparisons, identify trends, and support decision-making through clear visualizations.

## Dataset Used
- <a href= "https://github.com/Suryxbg/COVID-19-India_EDA_and_Feature-Engineering/blob/main/covid_19_india.csv">Covid_dataset

## Key Questions (KPIs)

- Which states reported the highest confirmed, active, recovered, and death cases?
- How does the recovery rate and case fatality rate vary across states?
- What is the trend of active cases relative to confirmed and recovered cases?
- Which states contribute most to the national COVID-19 burden?
- How does test positivity rate compare across states?

## Process

- Data Collection & Loading
  - The dataset used is the COVID-19 India dataset containing state-wise data on confirmed, cured, deaths, and active cases.
  - Data was loaded into a Pandas DataFrame for cleaning, transformation, and analysis.

- Data Cleaning
  - Removed duplicates and handled missing values.
  - Standardized inconsistent state names (e.g., Telengana → Telangana, Orissa → Odisha).
  - Converted date columns into proper datetime format.
  - Aggregated duplicate state entries to ensure one record per state per date.

- Feature Engineering
  - Created new attributes to derive more meaningful insights:
    - Active Cases = Confirmed – (Cured + Deaths)
    - Case Fatality Rate (CFR) = (Deaths / Confirmed) × 100
    - Recovery Rate = (Cured / Confirmed) × 100
    - Test Positivity Rate (TPR) = (Confirmed / Tests Conducted) × 100 (if testing data available)
  - Generated cumulative sums for each state to analyze long-term trends.
  - Derived daily new cases (Confirmed, Recovered, Deaths) to capture growth dynamics.

- Exploratory Data Analysis
  - Univariate Analysis: Examined the distribution of confirmed, recovered, deaths, and active cases.
  - Bivariate Analysis: Compared confirmed vs recovered, confirmed vs deaths, active vs CFR.
  - Multivariate Analysis: Used scatter and bubble plots to show relationships among multiple variables.
  - State-level Analysis: Identified top 5–10 states contributing most to confirmed, active, and death cases.

- Visualization & Dashboarding
  - Used matplotlib and seaborn to create:
    - Bar charts, horizontal bars, stacked bars for ranking and comparisons.
    - Pie charts to visualize proportional contributions of top states.
    - Scatter plots and bubble charts for correlations and multi-dimensional analysis.
    - Line charts to capture trends of fatality and recovery rates.
  - Combined multiple plots into a dashboard-style layout (2x3 format) for easy comparison.

- Insights Generation
  - Interpreted results from charts and metrics to highlight states with highest burden, best/worst recovery, and alarming fatality rates.
  - Summarized observations into actionable insights.


## Dashboard

- Bar chart of top states by confirmed cases.
- Horizontal bar chart of top states by active cases.
- Stacked bar chart comparing cured vs deaths.
- Pie chart of top 5 states by confirmed share.
- Scatter plot of active cases vs fatality rate.
- Line chart of case fatality rates across states.

<img width="1986" height="1189" alt="Covid_image" src="https://github.com/user-attachments/assets/99a507ad-2e2f-48fc-842b-8da98d5d934a" />

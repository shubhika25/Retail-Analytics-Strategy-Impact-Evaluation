# Retail-Analytics-Strategy-Impact-Evaluation


Retail Analytics & Strategy Impact Evaluation

Customer Insights + Power BI Dashboard + Trial–Control Uplift Modeling

This project delivers a full end-to-end retail analytics pipeline combining customer behaviour analysis, product-level insights, and experimental strategy evaluation. It includes an interactive Power BI dashboard and a Python-based uplift modeling framework using Trial vs Control store comparison.

 Project Highlights
1. Customer & Sales Analytics (Power BI)

Developed a Power BI dashboard with:

Dynamic slicers for Year → Quarter → Month

Customer segmentation by Lifestage and Premium Customer (Budget/Mainstream/Premium)

Sales trends (daily/weekly/monthly)

Brand-level performance

Units-per-customer & Avg Price per Unit

Revenue Contibution

<img width="1418" height="793" alt="image" src="https://github.com/user-attachments/assets/dce7e0c3-20cf-40b5-9689-be16b6f140b5" />
<br>
<img width="1418" height="797" alt="image" src="https://github.com/user-attachments/assets/45c0ab52-37b3-4f2b-94fd-f94edd607cdb" />


2. Data Exploration & Customer Insights

Key analyses performed:

Identification of top-selling brands

Contribution of Premium / Budget / Mainstream customers

Sales concentration by Lifestage segments

Purchase behaviour differences:

Units per customer

Price per unit

Basket size trends

Weekly and monthly sales seasonality patterns

3. Strategy Experiment – Trial vs Control Store Analysis

An A/B-style experiment was conducted to evaluate the impact of a new retail strategy.

Steps : 
a. Pre-trial Comparison

Selected a control store with similar historical sales behaviour

Calculated pre-trial sales totals

Measured pre-trial % deviation

b. Scaling the Control Store

Since stores vary in size, the control store sales were scaled using:

scaling_factor = trial_pre_sales / control_pre_sales


This created a synthetic control comparable to the trial store.

c. Uplift Estimation

For each month:

% deviation = |trial - scaled_control| / scaled_control

d. Variability Measurement

Standard deviation of pre-trial % difference was used to determine natural store-to-store variation.

e. 95% Confidence Interval Construction
Upper CI = scaled_control * (1 + 2 × std_dev)
Lower CI = scaled_control * (1 - 2 × std_dev)

f. Visual Impact Evaluation

A time-series plot was generated showing:

Trial store sales

Scaled control store sales

Upper & Lower 95% CI bands

Grey shaded trial period

If trial sales exceeded the upper CI, the strategy showed statistically significant uplift.

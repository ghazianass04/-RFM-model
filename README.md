# Online Retail Customer Segmentation using RFM Analysis

## Overview

This project analyzes online retail transaction data to understand customer purchasing behavior and segment customers based on their value and engagement.

The analysis uses **RFM (Recency, Frequency, Monetary Value) analysis** to identify different customer groups, such as **VIP/Loyal, Potential Loyalists, At Risk, Can't Lose, and Lost customers**.

## Objectives

* Clean and preprocess the retail transaction dataset.
* Calculate customer-level **Recency, Frequency, and Monetary Value**.
* Assign RFM scores using quantile-based scoring.
* Segment customers according to their RFM scores.
* Visualize customer distribution across different segments.
* Analyze the characteristics and relationships of VIP/Loyal customers.

## Methodology

1. **Data Preparation**

   * Removed records with missing `CustomerID`.
   * Converted `InvoiceDate` to datetime format.
   * Created a `TotalAmount` feature using `Quantity × UnitPrice`.

2. **RFM Analysis**

   * **Recency:** Number of days since the customer's last purchase.
   * **Frequency:** Number of transactions made by the customer.
   * **Monetary Value:** Total amount spent by the customer.

3. **RFM Scoring**

   * Customers were scored from **1 to 4** for each RFM dimension.
   * Higher scores represent better customer engagement and value, except for Recency, where a lower number of days results in a higher score.

4. **Customer Segmentation**

   * Combined RFM scores into an overall `RFM_score`.
   * Customers were classified into value-based segments:

     * Low-Value
     * Mid-Value
     * High-Value
   * Additional behavioral segments were created, including:

     * VIP/Loyal
     * Potential Loyalist
     * At Risk Customers
     * Can't Lose
     * Lost

5. **Visualization**

   * Customer distribution by RFM segment.
   * Treemap of customer segments.
   * Box plots for VIP/Loyal customers.
   * Correlation heatmap of Recency, Frequency, and Monetary Value.

## Technologies

* Python
* Pandas
* Plotly
* Jupyter Notebook

## Key Skills Demonstrated

* Data Cleaning & Preprocessing
* Exploratory Data Analysis (EDA)
* Feature Engineering
* Customer Segmentation
* RFM Analysis
* Data Visualization
* Business-oriented Data Analysis

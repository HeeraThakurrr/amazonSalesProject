# Amazon Sales Data Analysis

## Project Overview
This project involves a comprehensive **Exploratory Data Analysis (EDA)** of Amazon sales data. The goal is to derive actionable business insights regarding order trends, product popularity, fulfillment methods, and customer geography. The analysis focuses on data cleaning, processing, and summarizing key metrics using Python.

## Dataset Description
The dataset contains **128,975 records** and **23 columns**. It includes transactional data such as:
* **Order Details:** Order ID, Date, Status, Amount.
* **Product Details:** SKU, Category, Size, Style.
* **Fulfillment:** Ship Service Level, Fulfilled By, Courier Status.
* **Customer Location:** Ship City, Ship State, Ship Country.

## Tech Stack
* **Language:** Python
* **Libraries:** Pandas
* **Environment:** Jupyter Notebook

## Data Cleaning & Preparation
Before analysis, the raw data underwent significant preprocessing:
1.  **Handling Null Values:**
    * Dropped the empty `Unnamed: 22` column.
    * Filled missing `Amount` values with `0`.
    * Filled missing `Courier Status` with "Unshipped".
    * Dropped rows with missing city/state locations.
2.  **Data Type Conversion:**
    * Converted the `Date` column to datetime format to extract monthly trends.

## Key Insights

### 1. Sales Performance
* **Top Month:** April was the highest-performing month with **~28.8 Million** in revenue, followed by May (**~26.2M**) and June (**~23.4M**).
* **March Anomaly:** March shows significantly lower data points (171 orders), likely indicating partial data availability for that month.

### 2. Product Analysis
* **Top Categories:** "Set" and "Kurta" are the dominant categories, accounting for the vast majority of orders.
* **Revenue Drivers:** The "Set" category generates the highest revenue (~39M), followed by "Kurta" (~21M) and "Western Dress" (~11M).
* **Size Preferences:** M, L, and XL are the most popular sizes among customers.

### 3. Fulfillment & Logistics
* **Fulfillment Authority:** **Amazon** fulfills significantly more orders (approx. 70%) compared to Merchant fulfillment.
* **Service Level:** The majority of orders use **Expedited** shipping (~88k orders) over Standard shipping (~40k orders).

### 4. Geography
* **Top States:** The highest number of orders originate from **Maharashtra** and **Karnataka**, followed by Telangana and Uttar Pradesh.

### 5. Customer Type
* **B2B vs B2C:** The platform is overwhelmingly **B2C** (Business to Consumer), with B2B transactions making up less than 1% of the total orders.

## Future Improvements
* **Visualization:** Integrate `Matplotlib` or `Seaborn` to visualize sales trends and geographic heatmaps.
* **Code Optimization:** Refactor the monthly analysis sections into reusable functions to reduce code repetition.
* **Statistical Modeling:** Implement forecasting to predict sales for future months.

## How to Run
1.  Clone the repository.
2.  Install the required libraries:
    ```bash
    pip install pandas
    ```
3.  Load the `Amazon Sale Report.csv` file into the project directory.
4.  Run the `main.ipynb` (or `Amazon_Sales_EDA.ipynb`) file.

# LogiScale Supply Chain Analytics — Week 1

## Project Overview

This project focuses on building a robust data ingestion and preprocessing pipeline for a large-scale supply chain dataset using PySpark. The primary objective of Week 1 was to transform raw, unstructured logistics data into a clean and analysis-ready format that can support advanced analytics in subsequent stages.

The dataset represents real-world supply chain operations, including order transactions, shipping timelines, product performance, and customer segmentation. Handling such data requires careful validation, cleaning, and transformation to ensure accuracy and usability.

---

## Dataset Description

The dataset used in this project is sourced from Kaggle:

**DataCo Smart Supply Chain Dataset for Big Data Analysis**
https://www.kaggle.com/datasets/shashwatwork/dataco-smart-supply-chain-for-big-data-analysis

It contains over 180,000 records capturing detailed supply chain activities, including:

* Order information (Order ID, Order Date)
* Shipping details (Shipping Mode, Delivery Status, Delivery Timelines)
* Customer and market segmentation
* Product-level metrics (Sales, Profit, Quantity)
* Delivery performance indicators (Delay duration, Late delivery risk)

Due to its size, the dataset is not included in this repository. It can be downloaded directly from the link above.

---

## Tools and Technologies

* PySpark for distributed data processing
* Python for scripting and transformations
* Pandas for benchmarking and comparison
* Jupyter Notebook for development and execution

---

## Key Tasks Performed

### Data Ingestion

The raw CSV dataset was loaded into a PySpark DataFrame to enable scalable processing. Schema validation and structure checks were performed to ensure correct interpretation.

### Benchmarking (Pandas vs PySpark)

A performance comparison between Pandas and PySpark was conducted. While Pandas handled the dataset reasonably, PySpark demonstrated better scalability and efficiency for larger data operations.

### Data Quality Assessment

A detailed audit identified missing values and inconsistencies across columns. Null counts and percentage distributions were calculated to evaluate data quality.

### Data Cleaning and Transformation

Several preprocessing steps were applied:

* Removed canceled and invalid transactions
* Filtered records with missing critical values
* Converted date fields into proper formats
* Derived new features such as delay days and time-based attributes (year, month, quarter)
* Cast columns into appropriate data types

### Data Preparation for Analysis

Sensitive customer-related fields were removed to ensure privacy. The dataset was then structured into a clean format suitable for further analysis.

---

## Output

The processed dataset was exported as:

final_output.csv

This cleaned dataset serves as the input for Week 2 (Big Data Processing and Analytics).

---

## Key Observations

* A significant portion of orders experienced delivery delays, indicating operational inefficiencies
* The raw dataset contained inconsistencies such as null values and mixed formats
* PySpark provided better scalability compared to Pandas for large datasets

---

## Learning Outcomes

* Practical experience in handling large-scale datasets using PySpark
* Strong understanding of data cleaning and preprocessing workflows
* Insight into performance differences between Pandas and distributed systems
* Ability to build a structured data pipeline for analytics

---





# LogiScale Supply Chain Analytics — Week 2

## Project Overview

Week 2 of the LogiScale project focuses on transforming the cleaned dataset from Week 1 into meaningful business insights using PySpark. The objective was to move beyond data preparation and perform large-scale analytical computations to understand operational efficiency, delivery performance, and profitability across the supply chain.

This stage emphasizes real-world analytical thinking by applying aggregations, window functions, and anomaly detection techniques on a large dataset.

---

## Dataset

The dataset used in this phase is derived from the cleaned output of Week 1 and originally sourced from Kaggle:

DataCo Smart Supply Chain Dataset for Big Data Analysis
https://www.kaggle.com/datasets/shashwatwork/dataco-smart-supply-chain-for-big-data-analysis

The working dataset contains over 170,000 processed records and includes key attributes such as:

* Order Region, Market, Shipping Mode
* Sales, Profit, Quantity
* Delivery delay metrics and risk indicators
* Time-based attributes (year, month, quarter)

This dataset enables analysis of logistics efficiency and business performance at scale.

---

## Tools and Technologies

* PySpark for distributed data processing and analysis
* Python for implementation
* Pandas for exporting results
* Jupyter Notebook for execution

---

## Key Analysis Performed

### Route Efficiency Analysis

Evaluated shipping performance across regions by analyzing average delay, late shipment percentage, and shipment volume. This helps identify underperforming logistics regions.

### Shipping Mode Performance

Compared different shipping methods based on delivery time, delay patterns, risk percentage, and profitability. This analysis highlights which shipping modes are most efficient and cost-effective.

### Time-Based Trend Analysis

Used PySpark window functions to calculate running totals and identify revenue trends over time. Monthly aggregations provided insight into business growth and seasonal patterns.

### Anomaly Detection

Applied Z-score based analysis to detect abnormal delivery delays across regions. This helps identify unusual operational disruptions or inefficiencies.

### Profit Margin Analysis

Analyzed profitability across customer segments, product categories, and markets. This provided a clear understanding of high-performing and underperforming business areas.

---

## Output

The analysis results were exported as structured CSV files for further visualization and reporting:

```text
outputs/agg_route_efficiency.csv
outputs/agg_shipping_mode.csv
outputs/agg_monthly_trends.csv
outputs/agg_profit_margin.csv
outputs/agg_anomalies.csv
```

These outputs represent aggregated insights and are designed to be directly used in dashboarding tools such as Power BI or Tableau.

---

## Key Insights

* A significant percentage of shipments experienced delays, indicating inefficiencies in logistics operations
* Certain shipping modes consistently underperformed in terms of delivery time and reliability
* Regional disparities in delivery performance highlight areas requiring operational improvement
* Profitability varies across customer segments and product categories, suggesting opportunities for optimization
* Anomaly detection revealed irregular delay patterns that may indicate deeper systemic issues

---

## Learning Outcomes

* Applied PySpark for large-scale analytical computations
* Gained experience with grouping, aggregation, and window functions
* Understood how to convert raw data into business insights
* Learned anomaly detection techniques using statistical methods
* Built a data-driven approach to evaluating operational performance

---



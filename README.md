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


 LogiScale Control Tower – End-to-End Logistics Analytics Pipeline Week - 03
 
📊 Overview

This project presents an end-to-end data analytics pipeline built to analyze logistics and supply chain performance. It combines data cleaning, big data processing, and visualization to deliver actionable insights for operational efficiency.

The final output is an interactive Power BI dashboard supported by an automated data pipeline using PySpark and Pandas.

🎯 Objective

The goal of this project is to:

Analyze shipment delays across regions
Identify high-performing and underperforming logistics zones
Track shipment volumes and trends
Provide decision-ready insights through a dashboard
🏗️ Project Architecture
Raw Data → Data Cleaning → PySpark Processing → Aggregation → Power BI Dashboard → Automation
📅 Weekly Breakdown
🔹 Week 1 – Data Cleaning & Preparation
Cleaned raw dataset
Handled missing values
Removed irrelevant records
Output: final_output.csv
🔹 Week 2 – Big Data Processing (PySpark)
Created new features (delay_days)
Aggregated:
Average delay by region
Total shipments
Monthly trends
Output:
agg_route_efficiency.csv
agg_monthly_trends.csv
🔹 Week 3 – Data Visualization (Power BI)
Built interactive dashboard
KPI Cards:
Average Delay
Total Shipments
Best Performing Region
Charts:
Route Efficiency (Delay by Region)
Shipment Volume
Added insights and slicers
🔹 Week 4 – Automation & Final Pipeline
Integrated full pipeline using PySpark + Pandas
Added forecasting using rolling averages
Generated executive summary
Automated data export for dashboard refresh
🛠️ Tools & Technologies
Python
PySpark
Pandas
Power BI
Excel
Windows Task Scheduler (Automation)
📂 Key Files
File	Description
week1_environment_ingestion.py	Data cleaning
week2_big_data_processing.py	PySpark aggregation
week4_final_pipeline.py	Final automated pipeline
final_output.csv	Cleaned dataset
final_route_efficiency.csv	Dashboard input
final_monthly_trends.csv	Trend analysis
📈 Key Insights
Certain regions consistently show higher delivery delays
High shipment volume areas often correlate with inefficiencies
Some regions demonstrate optimized logistics performance
Data-driven decisions can significantly improve route efficiency
🚀 How to Run
Install dependencies:
pip install pandas pyspark
Update dataset path:
CSV_PATH = "your_path/final_output.csv"
Run pipeline:
python week4_final_pipeline.py
Refresh Power BI dashboard with updated CSV outputs
📊 Dashboard

The dashboard provides a centralized view of logistics performance, enabling quick identification of operational bottlenecks and opportunities for optimization.

💡 Learnings
Hands-on experience with big data processing using PySpark
Building end-to-end data pipelines
Creating business-focused dashboards
Translating raw data into actionable insights
📌 Conclusion

This project demonstrates how raw logistics data can be transformed into meaningful insights through a structured analytics pipeline. It reflects practical skills in data engineering, analysis, and visualization.



Week 4 – Final Pipeline & Automation
LogiScale Control Tower Project
📊 Overview

Week 4 focuses on integrating the entire data pipeline into a single automated workflow. This stage connects data cleaning, processing, and analysis into a unified system that generates final outputs and insights for decision-making.

The pipeline ensures that updated data can be processed and reflected in the dashboard with minimal manual effort.

🎯 Objective
Build a complete end-to-end data pipeline
Automate data processing and output generation
Generate executive-level insights
Prepare final datasets for dashboard integration
🏗️ Pipeline Flow
Cleaned Data (Week 1)
        ↓
PySpark Processing (Week 2)
        ↓
Aggregation & Feature Engineering
        ↓
Pandas Conversion & Forecasting
        ↓
Final Output Files
        ↓
Power BI Dashboard (Week 3)
🛠️ Tools & Technologies
PySpark – Data processing and aggregation
Pandas – Data transformation and forecasting
Python – Pipeline scripting
Power BI – Dashboard visualization
OS Module – File handling and automation
🔧 Key Components
1. Data Loading
Loads cleaned dataset (final_output.csv)
Uses PySpark for scalable processing
2. Data Cleaning & Filtering
Removes cancelled shipments
Handles missing values (important columns only)
3. Feature Engineering
Creates delay_days column
Extracts:
order_year
order_month
4. Aggregation
Route efficiency:
Average delay per region
Total shipments
Monthly trends:
Units sold
Revenue
5. Forecasting
Uses rolling average (3-month window)
Predicts short-term demand trends
6. Data Export
Generates final CSV files:
final_route_efficiency.csv
final_monthly_trends.csv
7. Executive Summary

Automatically identifies:

Region with highest delay
Best performing region
Total shipments
📂 Output Files
File	Description
final_route_efficiency.csv	Region-level performance
final_monthly_trends.csv	Monthly trends + forecast
⚙️ How to Run
Install dependencies:
pip install pandas pyspark
Update file path in script:
CSV_PATH = r"C:\path\to\final_output.csv"
Run the pipeline:
python week4_final_pipeline.py
🔄 Automation

This pipeline can be automated using Windows Task Scheduler:

Schedule script execution daily/weekly
Automatically refresh output datasets
Ensure Power BI dashboard stays updated
📈 Key Insights Generated
Identification of high-delay regions
Detection of efficient logistics zones
Shipment distribution trends
Forecasted demand patterns
💡 Key Learnings
Building an end-to-end data pipeline
Integrating PySpark with Pandas
Automating data workflows
Translating data into business insights
🏁 Conclusion

Week 4 completes the LogiScale project by transforming individual components into a fully functional and automated analytics pipeline. It demonstrates practical skills in data engineering, analysis, and real-world business problem solving.



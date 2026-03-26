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




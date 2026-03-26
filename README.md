# LogiScale Supply Chain Analytics — Week 1

## Project Overview

This project focuses on building a robust data ingestion and preprocessing pipeline for a large-scale supply chain dataset using PySpark. The primary objective of Week 1 was to transform raw, unstructured logistics data into a clean and analysis-ready format that can support advanced analytics in subsequent stages.

The dataset represents real-world supply chain operations, including order transactions, shipping timelines, product performance, and customer segmentation. Handling such a dataset requires careful data validation, cleaning, and transformation to ensure accuracy and usability.

---

## Dataset Description

The dataset used in this project contains over 180,000 records capturing detailed supply chain activities. It includes multiple dimensions of business operations such as:

* Order information (Order ID, Order Date)
* Shipping details (Shipping Mode, Delivery Status, Delivery Timelines)
* Customer and market segmentation
* Product-level metrics (Sales, Profit, Quantity)
* Delivery performance indicators (Delay duration, Late delivery risk)

This dataset provides a strong foundation for analyzing operational efficiency, delivery performance, and profitability across different regions and customer segments.

---

## Tools and Technologies

* PySpark for distributed data processing
* Python for scripting and transformations
* Pandas for performance benchmarking
* Jupyter Notebook for development and execution

---

## Key Tasks Performed

### Data Ingestion

The raw CSV dataset was loaded into a PySpark DataFrame to enable scalable processing. Schema validation and data structure checks were performed to ensure the dataset was correctly interpreted.

### Benchmarking (Pandas vs PySpark)

A comparative analysis was conducted between Pandas and PySpark to evaluate performance differences. While Pandas handled the dataset reasonably, PySpark demonstrated better scalability and efficiency, especially for aggregation operations on larger datasets.

### Data Quality Assessment

A detailed audit was performed to identify missing values and inconsistencies across columns. Null counts and percentage distributions were calculated to understand the extent of data quality issues.

### Data Cleaning and Transformation

Several preprocessing steps were applied to improve data quality:

* Removed canceled and invalid transactions
* Filtered out records with missing critical values
* Converted string-based date fields into proper date formats
* Derived new features such as delay in shipping and time-based attributes (year, month, quarter)
* Cast numerical columns into appropriate data types for accurate computation

### Data Preparation for Analysis

Sensitive customer-related fields were removed to ensure data privacy. The dataset was then structured into a clean format suitable for analytical processing in the next phase.

---

## Output

The processed dataset was exported as:

final_output.csv

This cleaned dataset will be used as the input for Week 2, where advanced analytics and business insights will be generated.

---

## Key Observations

* A significant portion of orders experienced delivery delays, indicating potential inefficiencies in the logistics process
* The raw dataset contained inconsistencies such as null values and mixed data formats, requiring structured preprocessing
* PySpark proved to be more efficient than Pandas for handling larger datasets and performing aggregations

---

## Learning Outcomes

* Gained practical experience in handling large-scale datasets using PySpark
* Developed a structured approach to data cleaning and preprocessing
* Understood the importance of data quality in analytics workflows
* Learned the performance differences between single-machine and distributed data processing tools

---




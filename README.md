# Walmart Stock Analysis Using PySpark and Databricks

## Project Overview

This project explores historical Walmart (WMT) stock market data using Apache Spark and PySpark within the Databricks environment.

The analysis demonstrates how distributed data processing techniques can be applied to financial time-series data to explore stock price movements, trading volumes, and relationships between financial variables.

The project uses both the PySpark DataFrame API and Spark SQL to perform data exploration, transformations, statistical analysis, and temporal aggregations.

## Project Objectives

The main objectives of this project are to:

1. Load and explore historical Walmart stock market data using PySpark.
2. Examine the dataset structure, schema, and data types.
3. Calculate descriptive statistics for stock prices and trading volumes.
4. Perform DataFrame transformations and derive new financial metrics.
5. Investigate the relationship between stock prices and trading volumes.
6. Analyze annual and monthly stock market trends.
7. Apply Spark SQL queries to extract meaningful insights.

## Technologies Used

| Technology | Purpose |
|---|---|
| Python | Programming language |
| Apache Spark | Distributed data processing framework |
| PySpark | Python API for Apache Spark |
| Databricks | Cloud-based analytics and notebook environment |
| Spark SQL | SQL-based data analysis |
| Jupyter Notebook | Notebook format for code and documentation |
| Git & GitHub | Version control and project documentation |

## Dataset Description

The project uses `walmart_stock.csv`, containing historical Walmart stock market data.

**Dataset characteristics:**

- Company: Walmart Inc. (WMT)
- Frequency: Daily trading records
- Starting period: January 2012
- Number of observations: 1,258
- Number of columns: 7

### Dataset Features

| Column | Description |
|---|---|
| Date | Trading date |
| Open | Opening stock price |
| High | Highest stock price during the trading day |
| Low | Lowest stock price during the trading day |
| Close | Closing stock price |
| Volume | Number of shares traded |
| Adj Close | Adjusted closing price accounting for corporate actions |

## Project Methodology

### 1. Spark Environment Initialization

The analysis was performed in Databricks using Apache Spark.

The Walmart stock dataset was loaded into a Spark DataFrame, and its schema was examined to understand the available features and data types.

### 2. Exploratory Data Analysis

Initial data exploration included:

- Displaying the first five records.
- Counting the total number of observations.
- Inspecting column names and data types.
- Examining the dataset structure.

### 3. Descriptive Statistical Analysis

Descriptive statistics were calculated for the following variables:

- High
- Low
- Close
- Volume

The analysis included minimum, maximum, and average values, with particular attention to the average closing stock price.

### 4. DataFrame Transformations

PySpark DataFrame operations were used to create derived features and perform analytical transformations.

A new financial metric, the High-to-Volume ratio, was calculated as:

**HV Ratio = High / Volume**

Additional operations identified the trading day with the highest recorded stock price and calculated the Pearson correlation coefficient between High and Volume.

### 5. Temporal Analysis

Date-based transformations were performed to extract year and month information.

The analysis examined:

- Average closing stock price by year.
- Maximum trading volume by month.
- Changes in trading activity across different periods.

### 6. Spark SQL Analysis

Spark SQL was used to perform queries on a temporary view of the Walmart stock dataset.

Queries included:

- Retrieving the first five records.
- Identifying the month with the highest average trading volume.
- Finding the highest recorded closing stock price.

This demonstrated how the DataFrame API and SQL can be used to analyze the same dataset.

## Key Findings

The completed notebook examines the following analytical questions:

**Stock Price Performance:** What were the average and maximum stock prices during the observation period?

**Trading Activity:** Which month experienced the highest average trading volume?

**Price–Volume Relationship:** What does the Pearson correlation coefficient reveal about the relationship between daily high stock prices and trading volume?

**Temporal Trends:** How did average closing prices and trading activity change across the dataset?

Detailed numerical results and interpretations are provided in the analysis notebook.

## Repository Structure

```text
Walmart-Stock-Analysis-PySpark/
│
├── data/
│   └── walmart_stock.csv
│
├── notebooks/
│   └── Walmart_Stock_Analysis_PySpark.ipynb
│
├── .gitignore
│
└── README.md
```

## Running the Project

The project was developed and executed using Databricks.

To reproduce the analysis:

1. Open a Databricks workspace.
2. Import the notebook from the `notebooks/` directory.
3. Upload `walmart_stock.csv` from the `data/` directory.
4. Configure the notebook's dataset path to match the uploaded file location.
5. Attach the notebook to an available compute environment.
6. Execute the notebook cells sequentially.

The analysis requires an environment with PySpark and Spark SQL support.

## Conclusion

This project demonstrates the practical application of Apache Spark and PySpark to financial time-series analysis.

Through DataFrame operations, statistical calculations, temporal aggregations, and Spark SQL queries, the project illustrates how structured financial data can be processed and analyzed within a scalable analytics environment.

The techniques demonstrated provide a foundation for more advanced data engineering, financial analytics, and large-scale time-series processing.

## Acknowledgments

This project was developed as part of the **Big Data and Energy Data Analysis** course in the MSc Sustainable Energy Future program at ECE Engineering School.

The lab activity was provided by Sarah Malaeb, with educational material referencing Jose Portilla and Pierian Training.

## Author

GitHub: [@damisar](https://github.com/damisar)

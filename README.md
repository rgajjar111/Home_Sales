# Home_Sales
This document outlines the steps for setting up a Spark environment, loading data, executing Spark SQL queries, and comparing the performance of queries with and without caching.

## Setting up Spark Environment:

Identify the desired Spark version from the official Apache Spark website.
Set the spark_version variable to the desired version.
Install Spark and Java dependencies using the provided code snippet.
Importing Necessary Packages:

## Import required packages such as SparkSession and time.

### Loading Data:
Read data from an AWS S3 bucket into a DataFrame.
Create a temporary view of the DataFrame for SQL querying.

### Executing Spark SQL Queries:
Execute various SQL queries on the loaded DataFrame.
Calculate average prices for houses with specific criteria.

### Performance Comparison:
Measure the runtime of a query filtering out view ratings with average prices greater than or equal to $350,000.
Compare runtime with and without caching the DataFrame.

### Partitioning and Parquet Data:
Partition the DataFrame by the date_built field and write it to Parquet format.
Read the Parquet formatted data and create a temporary table for it.
Execute the same query as before on the Parquet DataFrame and measure its runtime.

### Uncaching DataFrame:
Uncache the temporary table to release cached memory.

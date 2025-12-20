# Data Pipeline for Marketing Analytics – Databricks MVP

This repository contains a minimum viable data engineering project developed as part of a postgraduate course in Data Science and Analytics, with a focus on Data Engineering.
The project was also designed to serve as a portfolio piece, demonstrating practical skills in data modeling, SQL, and cloud-based data pipelines.

For a more detailed description of the work, please refer to [Report - Data Engineering MVP](WIP)

### Project Overview

The objective of this project is to build a cloud-based data pipeline and a simulated data warehouse using Databricks, following a Bronze / Silver / Gold architecture and a star schema design.

The data represents a hypothetical food retail company, and the pipeline supports descriptive analytical questions related to:
* Customer behavior
* Promotional campaign effectiveness
* Product performance
* Purchase channels

### Repository Structure
Also stored in this folder are all of the notebooks utilized in the construction of this data pipeline. Executing them in order should produce the same results reported in the pdf document.
(WIP)
Data Engineering
  Scripts

### Dataset

The dataset was originally released on GitHub by the iFood Brain Team for hiring purposes and was later shared on Kaggle.

[Link](https://github.com/nailson/ifood-data-business-analyst-test)

Format: CSV

Size: 2,240 customers

### Business Questions 
The following are the business questions we hope to address with this work:

#####a)	Which features of the customer base are the most significant is maximizing expenditure?
Naturally, a company’s primary objective is to increase revenue. Therefore, the first question posed to the data concerns which customer characteristics are most relevant to higher spending levels. Since most of these features are categorical (textual), customers can be grouped by category and compared based on their average spending.

#####b)	Which features of the customer base are most relevant to the effectiveness of promotional campaigns?
In a similar vein, the same customer features can be analyzed to ascertain the impact of the promotional campaigns featured in the data.

#####c)	Which are the best performing products?
We take a brake from investigating the customer data to focus on the different product categories. It is prudent to understand from the data which products are the ones that bring about the most revenue to the company.
#####d)	Which is the most popular method of purchasing?
The last question pertains to the different channels of purchase available. Understanding which channels generate the highest revenue is essential for strategic decision-making.

### Architecture
The data pipeline is structured around medallion layers:

##### Bronze Layer

Raw ingestion of the original CSV file. Stored as a Delta table without transformations

##### Silver Layer

Data cleaning and normalization

Star schema modeling

Fact and dimension tables

##### Gold Layer

Aggregated, analysis-ready tables

Focused on business metrics and descriptive insights

### Data Model (Star Schema)

#####Fact Table

- FACT_Sales: quantitative measures such as spending by product category and purchase counts

#####Dimension Tables

- DIM_Customer: demographic and household attributes

- DIM_Promo: promotional campaign responses

- DIM_Calendar: time-related attributes based on customer enrollment date

This structure allows flexible slicing and aggregation for analytical queries.

### Final Notes

This project reflects practical decision-making under realistic constraints and aims to demonstrate:

Solid dimensional modeling

Correct use of Delta tables

Clear analytical thinking

Ability to translate business questions into data structures

Feel free to explore the notebooks or adapt the structure for similar analytical use cases.
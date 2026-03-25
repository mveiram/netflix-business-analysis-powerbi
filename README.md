# 📊 Netflix-business-analysis-powerbi
This project simulates a real-world business scenario for a streaming platform similar to Netflix. The objective is to analyze content distribution and derive insights to support strategic decisions regarding content investment.  The analysis focuses on identifying which types of content (by genre, country, and format)
## 🎯 Business Problem

### Streaming platforms invest heavily in content production and acquisition. However, not all content generates the same level of value.

#### 🎯 This project aims to answer key questions such as:

Which type of content (Movies vs TV Shows) delivers more value?


What genres are most prominent and potentially impactful?


Which countries contribute the most to the platform’s catalog?


How has content availability evolved over time?

## 📂 Dataset

Source: Kaggle

Records: 8,809 titles

Format: CSV


## 🧹 Data Cleaning & Preparation

The dataset was processed using Power BI (Power Query) to ensure data quality and usability.

Key steps:

### Removed irrelevant columns:


description (unstructured text not used in analysis)
cast and director (not aligned with current business questions)
show_id (technical identifier with no analytical value)


### Handled missing values:
Standardized null values in relevant fields (e.g., country)


### Data type transformations:
Converted date_added to date format
Extracted year and month for time-based analysis
Feature engineering:
Cleaned and structured duration field for analysis

### The dataset was processed using Power BI (Power Query) to ensure data quality and usability.

## 📊 Data Model

The dataset was structured to support analysis across the following dimensions:

Content type (Movie / TV Show)

Genre

Country

Time (year/month added)

Duration

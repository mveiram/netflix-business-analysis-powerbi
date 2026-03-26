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


## 🧹 Data Cleaning & Preparation (ETL)

The dataset was processed using Power BI (Power Query) to ensure data quality and usability.

Key steps:

### 🔧 Removed irrelevant columns:


description (unstructured text not used in analysis)
cast and director (not aligned with current business questions)
show_id (technical identifier with no analytical value)


### 🔧 Handled missing values:
Standardized null values in relevant fields (e.g., country)

Country Column Normalization
Detected multiple countries within single records (e.g., "USA, UK").

Standardized the column by extracting the primary country (first value before delimiter).

Trimmed extra spaces and ensured consistency.


### 🔧 Data type transformations:
Converted date_added to date format

Extracted temporal features from date_added:

year_added

month_added

month_name

### 🔧 Duration Column Normalization

The original duration column contained mixed formats:

"90 min" (Movies)

"2 Seasons" (TV Shows)

Created structured fields:

duration_value (numeric)

duration_type (categorical: min / season)

Cleaned and standardized values:
Converted all text to lowercase, Unified "Seasons" and "Season" into "season" and  removed inconsistent and invalid records.

Handling Inconsistent Data

Identified and removed anomalous values in duration_type that did not match expected categories.
Eliminated null values in critical fields where necessary.

Preserved original date_added column for full time-based analysis.

### The dataset was processed using Power BI (Power Query) to ensure data quality and usability.

## 📊 Data Model

The dataset was structured to support analysis across the following dimensions:

Content type (Movie / TV Show)

Genre

Country

Time (year/month added)

Duration

# University Ranking Analysis

## Team Members
- Abdulkrem Al Shammari
- Ghada Mohammed 
- Mamdouh Alsharari
- Abdullah Alhokbani
- Adel Albaqmi

---

## Introduction

### Problem:
Understanding how various factors, such as employment rankings, research rankings, and others, influence a university's overall ranking is essential for both universities and policymakers. This project aims to analyze these factors and identify the most significant contributors to a university�s overall global standing. Furthermore, it seeks to determine which countries consistently have a high concentration of top-ranked universities globally.

### Objectives:


1. Investigate Which universities are ranked in the top 10 globally
2. Investigate Which universities are ranked in the top 10 for employment outcomes
3. Identify What positions do universities in Saudi Arabia hold within the global rankings?
4.  Determine which factors (e.g., **research rankings**, **employment rankings**) and others, most significantly impact a university�s **overall ranking**.
5. Investigate the correlation between **national** and **global** university rankings.
6. Identify countries with a high concentration of **top-ranked universities**.
---

## Dataset Overview

The dataset is sourced from three primary university ranking systems:
- **Times Higher Education (THE)**
- **Shanghai Ranking**
- **Center for World University Rankings (CWUR)**

It contains data on national rankings, global rankings, research rankings, employment rankings, and other relevant performance metrics.

---

 
 # Exploratory Data Analysis (EDA) Process

## 1. **Data Profiling**

   ### 1.1 **Descriptive Analysis**:
   - Performed a descriptive statistical summary (mean, median, standard deviation, variance) for all key columns such as overall ranking, research ranking, and employment ranking. This provided insights into the central tendencies and spread of the data.

   ### 1.2 **Data Quality Checks**:
   - **Reliability**: the data source does not mentioned any source of datasets which make them unreliable
   - **Timeliness**: There is no period of interest for the analysis nor up to date data, Not specified (Updated a year ago)
   - **Consistency**: each of dataset has its own format and values due their criteria of evaluating universities.
   - **Relevance**: Evaluated if all the features in the dataset are relevant to the analysis of university rankings and performance.
   - **Uniqueness**: Checked for duplicate entries in the dataset to ensure that each university is represented only once.
   - **Completeness**: Assessed missing data patterns and documented the completeness of important features like national and global rankings.
   - **Check Accuracy**: 

---

## 2. **Data Cleaning**

   ### 2.1 **Handling Missing Values**:
   - Handled missing data by applying appropriate imputation values.

   ### 2.2 **Correcting Errors**:
   - Cleaned and standardized inconsistent text values in columns like World Rank. Removed irrelevant characters (e.g., `+`, `�`) from numerical columns and converted them into the correct data types (`int` or `float`).

   ### 2.3 **Dealing with Outliers**:
   - Identified and handled outliers in ranking-related columns using domain knowledge and statistical methods. Outliers were assessed based on extreme rankings or unusual score patterns.

---

## 3. **Univariate Analysis**

   - Performed univariate analysis on individual variables to assess their distribution and trends.
   - **Visualizations**: Used histograms and box plots to understand the distribution of global and national rankings, as well as research and employment rankings.
   
---

## 4. **Bivariate/Multivariate Analysis**

   - Conducted bivariate and multivariate analysis to explore relationships between different variables.
   - **Correlation Matrix**: Generated a correlation matrix to identify the strength of relationships between rankings (e.g., global rank vs. national rank).
   - **Country Analysis**: Grouped data by country to identify nations with the highest concentration of top-ranked universities and visualized the findings using bar charts.

---

## Key Insights

### 1. ** Top 10 Globally Ranked Universities**
   - **Insight**: The top 10 universities globally are differ across ranking systems.


### 2. **Research Ranking as the Most Significant Factor**
   - **Insight**: Research ranking has the strongest influence on a university�s overall ranking.

### 3. **Top Universities are Concentrated in the US and UK**
   - **Insight**: US and UK are the highest number of globally top-ranked universities.
  

### 4. **Correlation Between National and Global Rankings**
   - **Insight**: National ranking moderately impacts the overall ranking but is less influential than research rankings.


### 5. **Research-Intensive Countries Lead the Rankings**
   - **Insight**: Countries like the US, UK,  lead global university rankings due to strong research output.
  

### 6. **negative Correlation Between Employment and Research Rankings**
   - **Insight**: There is minimal correlation between employment and research rankings.


# Usecase-3-Project-2

## Project Overview
This project aims to analyze world university rankings using the dataset from Kaggle. We will address key problem statements related to global and national university rankings and their factors.

### Problem Statements
The project answers the following problem statements question:

1. **Top 10 Global Universities**: Which universities are ranked in the top 10 globally?
2. **Top 10 Employment Outcomes**: Which universities are ranked in the top 10 for employment outcomes?
3. **Saudi Arabian Universities**: What positions do universities in Saudi Arabia hold within the global rankings?
4. **Impact of Various Factors**: Considering various factors such as employment rankings, research rankings, and others, which has the most significant impact on a university's overall ranking?
5. **Correlation Between Rankings**: Is there a correlation between national and global university rankings? Based on this information, can you recommend a country that has a high concentration of top-ranked universities?

## Steps to Complete the Project:

### Step 1: Defining the Problem Statement

We have outlined specific questions that will guide our analysis and research throughout the project.


### Step 2: Collecting Data

This is the most important step because you can't complete your work without data. The project uses specific datasets collected from the [Kaggle website](https://www.kaggle.com/datasets/ourfuture/world-university-rankings).

*About Dataset*: The dataset contains universities' world and national rankings and also employability and education rankings and other features we will recognize later.


### Step 3: Exploratory Data Analysis
In this step, we will conduct an exploratory analysis to uncover patterns, trends, and insights.



#### Key Aspects of EDA:
**1. Data Profiling:**
- **Descriptive** Analysis is a statistical method used to summarize and describe the main features of a dataset



**Viewing the dataframe**
```python
print(f"Shanghai Ranking DataFrame shape: {shanghai_rank.shape}")
print(f"Times Higher Education DataFrame shape: {times_h.shape}")
print(f"World Rank University DataFrame shape: {word_rank.shape}")
```
```markdown
Shanghai Ranking DataFrame shape: (1000, 6)
Times Higher Education DataFrame shape: (1591, 20)
World Rank University DataFrame shape: (2000, 9)
```
As we see the highest number of rows exists in *World Rank University* dataset and that describes this dataset as more than comprehensive the other datasets.

**Statistics and information** 
```python
print("World Rank University information:-\n")
word_rank.info() # Information about the dataframe
word_rank.describe(include=['object']) # Object columns description
```
```markdown
World Rank University information:-

<class 'pandas.core.frame.DataFrame'>
RangeIndex: 2000 entries, 0 to 1999
Data columns (total 9 columns):
 #   Column              Non-Null Count  Dtype  
---  ------              --------------  -----  
 0   World Rank          2000 non-null   object 
 1   University Names    2000 non-null   object 
 2   Location            2000 non-null   object 
 3   National Rank       2000 non-null   int64  
 4   Educational Rank    2000 non-null   object 
 5   Employability Rank  2000 non-null   object 
 6   Faculty Rank        2000 non-null   object 
 7   Research Rank       2000 non-null   object 
 8   Score               2000 non-null   float64
dtypes: float64(1), int64(1), object(7)
memory usage: 140.8+ KB
```

|           | World Rank      | University Names                               | Location | Educational Rank | Employability Rank | Faculty Rank | Research Rank |
|-----------|-----------------|------------------------------------------------|----------|------------------|-------------------|--------------|----------------|
| count     | 2000            | 2000                                           | 2000     | 2000             | 2000              | 2000         | 2000           |
| unique    | 2000            | 2000                                           | 95       | 439              | 1030              | 262          | 1935           |
| top       | 1Top 0.1%      | Harvard University\nCWUR Rating System: Ed... | USA      | -                | -                 | -            | -              |
| freq      | 1               | 1                                             | 332      | 1562             | 967               | 1727         | 66             |

From this table, we can figure out many things: 
1. World Rank contains a string so we need to deal with it and convert it to int.
2. The USA appears most frequently, indicating a concentration of top-ranked universities.
3. There is no duplication in University Names column so that is good.
4. Educational Rank - Research Rank the most duplication is a dash "-", so that indicates columns contain null values.


- **Check Data Quality Dimensions** are attributes that help assess the quality of data in a dataset. Evaluating these dimensions ensures that the data is fit for its intended purpose.
Evaluating these dimensions ensures that the data is fit for its intended purpose. Here are the key dimensions of data quality:
1. Reliability
2. Timeliness
3. Consistency
4. Relevance
5. Uniqueness
6. Completeness
7. Check Accuracy

The process includes:
- Validating the appropriateness of data types for the dataset.
- Identifying outliers using established validation rule


**2. Data Cleaning:**
- Handling missing values
- Correcting errors.
- Dealing with outliers.

                               
### Step 4: Communicating Results

The analysis is structured around five primary questions: identifying the top 10 global universities, examining employment outcomes, investigating the rankings of Saudi Arabian universities, assessing the impact of various ranking factors, and exploring the correlation between national and global rankings. Through this systematic approach, we aim to provide actionable insights for universities, policymakers, and prospective students.

The findings from this analysis will be presented using both univariate and multivariate techniques, offering a detailed understanding of the data. 

#### 1- Univariate Analysis:
- Q1: Which universities are ranked in the top 10 globally?

![The top universitites in World Ranking University](https://github.com/Faris35/Usecase-3-Project-2/blob/main/top_unviersity.png)

- Q2: What positions do universities in Saudi Arabia hold within the global rankings?

```python

for ind in df_ksa.index:
    print(f'University Names:{df_ksa['University Names'][ind]} -- World Rank:{df_ksa['World Rank'][ind]}')
    print("")

```

```markdown

University Names:King Abdulaziz University -- World Rank:245

University Names:King Abdullah University of Science and Technology -- World Rank:279

University Names:King Saud University -- World Rank:352

University Names:King Fahd University of Petroleum and Minerals -- World Rank:657

University Names:King Saud bin Abdulaziz University for Health Sciences -- World Rank:1311

University Names:King Khalid University -- World Rank:1447

University Names:Taif University -- World Rank:1509

University Names:Imam Abdulrahman Bin Faisal University -- World Rank:1547

University Names:Taibah University -- World Rank:1586

University Names:Prince Sattam Bin Abdulaziz University -- World Rank:1711

University Names:Umm Al-Qura University -- World Rank:1742

University Names:Alfaisal University -- World Rank:1762

University Names:Jazan University -- World Rank:1811

University Names:Qassim University -- World Rank:1907

University Names:University of Tabuk -- World Rank:1974

University Names:King Faisal University -- World Rank:1979
```

- Q3: Countries With The Highest Number of Universities At The Top 500

![](https://github.com/Faris35/Usecase-3-Project-2/blob/main/top_500.png)

#### 2- Multivariate Analysis:
- Q4: Which universities are ranked in the top 10 for employment outcomes?

![Top 10 Employment Outcomes](https://github.com/Faris35/Usecase-3-Project-2/blob/main/empl_rank.png)

- Q5: Considering various factors such as employment rankings, research rankings, and others, which has the most significant impact on a university's overall ranking?
![Top 10 Employment Outcomes](https://github.com/Faris35/Usecase-3-Project-2/blob/main/corr_with_another_factors.png)

**Insights:**
  
Research Rank has the strongest impact on World Rank. The very high correlation (0.897) indicates that research quality is a dominant factor in determining a university’s overall ranking.
Score and World Rank (-0.916): This strong negative correlation indicates that as the score increases, the world rank tends to decrease.
Educational Rank and Faculty Rank also influence the World Rank, but their impact is moderate. These factors likely affect a university’s reputation, but not as much as research.
Employability Rank has the weakest relationship with World Rank. While employability is important, it seems to play a smaller role in global university rankings compared to academic factors like research.
National Rank has a moderate positive correlation with World Rank, meaning that a university’s performance at the national level influences its global position, but not as much as research or education

- Relationship Between World Rank and Score

 ![Relationship Between World Rank and Score](https://github.com/Faris35/Usecase-3-Project-2/blob/main/scatter.png)

- Q6 Is there a correlation between national and global university rankings?

![Global and National](https://github.com/Faris35/Usecase-3-Project-2/blob/main/globa_national.png)


### Contributors:
- Faris
- Ahood
- Sarah
- Kawthar
- Abdulrahman

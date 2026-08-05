# predicting-imdb-ratings
Predicting Movie Success with Machine Learning

**View the Interactive Report:** https://ryleewang23.github.io/predicting-imdb-ratings/ 

# Image of ROC Curve
<img width="2100" height="1800" alt="roc_curves" src="https://github.com/user-attachments/assets/32d42711-f9de-4732-8266-c318189cbc5f" />

# Predicting Highly Rated IMDb Movies
A machine learning project built in R that predicts whether a movie will receive a **high IMDb rating (7.0 or above)** using movie metadata.

## Project Overview
This project explores whether characteristics such as a movie's **runtime, release decade, genre, international title coverage, and crew information** can be used to predict if a movie will receive a high IMDb rating.

Using a sample of IMDb movie data, I built and compared two classification models:
- Logistic Regression
- Decision Tree

The goal was to practice the complete machine learning workflow, from data cleaning and feature engineering to model evaluation and interpretation.

## Research Question
**Can movie metadata predict whether a movie receives an IMDb rating of 7.0 or higher?**

## Dataset
This project uses a sampled IMDb dataset consisting of four tables:
- `title.basics`
- `title.ratings`
- `title.akas`
- `title.crew`

The datasets were merged using relational joins to create a single movie-level dataset for analysis.

## Data Preparation
The analysis included:
- Cleaning missing values
- Joining multiple IMDb datasets
- Creating a binary target variable:
  - **High Rating:** IMDb rating ≥ 7.0
  - **Not High Rating:** IMDb rating < 7.0
- Engineering new features including:
  - Release decade
  - Primary genre
  - Number of international titles
  - Number of represented regions
  - Director availability
  - Writer availability

## Machine Learning Models
Two supervised classification models were trained:

**Logistic Regression**
Used as the baseline model for predicting whether a movie receives a high IMDb rating.

**Decision Tree**
Provides an interpretable model that identifies the most important decision rules used for classification.

## Model Evaluation
The models were evaluated using:
- Accuracy
- Balanced Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC
- Confusion Matrix
- 5-Fold Cross Validation

## Visualizations
The project includes several visualizations, including:
- Rating Distribution
- High Ratings by Genre
- International Coverage vs. Rating
- Model Comparison
- ROC Curves
- Confusion Matrices
- Decision Tree Visualization

## Technologies
- R
- tidyverse
- tidymodels
- ggplot2
- rpart
- rpart.plot
- R Markdown

## How to Run
Prerequisites
- R (version 4.5 or later)
- RStudio
- Required packages:
  - tidyverse
  - tidymodels
  - rpart.plot
  - readr

Install the required packages:
```r
install.packages(c(
  "tidyverse",
  "tidymodels",
  "rpart.plot",
  "readr"
))
```
**Note:**
This project uses a **course-provided sample of the IMDb Non-Commercial Datasets**.

Because the sample data is not included in this repository, place the following files into the `data/` folder before running the analysis:

- `title.basics.csv`
- `title.akas.csv`
- `title.crew.csv`
- `title.ratings.tsv`

The sample datasets used for this project are not distributed with this repository. If you are recreating this project, you can generate a similar sample using the official IMDb Non-Commercial Datasets here: **https://datasets.imdbws.com/** 

### Running the Project

1. Clone this repository.
2. Open "predicting.imdb.ratings.Rproj" in RStudio.
3. Place the required data files in the "data" folder.
4. Open "analysis.Rmd".
5. Run the code chunks or click **Knit** to generate the HTML report.

## Key Takeaways
This project demonstrates a complete machine learning workflow in R, including:
- Data cleaning
- Feature engineering
- Relational joins
- Exploratory data analysis
- Classification modeling
- Model evaluation
- Cross-validation
- Data visualization

## Author
**Rylee Wang**
Data Science Student  
University of California, Davis

Interested in machine learning, data analytics, and building AI-powered applications.

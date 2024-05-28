# Movies-data-processing
# Movie Dataset Analysis

## Introduction

This project focuses on analyzing a movie dataset to derive insights into the characteristics of movies such as genre, director, actors, and audience engagement. We perform data cleaning and exploratory data analysis to uncover patterns and trends in the movie industry.

## Dataset

The dataset (`movies.csv`) contains information about various movies, including their titles, genres, directors, actors, release years, and audience engagement metrics.

## Unique Steps

1. **Data Cleaning:**
   - Explored the dataset's structure using `.info()` and `.head()` to understand its contents.
   - Removed columns such as `Gross` and `RunTime` that were not relevant for analysis.
   - Handled missing values by dropping rows with null values.
   - Stripped whitespace and unwanted characters from string columns (`GENRE`, `ONE-LINE`, `STARS`, `YEAR`, `Director`, `Actor`).
   - Split the `GENRE` column into multiple genre columns (`Genre1`, `Genre2`, `Genre3`) based on comma separation.
   - Split the `STARS` column into `Director` and `Actor` columns based on pipe (|) separation.
   - Cleaned up director and actor names by removing unnecessary prefixes such as "Director:" and "Stars:".
   - Converted audience engagement metric `VOTES` to integer type after removing commas.

2. **Exploratory Data Analysis (EDA):**
   - Investigated the distribution and summary statistics of numerical features such as `VOTES`.
   - Explored the frequency of movie genres using `value_counts()` on columns `GENRE`, `Genre1`, `Genre2`, and `Genre3`.
   - Analyzed the diversity of directors using `describe()` on the `Director` column.

## Results

- The dataset contains a diverse range of movie genres, with certain genres being more prevalent than others.
- Directors and actors exhibit varying levels of involvement across movies, with some being more prolific than others.
- Audience engagement, measured by the number of votes, varies widely across movies, suggesting differences in popularity and reception.

## Future Directions

- Perform sentiment analysis on user reviews or ratings to gauge audience sentiment towards movies.
- Explore correlations between movie attributes such as genre, director, and actor, and audience engagement metrics.
- Build predictive models to forecast audience engagement or box office success based on movie features.

## Dependencies

- pandas

## How to Use

1. Clone the repository.
2. Install pandas using `pip install pandas`.
3. Run the Jupyter Notebook or Python script to replicate the data cleaning and analysis steps.
4. Explore the dataset further and derive additional insights based on specific research questions or hypotheses.

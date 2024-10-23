# Narrative Revelation and Book Popularity: Analyzing Information Revelation in English Fiction

## Project Overview
This project aims to investigate the relationship between the information revelation, measured through Kullback-Leibler divergence (KLD), and the popularity of English-language fiction books. The analysis utilizes book metadata, KLD scores, and control variables to explore how narrative structures influence reader engagement, as reflected in download counts. The analysis covers multiple genres and includes an exploration of which variables predict book popularity.

## Objective

The primary objective of the project was to:
* Develop book-level measures of KLD characteristics (e.g., average, variance, slope) for each book.
* Examine the relationship between KLD measures and the log-transformed download counts to assess book popularity.
* Investigate genre-specific heterogeneity in the impact of KLD measures using OLS and LASSO regressions.

## Methodology

**1. Data Sources:**
* Metadata: Includes book-level attributes and download counts from Project Gutenberg.
* KLD Scores: Measures the amount of information revelation across narrative sections for each book, in the form of Python lists.

**2. Feature Engineering:**
* Constructed book-level characteristics for KLD, such as average KLD, variance, slope, skewness, and kurtosis.
* Added control variables like word count, sentiment scores, and genre indicators.

**3. Regression Analysis:**
* Regressed KLD measures and control variables against the log-transformed download counts.
* Performed OLS regression to examine the relationship between KLD measures and book popularity.
* Conducted LASSO regression to infer which variables are most independently predictive of log-downloads.

**4. Genre-Specific Analysis:**
* Conducted separate regressions for different genres to explore how KLD measures influence book popularity across genres.

## Results

* **KLD Measures:** Books with balanced and less variable topic distributions (lower variance in KLD) tend to have higher downloads. The slope of KLD was found to negatively affect popularity in genres like romance, indicating a preference for more consistent thematic development.
* **Word Count:** Longer books are generally associated with higher popularity across several genres.
* **Sentiment:** Higher average sentiment (more positive tone) was negatively correlated with downloads, especially in genres like science fiction and horror.
* **Genre-Specific Insights:**

  * Science Fiction: Sentiment and word count were significant predictors of book popularity.
  * Romance: A steeper slope in KLD was negatively correlated with popularity.

* **LASSO Regression:** Identified word count, sentiment average, speed, and specific genres (e.g., science fiction, fantasy, horror) as significant predictors of book popularity.


## Key Insights

* **Predictive Factors:** Word count and genre are among the strongest predictors of book popularity, while the slope and variability of information revelation play a nuanced role depending on the genre.
* **Genre-Specific Trends:** Different genres show varying relationships between narrative structure and popularity, highlighting the importance of tailoring analysis to genre-specific preferences.

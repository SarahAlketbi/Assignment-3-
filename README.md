
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1Buk0DJzgzc805ktkCM3SxBgwplq3CUeu#scrollTo=OJ13ywg1jJQ5)


# Activity 3: Air Quality Analysis in NYC
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1Buk0DJzgzc805ktkCM3SxBgwplq3CUeu#scrollTo=OJ13ywg1jJQ5)


##  Project Description

This Assignment is part of the Data Science coursework and involves analyzing hyperlocal air quality data collected by low-cost sensors mounted on moving vehicles across New York City (NYC).  
The main goal is to apply statistical techniques learned in the chapters on **Sampling and Empirical Distributions**, **Testing Hypotheses**, and **Estimation**.

The data is preprocessed to join air quality sensor readings with NYC neighborhood boundaries using geospatial operations.

##  Objectives

- Randomly sample the data and analyze empirical distributions.
- Estimate median pm10 levels using bootstrapping and construct 95% confidence intervals.
- Perform hypothesis testing on the population mean of pm10 levels.
- Analyze neighborhood-specific pollution levels and bootstrap the mean for the top 3 polluted neighborhoods.

##  Dataset Description

- **NYC_PM.csv**  
  Attributes: `SensorID`, `time`, `temperature`, `humidity`, `pm25`, `pm1`, `pm10`, `longitude`, `latitude`
  - Focus attributes: `temperature`, `humidity`, `pm1`, `pm25`, `pm10`

- **nyc_polygon.geojson**  
  Polygons representing administrative boundaries (neighborhoods) in NYC.

##  How to Run

1. Open the notebook `Activity3_questions.ipynb`.
2. Click the **"Open in Colab"** button at the top, or upload it manually to Google Colab.
3. Install required libraries if needed (`datascience`, `geopandas`, `pandas`, `matplotlib`).
4. Run the cells sequentially to:
   - Preprocess the data (join CSV and GeoJSON files).
   - Perform sampling, bootstrapping, and statistical analysis.
   - Generate visualizations for distributions and confidence intervals.

##  Key Methods and Techniques Used

- `datascience.Table` abstraction for all data handling.
- Random sampling without replacement (10% of data).
- Bootstrap resampling (500–5000 repetitions) for confidence interval estimation.
- Empirical histograms using `Table.hist`.
- Hypothesis testing using confidence intervals.
- Geospatial operations using `geopandas` for preprocessing.

##  Visualizations

- Empirical histograms of sampled and full datasets.
- Histogram of bootstrapped medians with 95% CI.
- Histogram of bootstrapped means for the top 3 neighborhoods with 95% CIs.

##  Important Notes

- **Extreme pm10 values (>300 µg/m³)** were removed before analysis as instructed.
- **Datascience Table abstraction** (not Pandas DataFrames) was used throughout the project.
- **500 bootstraps** were sometimes used for faster performance when necessary (acceptable for educational assignments).
- Confidence intervals were calculated using the **2.5th and 97.5th percentiles**.



##  Open in Colab


[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1Buk0DJzgzc805ktkCM3SxBgwplq3CUeu#scrollTo=OJ13ywg1jJQ5)


---

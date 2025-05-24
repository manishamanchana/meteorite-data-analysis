# Geospatial and Temporal Analysis of Global Meteorite Landings Using Clustering and Statistical Modeling

## Overview

This project performs **geospatial and temporal analysis** of global meteorite landings using clustering, statistical modeling, and exploratory data analysis. It aims to uncover hidden patterns in the spatial distribution and mass of meteorites and analyze temporal trends to understand the influence of improved detection over time.

---

## Objective

To determine whether meteorite landings occur randomly or exhibit regional and mass-based patterns, and how these patterns evolve over time.

---

## Dataset

**Source:** [NASA Meteorite Landings Dataset (Kaggle)](https://www.kaggle.com/datasets/nasa/meteorite-landings)

- ~45,000 records
- Fields include: name, mass (g), year, fall type, classification, latitude, longitude

---

## Data Preprocessing

- Removed invalid or missing lat/long, mass, or year fields
- Excluded zero or negative masses and unparseable years
- Converted year to integer and grouped by decade
- Derived latitude zones for regional comparison

---

## Exploratory Data Analysis (EDA)

EDA techniques and libraries:
- **Libraries Used:** `pandas`, `numpy`, `matplotlib`, `seaborn`, `folium`
- Visualized global distribution via maps and KDE plots
- Assessed mass distribution using histograms and violin plots
- Analyzed decade-wise trends in discovery frequency and mass

---

## Statistical Analysis

### Hypothesis Testing

| Test              | Purpose                                | Result               |
|-------------------|----------------------------------------|----------------------|
| Chi-Square        | Frequency vs. Latitude Zone            | p < 0.001 (Significant) |
| Kruskal-Wallis    | Mass vs. Latitude Zone                 | p < 0.001 (Significant) |
| Shapiro-Wilk      | Normality of mass (zone-wise)          | p < 0.05 (Non-normal) |
| Levene’s Test     | Equality of variances across zones     | p < 0.05 (Unequal variances) |

---

## Clustering & Risk Modeling

### Algorithms Applied:
- **K-Means Clustering** to segment regions by meteorite density
- **DBSCAN** to identify dense hotspots and outliers
- **KDE heatmaps** and **hexbin plots** to visualize impact zones

### Notable Insights:
- Clusters aligned with North Africa, Antarctica, India/SE Asia, and Australia
- High likelihood in deserts and ice-rich regions due to preservation and visibility

---

## Temporal Analysis

- Sharp rise in reports after 1950, particularly post-1980
- Increased frequency linked to detection and scientific collaboration
- No consistent change in average meteorite mass over time
- Linear regression fit suggests observational bias over actual increase

---

## Conclusions

- Meteorite landings are **not spatially or mass-wise uniform**
- Clustering and statistical models show **clear patterns** influenced by environmental and observational factors
- Temporal analysis reveals **reporting-driven growth**, not increased impact rates

---

## Author Background

**Manisha Manchana**  
    - Master's in Data Science at University of Alabama at Birmingham  
    - Former Data Engineer at TA Digital  
    - [LinkedIn](https://www.linkedin.com/in/manisha-manchana/)  

### Skills Applied in This Project
- **Python**: Data manipulation, Processing, Analysis and Visulization
- **EDA & Statistical Testing**: Chi-Square, Kruskal-Wallis, Regression
- **Clustering Techniques**: K-Means, DBSCAN

---

## References

1. [Mass distributions of meteorites (MNRAS, 2020)](https://doi.org/10.1093/mnras/staa521)  
2. [Machine Learning on Asteroids (MNRAS, 2024)](https://doi.org/10.1093/mnras/stae105)  
3. [Spatial Classification of Algerian Meteorites (ASR, 2023)](https://doi.org/10.1016/j.asr.2023.06.015)  
4. [NASA Meteorite Landings Dataset](https://www.kaggle.com/datasets/nasa/meteorite-landings)

---

## Files

- `report.pdf`: Final project report with methodology, analysis, and results  
- `eda.ipynb`: Jupyter notebook containing full EDA and modeling pipeline  

---

> This project showcases the intersection of data engineering, geospatial science, and statistical modeling to understand and interpret real-world extraterrestrial phenomena.

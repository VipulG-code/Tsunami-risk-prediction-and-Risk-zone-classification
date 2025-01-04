# Tsunami-risk-prediction-and-Risk-zone-classification
This repository contains an in-depth analysis of earthquake data from 1995 to 2023, focusing on the relationship between seismic parameters and the occurrence of tsunamis. The project includes clustering, exploratory data analysis (EDA), risk zone classification, and predictive modeling.

Dashboard link: https://public.tableau.com/views/EarthquakeAnalysis_17354827858960/Dashboard1?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link

Don't forget to give this repo a star 🌟 
## Table of Contents
- [Project Overview](#project-overview)
- [Steps Involved](#steps-involved)
- [Dataset](#dataset)
- [Analysis and Methodology](#analysis-and-methodology)
  - [1. Data Cleaning](#1-data-cleaning)
  - [2. Clustering](#2-clustering)
  - [3. Exploratory Data Analysis (EDA)](#3-exploratory-data-analysis-eda)
  - [4. Risk Zone Classification](#4-risk-zone-classification)
  - [5. Predictive Modeling](#5-predictive-modeling)
- [Results](#results)
- [Technologies Used](#technologies-used)
- [How to Use This Repository](#how-to-use-this-repository)
- [Future Scope](#future-scope)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

This project analyzes a dataset of earthquakes occurring between 1995 and 2023, along with seismic parameters, to understand patterns and relationships that predict tsunami occurrences. Key goals include:
1. Identifying relationships between seismic parameters and tsunami occurrences.
2. Classifying regions into high, medium and low-risk zones based on historical data.
3. Building predictive models to determine the likelihood of tsunami generation from seismic data.

## Steps Involved

![image](https://github.com/user-attachments/assets/d1ecc700-613f-442a-b925-7c09b5391023)

1. **Data Import and Cleaning**
2. **Clustering with DBSCAN**
3. **Exploratory Data Analysis (EDA)** (Univariate, Bivariate, Correlation, and Feature Importance)
4. **Risk Zone Classification**
5. **Predictive Modeling** (XGBoost and Sequential ANN)

## Dataset

The dataset contains earthquake data from 1995 to 2023 with the following parameters:
- Magnitude
- Depth
- Frequency in the last 5 years
- Major earthquake frequency in the last 5 years
- Ratio of earthquake occurrences in the last 5 years
- Tsunami occurrence (binary: 1/0)

## Analysis and Methodology

### 1. Data Cleaning
- Handled missing and inconsistent data.
- Standardized numerical values for easier analysis and modeling.

### 2. Clustering
![image](https://github.com/user-attachments/assets/d3fb91f2-b0c4-4ea9-a7b1-0de6c7c578cf)

- Applied **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)** to group data points into clusters based on density.

### 3. Exploratory Data Analysis (EDA)
- **Univariate Analysis**: Distribution of individual variables like magnitude, depth, and frequency.
- **Bivariate Analysis**: Relationships between pairs of variables, such as magnitude vs. depth.
- **Correlation Analysis**: Examined interdependence between parameters.
- **Feature Importance**: Identified key factors influencing tsunami occurrences.

### 4. Risk Zone Classification
![image](https://github.com/user-attachments/assets/fd01fb60-4763-401e-8c78-2a064ee02d30)

- Classified regions into **High Risk**, **Medium Risk**, and **Low Risk** zones based on:
  - Median magnitude
  - Frequency over 5 years (`freq_5years`)
  - Major earthquake frequency (`freq_major_5years`)
  - Ratio of occurrences (`ratio_5years`)
  - Depth

### 5. Predictive Modeling
- **XGBoost Classifier**: Achieved an accuracy of **92.8%** in predicting tsunami occurrences.
- ![image](https://github.com/user-attachments/assets/ce7f6330-b143-4487-bb91-0a3ae80d34c0)

- **Sequential ANN**: Achieved an accuracy of **89%**.
- ![image](https://github.com/user-attachments/assets/474711a6-92bd-483f-b13d-309207fd0a72)

## Results
- Identified strong relationships between seismic parameters and tsunami occurrences.
- Successfully classified regions into risk zones, providing actionable insights.
- Developed highly accurate predictive models for tsunami occurrence.

## Technologies Used
- **Python**
- **Libraries**: Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, XGBoost, TensorFlow/Keras
- **Clustering Algorithm**: DBSCAN

## How to Use This Repository
1. Clone the repository:
   ```bash
   git clone https://github.com/Parthnuwal7/Tsunami-risk-prediction-and-Risk-zone-classification
   ```
2. Install the required Python libraries:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Jupyter notebooks or scripts in sequence to replicate the analysis and models.

## Future Scope
- Incorporating real-time earthquake data for dynamic risk assessment.
- Enhancing predictive models with additional features like geospatial data.
- Expanding risk zone classification to sub-regions for finer granularity.

## Contributing
Contributions are welcome! Please fork the repository, create a feature branch, and submit a pull request with your proposed changes.

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

# 🚕 NYC Taxi Trip Duration — Exploratory Data Analysis & Data Cleaning

## 📂 Original Dataset

Dataset source:  
https://www.kaggle.com/datasets/yasserh/nyc-taxi-trip-duration

Dataset author:  
https://www.kaggle.com/yasserh

---

## 🗽 About the Dataset

The competition dataset is based on the 2016 NYC Yellow Cab trip record data made available in BigQuery on Google Cloud Platform. The data was originally published by the NYC Taxi and Limousine Commission (TLC).

The dataset was sampled and partially cleaned for the purposes of a machine learning playground competition. Based on individual trip attributes, the objective is to predict taxi trip duration.

---

## 📊 Dataset Columns

- `id` — unique identifier for each trip

- `vendor_id` — identifier of the taxi vendor associated with the trip record

- `pickup_datetime` — date and time when the trip started

- `dropoff_datetime` — date and time when the trip ended

- `passenger_count` — number of passengers in the vehicle

- `pickup_longitude` — longitude of pickup location

- `pickup_latitude` — latitude of pickup location

- `dropoff_longitude` — longitude of dropoff location

- `dropoff_latitude` — latitude of dropoff location

- `store_and_fwd_flag` — indicates whether the trip record was temporarily stored in vehicle memory before being sent to the vendor server

- `trip_duration` — trip duration in seconds

---

# ⚙️ How to Run

## 1. Clone the repository

SSH
git clone git@github.com:KrzysztofZakrzewski/NYC_Taxi_Trip_Duration_ML.git
HTML
git clone https://github.com/KrzysztofZakrzewski/NYC_Taxi_Trip_Duration_ML.git
cd <repository_name>
conda env create -f environment.yml
conda activate taxi_reg
jupyter notebook
Or open the project directly in VSCode and select the `taxi_reg` kernel.

## 5. Dataset

Download the original dataset from Kaggle:

https://www.kaggle.com/datasets/yasserh/nyc-taxi-trip-duration

Place the dataset inside the `data/` directory before running the analysis.

# 🎯 Goals of the Analysis

- Understanding relationships between dataset features
- Detecting corrupted or unrealistic observations
- Validating temporal and geographic consistency
- Preparing cleaned and coherent data for machine learning regression
- Exploring transportation and traffic behavior patterns in NYC

---

# 🧪 Analysis Structure

## 1. 🔍 Technical Overview

Initial dataset inspection including:
- feature overview
- missing values analysis
- duplicate validation
- preliminary sanity checks

---

## 2. 🧹 Column Analysis and Potential Data Corrections

Detailed validation and cleaning of:
- datetime columns
- geographic coordinates
- trip duration values
- transportation consistency
- suspicious observations and outliers

### 2.1 ⏱️ Datetime Validation and Trip Duration Analysis

### 2.2 🗺️ Geographic Sanity Check — NYC Reference Bounds

### 2.3 🌍 Geographic Data Validation Using NYC Reference Map

### 2.4 📏 Calculate Geographic Distance

### 2.5 🚩 Column `store_and_fwd_flag`

### 2.6 👥 Column `passenger_count`

---

## 3. 📈 Relationship Analysis

Analysis of relationships between features including:
- distance vs trip duration
- speed vs hour of day
- passenger activity patterns
- vendor comparison
- transportation behavior analysis

---

## 4. 🔗 Correlation Matrix

Correlation analysis between selected numerical features and trip duration.

---

## 5. 🧼 Final Cleaning and Dataset Preparation for ML Regression

Final consistency filtering, feature engineering, and export of the cleaned dataset prepared for machine learning regression tasks.

---

## 6. ✅ Final Conclusions

Summary of findings, cleaning decisions, transportation behavior insights, and final dataset readiness assessment for regression modeling.


# 💡🧠 Personal Insight

One of the most valuable things I learned during this analysis was that it is much more effective to first define spatial relationships and distances, and only then move to temporal analysis.

First comes:
- the point,
- then the line between points,
- then the plane,
- then space itself
- — and only at the very end does time appear allowing you to... do... stuff.

This approach significantly simplifies the workflow. Knowing when something happened or how long it lasted becomes far less meaningful if we still do not understand where it actually happened and what kind of movement the data represents.
# NSDC-Spotify-Popularity-Prediction-Project

## Project Overview
Developed a predictive machine learning model to forecast the yearly streams of songs on Tyler, the Creator’s album *Chromakopia*. By analyzing historical streaming data and song features, this project identifies the key factors that drive commercial success for the artist’s discography and predicts the performance of his latest release.

## Tech Stack
* **Language:** Python
* **Environment:** Google Colab
* **Libraries:** Pandas, NumPy, Scikit-Learn, Seaborn, Matplotlib
* **Techniques:** Regression Analysis, Principal Component Analysis (PCA), Hyperparameter Tuning (GridSearchCV), Mutual Information Regression

## Key Features & Workflow

### 1. Data Collection & Cleaning
* **Sourcing:** Integrated a Kaggle dataset containing Spotify API streaming data with market performance metrics from Kworb.
* **Cleaning:** Utilized Python to remove duplicate entries and filtered the dataset to focus specifically on tracks where Tyler, the Creator was the lead artist.

### 2. Data Preparation & Feature Engineering
* **Feature Creation:** Derived a `featured_artists_count` column by converting artist entries into numerical counts, handling null values as zero.
* **Normalization:** Converted track `duration` from minutes to seconds for standardized numerical analysis.
* **Dimensionality Reduction:** Performed **Principal Component Analysis (PCA)** to streamline feature sets and used **Mutual Information Regression** to identify the most impactful predictors of stream volume.

### 3. Model Development & Optimization
Benchmarked multiple regression architectures to predict yearly stream counts:
* **Models Tested:** Linear Regression, Decision Trees, Random Forest, and **Gradient Boosting Regressor**.
* **Optimization:** Employed **GridSearchCV** for hyperparameter tuning to minimize error rates and maximize predictive accuracy across all candidate models.

### 4. Evaluation & Results
* **Performance Metrics:** Evaluated models using **Mean Squared Error (MSE)** and **$R^2$ Score**.
* **Winner:** The **Gradient Boosting Regressor** emerged as the top performer with a high accuracy of **$R^2 = 0.936$**.
* **Feature Importance:** Visualized the specific song attributes that most heavily influence Tyler, the Creator’s streaming longevity.

## Summary of Findings
* Successfully demonstrated that song performance can be predicted with over 93% accuracy using historical streaming patterns and engineered features.
* The results provide insights into how collaboration counts and track characteristics influence the "shelf-life" of new releases in the streaming era.

## Repository Content
* `Chromakopia_Prediction.ipynb`: Complete Python implementation and model training.
* `Project Slideshow`: Visual presentation of the methodology and showcase results.

---
*Developed as part of the National Student Data Corps (NSDC) Project (Oct 2024 - Dec 2024).*


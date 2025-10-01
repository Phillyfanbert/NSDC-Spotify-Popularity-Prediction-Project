# NSDC-Spotify-Popularity-Prediction-Project
_NSDC UCLA — Machine Learning Music Trend Analysis_
_Predicting the Success of Chromakopia Songs_

**Project Overview**
This project aims to predict the yearly streams of songs on Tyler, the Creator’s album Chromakopia using machine learning models trained on his past music data. By analyzing Spotify features (danceability, tempo, acousticness, etc.) alongside streaming history, we sought to identify which factors most strongly drive long-term popularity.

This work was completed as part of the National Student Data Corps (NSDC) UCLA Chapter.

**Datasets**

We combined two main datasets for richer insights:

Kaggle: Tyler, the Creator Dataset

Contains Spotify audio features (danceability, key, tempo, etc.).

Kworb Streaming Data

Includes total and daily Spotify streams for each track.

**Data Cleaning**
Filtered for Tyler, the Creator’s songs only.

Standardized duration (to seconds) and null values in features.

Merged datasets into a single structured dataset.

Created engineered features (examples below).

**Feature Engineering**
We designed new variables to better capture the “feel” of a track:

Dance Factor = (Valence × Tempo × Instrumentalness) ÷ Speechiness

Live Concert Energy = Liveness × Acousticness × (1 ÷ Speechiness)

Production Complexity = Instrumentalness + (1 − Acousticness) + (Time Signature ÷ 4)

Feel Good Index = Valence × Tempo × Duration

These features improved model interpretability and performance.

**Methods**
We trained multiple regression models to predict yearly streams:

Linear Regression — baseline linear trends.

Decision Tree Regression — interpretable splits but prone to overfitting.

Random Forest Regression — ensemble of trees to boost accuracy.

Gradient Boosting Regression — sequential tree-building to minimize residuals.

Feature selection was guided by Mutual Information Scores and importance analysis.

**Results**
| Model                        | MSE        | R²         |
| ---------------------------- | ---------- | ---------- |
| Linear Regression            | 0.2111     | 0.8829     |
| Decision Tree                | 0.3294     | 0.8172     |
| Random Forest                | 0.2172     | 0.8903     |
| **Gradient Boosting (Best)** | **0.1459** | **0.9364** |

Best model: Gradient Boosting Regression

Most predictive feature: Daily Streams

Predictions were then applied to the Chromakopia tracklist to forecast yearly streams.

**Future Work**
Expand dataset beyond Tyler, the Creator for generalizability.

Explore deep learning models for non-linear feature interactions.

Deploy a simple web app to input song features and predict streams.

**Team**
Project completed by NSDC at UCLA:
Azadeh, Chloe, Colin, Jaiden, Kota, Philbert, Vidita, Michelle


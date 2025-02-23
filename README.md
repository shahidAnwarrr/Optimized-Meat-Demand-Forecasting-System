# Optimized Meat Demand Forecasting System

## Overview

The **Optimized Meat Demand Forecasting System** is a machine learning-based solution designed to help grocery store owners optimize their meat inventory management. Using historical sales data, the system forecasts future meat demand—enabling better planning for orders, reducing losses from unsold stock, and ensuring adequate supply for customers.

## Key Features

- **Data Preprocessing:**
  - Loads historical sales data from a CSV file.
  - Excludes the period from December 15, 2024, to December 25, 2024 (the Christmas season), to prevent this anomalous period from distorting the model.
  - Converts relevant columns to numeric types and handles categorical variables by creating dummy variables.

- **Feature Engineering:**
  - Creates binary features such as `open_next_day` based on the store's operating status.
  - Generates average price features across different meat types.
  - Constructs lag features (e.g., previous day's sales) to capture temporal dependencies.

- **Model Development:**
  - Trains a Random Forest regression model with hyperparameter tuning.
  - Uses Mean Absolute Percentage Error (MAPE) to measure model performance.

- **Forecasting & Visualization:**
  - Implements a recursive forecasting strategy to generate daily predictions for future periods.
  - Provides a one-page Flask dashboard where clients can input forecast parameters (dates, planned price, average price).
  - Displays forecast results in both tabular and graphical formats, along with the current model accuracy (MAPE).

## Getting Started

### Prerequisites

- Python 3.x
- Required packages:
  - Flask
  - pandas
  - numpy
  - matplotlib
  - scikit-learn

Install the required packages using pip:

```bash
pip install flask pandas numpy matplotlib scikit-learn

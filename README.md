# Data Scientist Nanodegree - Starbucks Capstone Project

## Table of Contents

- Project Overview
- Dataset
- Problem Statement
- Approach
- Results
- Installation & Usage
- File Structure
- Requirements
- Acknowledgments

---

## Project Overview

This repository contains the capstone project for Udacity's Data Science Nanodegree program.
For the project, an dataset from Starbucks is provided, which mimics customer behavior on the Starbucks Rewards mobile app.
Starbucks sends various offers to users, such as informational letters, discounts or BOGO (buy one get one free) deals.
Not all users receive the same offers, and the challenge is to analyze transaction, demographic, and offer data to determine
which demographic groups respond best to which offer type.
In this project, Random Forest classification approach is used to reach this goal.

---

## Dataset

The project utilizes three datasets provided by Starbucks:

- **portfolio.json**: Metadata about each offer (e.g., type, duration, reward).
- **profile.json**: Demographic data for each customer (e.g., age, gender, income).
- **transcript.json**: Event log including transactions, offers received/viewed/completed.

Each dataset is in JSON format and must be preprocessed for modeling.

---

## Problem Statement

Starbucks regularly sends personalized offers to its customers. The business challenge is to predict whether a customer will complete an offer based on:

- Customer demographics
- Offer characteristics
- Historical interactions

This enables Starbucks to better target offers and maximize promotional effectiveness and ROI.

---

## Approach

- **Data Cleaning & Feature Engineering:**  
  - Merged the three datasets to create a comprehensive view of customer-offer interactions.
  - Engineered features such as offer type, customer age group, income bracket, and interaction history.
  - Handled missing values and encoded categorical variables.

- **Model Selection:**  
  - Implemented a Random Forest Classifier to predict offer completion.
  - Chose Random Forest for its robustness to overfitting, ability to handle mixed data types, and interpretability.

- **Evaluation:**  
  - Used train/test split and cross-validation.
  - Evaluated model performance using accuracy, precision, recall, and F1-score.

---

## Results

The Random Forest model demonstrated a good starting point for solving the problem described above. 
Feature importance analysis revealed that both offer type and customer demographics significantly influence offer completion rates.
However, it is a good idea to compare the results with other models in order to obtain an overall picture of performance.

---

## Installation & Usage

**Prerequisites:**

- Python 3.x
- Jupyter Notebook

**Required Libraries:**

- numpy
- pandas
- scikit-learn
- matplotlib
- seaborn
- json
- math

**Setup Instructions:**

1. Clone this repository.
2. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```
3. Ensure the input datasets are in place in `data/` directory.
4. Run the main notebook:
    ```bash
    jupyter notebook Starbucks_Capstone_notebook.ipynb
    ```

---

## File Structure

- `Starbucks_Capstone_notebook.ipynb`: Main notebook for data exploration, preprocessing, modeling, and evaluation.
- `data/`: Folder containing the raw data files (`portfolio.json`, `profile.json`, `transcript.json`).
- `requirements.txt`: List of required Python packages.

---

## Requirements

- pandas
- numpy
- math
- json
- matplotlib
- sklearn

---

## Acknowledgments

- Udacity for the capstone project framework and datasets.
- Starbucks for providing anonymized customer and offer data.
- Inspiration from other open-source solutions and data science best practices.

# 📊 Personal Mood Analysis & Prediction Project

A data science project that transforms messy, real-world personal mood tracking data into actionable insights. This project analyzes daily habits like sleep, study, exercise, and hydration to discover which factors have the most significant impact on mood.

---

## ✨ Overview

The goal of this project is to apply a full data science workflow to a personal dataset. It demonstrates:

- How to handle common data quality issues
- How to perform insightful exploratory data analysis (EDA)
- How to build a predictive model to uncover underlying patterns

**Key Insight:** Identify the most influential drivers of mood from daily logged data.

---

## 🚀 Project Workflow

This project follows a complete, end-to-end data science pipeline:

### 1. Data Loading & Cleaning

- Loads data directly from an `.xlsx` file (avoids CSV parsing issues)
- Cleans and standardizes column data
- Handles missing or inconsistent values using methods like interpolation and median filling

### 2. Exploratory Data Analysis (EDA)

- Performs visual analysis to understand relationships between variables
- Generates plots for:
  - Mood distribution
  - Correlations between habits
  - Impact of each habit on mood

### 3. Predictive Modeling

- Trains a `RandomForestClassifier`, a powerful ensemble model
- Learns complex, non-linear patterns linking daily habits to mood outcomes

### 4. Insight Generation

- Extracts feature importances from the trained model
- Quantifies the relative impact of each habit on mood
- Provides a clear, data-driven conclusion on predictive power

---

## 🧠 Key Insights Uncovered

The analysis produced two types of insights: quantitative importance from the model and qualitative inferences from the visual data exploration.

### 1. What the Model Learned: The Most Important Factors

The Random Forest model identified a clear hierarchy of which factors were most predictive of mood:

- **Most Important Factor:** **Sleep** was identified as the single most significant predictor (45% importance).
- **Second Most Important:** **Study hours** — strong correlation with mood changes (37% importance).
- **Lesser Impact:** **Exercise** and **Hydration**, while still relevant, had a comparatively smaller impact on the model's predictions.

![download](https://github.com/user-attachments/assets/5a435a51-01b9-4e98-92a8-e76685ec9532)

### 2. What I Can Infer From My Habits (EDA)

By visualising the data, we can understand how these habits likely influence mood:

- **Positive Impact of Sleep:** The EDA plots suggest a strong positive relationship between sleep and mood. Days with more sleep consistently clustered with higher-rated moods like "Happy" and "Relaxed." Conversely, lower sleep durations were clearly linked to moods like "Tired" and "Unmotivated."
- **The Double-Edged Sword of Studying:** The impact of studying appears more complex. While moderate study hours may correlate with feeling "Neutral" or productive, the data suggests that very high study hours often correspond with lower-rated moods like "Tired" or "Overwhelmed." This indicates a potential burnout threshold.
- **Clear Habit-Based Clustering:** The pairplot visualization showed that moods are not random. Days tend to group together based on habits. For example, days with low sleep and high study hours often form a distinct cluster under the "Low Mood" category, providing strong visual evidence of this pattern.

---

## 🛠️ How to Use This Project

### 1. Prerequisites

Ensure you have Python installed. Then install required libraries. You can use the following `requirements.txt` file:

```txt
pandas
numpy
matplotlib
seaborn
scikit-learn
openpyxl
```
### 2. Prepare Your Data
Create an Excel file named ```mood tracker.xlsx``` in the same directory as the script.

Ensure it has columns like ```Mood```, ```Study```, ```Exercise```, ```Hydration```, etc. The script is designed to be flexible with missing columns or data.

### 3. Run the Analysis
Execute the Python script from your terminal:

```python mood_classification.py```

The script will print the cleaning steps, generate EDA plots, and finally output the feature importance results before displaying the final summary chart.

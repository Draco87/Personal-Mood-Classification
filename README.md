# 📊 Personal Mood Analysis & Prediction Project

A data science project that transforms messy, real-world personal mood tracking data into actionable insights. This project analyses daily habits like sleep, study, exercise, and hydration to discover which factors have the most significant impact on mood.

## ⚠️ Disclaimer

This project is intended for **educational and exploratory purposes only**. The analysis is based on a limited set of **self-logged data** and does **not** account for other critical factors that may influence well-being, such as:

- Diet  
- Hormonal balance  
- Social interactions  
- Screentime, etc.  

The insights generated through this project are **not a substitute for professional medical advice**. Always consult a qualified healthcare provider with any questions regarding your health.

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

### 1. 📈 What the Correlation Map Showed (Linear Trends)

![download](https://github.com/user-attachments/assets/3e206b73-6767-4cf7-b4bb-7d045f9749e6)

The initial correlation analysis provided a baseline understanding of linear relationships between habits and mood:

- **Strongest Positive Link:**  
  Hydration exhibited the strongest positive linear correlation with mood (**r = 0.29**).

- **Inverse Habit Relationship:**  
  A notable inverse correlation was observed between **Exercise** and **Hydration** (**r = -0.35**), suggesting that hydration levels tended to be lower on days when exercise was logged.

---

### 2. 📊 What the Visual Plots Showed (Habit-Mood Relationships)

![download](https://github.com/user-attachments/assets/ce9e5222-4641-46d3-a8d6-cb483f64cdc3)


- **Clear Positive Impact of Sleep:**  
  Boxplots revealed a consistent positive relationship between **sleep duration** and **mood**. Higher median sleep was strongly associated with better moods (e.g., _“Happy,” “Relaxed”_).
  
![download](https://github.com/user-attachments/assets/79aef47a-74e6-483e-804c-1b4684b76289)

- **Habit-Based Clustering is Real:**  
  The pairplot analysis demonstrated that **moods are not randomly distributed**. Days with similar habit patterns (e.g., **low sleep** + **high study hours**) clustered together and were often linked to **low mood states**.

---

### 3. ⚙️ What the Model Learned: The Most Important Factors

The Random Forest model identified a clear hierarchy of which factors were most predictive of mood:

- **Most Important Factor:** **Sleep** was identified as the single most significant predictor (45% importance).
- **Second Most Important:** **Study hours** — strong correlation with mood changes (37% importance).
- **Lesser Impact:** **Exercise** and **Hydration**, while still relevant, had a comparatively smaller impact on the model's predictions.

![download](https://github.com/user-attachments/assets/5a435a51-01b9-4e98-92a8-e76685ec9532)

### 4. ✒️ What I Can Infer From My Habits (EDA)

By visualising the data, we can understand how these habits likely influence mood:

- **Positive Impact of Sleep:** The EDA plots suggest a strong positive relationship between sleep and mood. Days with more sleep consistently clustered with higher-rated moods like "Happy" and "Relaxed." Conversely, lower sleep durations were clearly linked to moods like "Tired" and "Unmotivated."
- **The Double-Edged Sword of Studying:** The impact of studying appears more complex. While moderate study hours may correlate with feeling "Neutral" or productive, the data suggests that very high study hours often correspond with lower-rated moods like "Tired" or "Overwhelmed." This indicates a potential burnout threshold.
- **Clear Habit-Based Clustering:** The pairplot visualisation showed that **moods are not random**. Days tend to group together based on habits. For example, days with low sleep and high study hours often form a distinct cluster under the "Low Mood" category, providing strong visual evidence of this pattern.


> These insights highlight the tangible impact of daily habits on mood patterns and underscore the value of combining statistical and visual methods in behavioural data analysis.
---

## 🛠️ How to Use This Project

### 1. Prerequisites

Ensure you have Python installed. Then, install the required libraries. You can use the following `requirements.txt` file:

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

Ensure it has columns like ```Mood```, ```Sleep```,```Study```, ```Exercise```, ```Hydration```, etc. The script is designed to be flexible with missing columns or data.

### 3. Run the Analysis
Execute the Python script from your terminal:

```python mood_classification.py```

The script will print the cleaning steps, generate EDA plots, and finally output the feature importance results before displaying the final summary chart.

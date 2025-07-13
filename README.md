````markdown
# Cardiovascular Disease Prediction

## Project Overview
This project builds a machine-learning pipeline to predict a patient’s risk of cardiovascular disease based on medical records and lifestyle factors. It covers data ingestion, cleaning, exploratory analysis, model training, and evaluation.

---

## Table of Contents
- [Features](#features)  
- [Data Dictionary](#data-dictionary)  
- [Modules](#modules)  
- [Tech Stack](#tech-stack)  
- [Installation](#installation)  
- [Usage](#usage)  
- [Results](#results)  
- [Contributing](#contributing)  
- [License](#license)  

---

## Features
- Load and inspect raw patient data  
- Clean, encode, and remove outliers  
- Visualize demographics, health indicators, and habits  
- Train and compare three classifiers (Random Forest, Decision Tree, Logistic Regression)  
- Evaluate models with accuracy, precision, recall, F1, and confusion matrices  

---

## Data Dictionary

| Feature                          | Description                                              |
|----------------------------------|----------------------------------------------------------|
| **General_Health**               | Self-reported health status (Poor, Fair, Good, etc.)     |
| **Checkup**                      | Time since last medical checkup                          |
| **Exercise**                     | Whether patient exercises regularly (Yes/No)             |
| **Heart_Disease**                | Target variable (0 = No, 1 = Yes)                        |
| **Skin_Cancer**                  | History of skin cancer (0/1)                             |
| **Other_Cancer**                 | History of other cancers (0/1)                           |
| **Depression**                   | History of depression (0/1)                              |
| **Diabetes**                     | Diabetes status (No, pre-diabetes, gestational, Yes)     |
| **Arthritis**                    | History of arthritis (0/1)                               |
| **Sex**                          | Gender (Male/Female)                                     |
| **Age_Category**                 | Age bracket (e.g., 18–24, 25–29, …, 80+)                 |
| **BMI**                          | Body Mass Index                                         |
| **Smoking_History**              | Ever smoked (0/1)                                       |
| **Alcohol_Consumption**          | Drinks per month                                         |
| **Fruit_Consumption**            | Servings of fruit per week                               |
| **Green_Vegetables_Consumption** | Servings of green vegetables per week                    |
| **FriedPotato_Consumption**      | Servings of fried potatoes per week                      |

---

## Modules
1. **Data Import**  
   - Load CSV into pandas DataFrame  
2. **Preprocessing**  
   - Drop redundant columns (Height, Weight)  
   - Map and encode categorical values  
   - Remove outliers with IQR method  
3. **Exploratory Data Analysis (EDA)**  
   - Demographics (gender, age, BMI)  
   - Health & lifestyle visualizations  
4. **Modeling**  
   - Train Random Forest, Decision Tree, Logistic Regression  
5. **Evaluation**  
   - Compute accuracy, precision, recall, F1  
   - Plot confusion matrices  

---

## Tech Stack
- **Language:** Python 3.x  
- **Data Manipulation:** pandas, NumPy  
- **Visualization:** Matplotlib, Seaborn  
- **Modeling:** scikit-learn  
- **Environment:** Jupyter Notebook or any Python IDE  

---

## Installation

1. **Clone the repo**  
   ```bash
   git clone https://github.com/Sakshi00555/Cardiovasculardisease
   cd cardiovascular-prediction
````

2. **Create and activate a virtual environment**

   ```bash
   python3 -m venv venv
   source venv/bin/activate      # Linux/macOS
   venv\Scripts\activate         # Windows
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Place dataset**

   * Download `CVD_cleaned.csv` into the project root.

---

## Usage

1. **Start Jupyter Notebook**

   ```bash
   jupyter notebook
   ```
2. **Open** `Cardiovascular_Disease_Prediction.ipynb`
3. **Run all cells in order** to reproduce the preprocessing, EDA, modeling, and evaluation.

---

## Results

| Model               | Accuracy | Precision | Recall | F1 Score |
| ------------------- | -------- | --------- | ------ | -------- |
| Random Forest       | 0.914    | 0.417     | 0.036  | 0.067    |
| Decision Tree       | 0.719    | 0.198     | 0.753  | 0.313    |
| Logistic Regression | 0.915    | 0.479     | 0.039  | 0.073    |

* **Key findings:**

  * Age ≥ 55 and BMI ≥ 25 are the strongest risk factors.
  * Higher fruit/vegetable intake correlates with lower risk; fried potatoes increase risk.
  * Smoking significantly raises disease likelihood.
  * Patients who exercise often are diagnosed more—likely due to more frequent checkups.

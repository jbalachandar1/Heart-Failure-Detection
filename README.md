# Heart Disease Prediction

A machine-learning pipeline to predict the presence of heart disease based on patient clinical and demographic features. Implements both Logistic Regression and Random Forest classifiers, provides model evaluation metrics, and includes a simple Gradio web interface for live predictions.

## 🚀 Features

- **Data Loading & Cleaning**  
  - Reads `heart.csv`, checks for missing values, and displays basic statistics.  
- **Encoding & Feature Engineering**  
  - Label-encodes categorical variables.  
  - Selects features via correlation analysis.  
- **Exploratory Data Analysis**  
  - Histograms for all numerical features.  
  - Boxplot of ST depression (`Oldpeak`) by disease status.  
  - Correlation heatmap.  
- **Model Training & Evaluation**  
  - **Logistic Regression** and **Random Forest** classifiers.  
  - Standard scaling of features.  
  - Classification reports (precision, recall, F1-score) and confusion matrices.  
- **Model Persistence**  
  - Saves trained models and preprocessing objects (`.pkl`) with `joblib`.  
- **Interactive Demo**  
  - Gradio interface for live input of patient metrics and on-the-fly prediction.

## 📊 Results

| Model               | Accuracy | Precision (0 / 1) | Recall (0 / 1) | F1-Score (0 / 1) |
|---------------------|---------:|------------------:|---------------:|-----------------:|
| Logistic Regression |     0.85 |             0.80 / 0.90 |          0.87 / 0.84 |         0.83 / 0.87 |
| Random Forest       |     0.88 |             0.84 / 0.90 |          0.87 / 0.88 |         0.85 / 0.89 |

> **Support:** 77 normal / 107 disease cases (184 total).

## 📂 Dataset

- **Source:** `heart.csv`  
- **Features:**  
  - `Age`, `Sex` (M/F), `ChestPainType` (TA, ATA, NAP, ASY)  
  - `RestingBP`, `Cholesterol`, `FastingBS`  
  - `RestingECG` (Normal, ST, LVH), `MaxHR`, `ExerciseAngina`, `Oldpeak`, `ST_Slope`  
- **Target:** `HeartDisease` (0 = Normal, 1 = Disease)

## 🔧 Installation

1. Clone the repository:  
   ```bash
   git clone https://github.com/your-username/heart-disease-prediction.git
   cd heart-disease-prediction

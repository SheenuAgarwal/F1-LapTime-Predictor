# 🏎️ F1 Qualifying Lap Time Predictor

This project builds a machine learning model to predict F1 qualifying lap times using telemetry, weather, tyre, and driver performance data. The model is trained on data from 2021 to 2025 (up to Monaco GP) and makes predictions for the upcoming Spanish GP 2025.

## 📊 Data
- **Source**: `race_df.csv`, `qualifying_df.csv`
- **Fields** include:
  - Driver ID and Number
  - Stint, Tyre Compound, and Freshness
  - Sector Speeds: `SpeedI1`, `SpeedI2`, `SpeedFL`, `SpeedST`
  - Weather: Air Temp, Track Temp, Humidity, Wind, Rainfall
  - Track status, Lap number, Year, Grand Prix ID
  - Target: `LapTimeSeconds`

## 📦 Features
- Model training using Ridge, Random Forest, Gradient Boosting, and XGBoost.
- Hyperparameter tuning via GridSearchCV.
- Feature importance visualization.
- Support for future predictions (e.g., Spanish GP 2025).

## ⚙️ ML Models Used
- XGBoost Regressor
- Random Forest Regressor
- Ridge Regression
- Gradient Boosting Regressor
  
## 🧠 Best Model
- Automatically selected based on highest R² on test set.
- Feature importances shown for interpretability.

## 🖼️ Output
- Feature importance chart: [`images/feature_importance.png`](https://github.com/Shreeansh-Gupta/F1-LapTime-Predictor/blob/main/Top20_Feature_Importance_Race.png?raw=true)


## 📂 Files
- `Race_Predictor_model_f1_cleaned.py` – Cleaned version for GitHub
- `race_df.csv` – Input dataset
- `Race_Predictor_model_f1.ipynb` – Original notebook
- `images/feature_importance.png` – Chart
- `README.md` – Project overview

## 🔧 Installation

Install required packages using pip:

```bash
pip install pandas numpy scikit-learn matplotlib xgboost
```  

## 🚀 How to Run
1. Clone this repo.
2. Ensure `race_df.csv` is in the root directory.
3. Run `Race_Predictor_model_f1_cleaned.py`.

## 🔮 Future Work
- Add telemetry-based predictors (braking, acceleration zones)
- GP-specific model tuning

📌 Usage
Run the notebook Race_Predictor_model_f1_cleaned.ipynb in Jupyter or any Python environment. Make sure race_df.csv is in the same directory.

🗂️ Data Source
- Historical race and qualifying data (2021–2025)
- Weather data scraped for May 31, 2025, at Barcelona Circuit
- Real-time prediction integration via API

📎 Author
Shreeansh

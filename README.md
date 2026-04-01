# Cardiac Diagnostic Model
### Byte 2 Beat Hackathon - Cardiovascular Disease Prediction

## Project Summary
A dual-model diagnostic framework for cardiovascular disease prediction.
Built a population-level risk screener (XGBoost, AUC = 0.8) and a clinical diagnostic model (Random forest, AUC = 0.956), with SHAP analysis for both.

## Repository Contents
- `fullcode.ipynb` — full analysis pipeline (EDA, models, SHAP)
- `report.pdf` — project report
- `heart_scaler.joblib` / `cardio_scaler.joblib` — fitted scalers
- `cardio_xgb_model.joblib` — trained cardiac model weights
- `heart_rf_model.joblib` — trained heart model weights
- `requirements.txt` — required libraries

## How to run
1. Open `fullcode.ipynb` in Google Colab
2. Go to Runtime -> Run all
3. Datasets are loaded via gdown links inside the notebook

## Results
| Model | Dataset | Accuracy | AUC |
|-------|---------|----------|-----|
| XGBoost (tuned) | Cardiac (68k patients) | 73.5% | 0.8 |
| Random forest | Heart (746 patients) | 90.7% | 0.956 |
<img width="1150" height="490" alt="image" src="https://github.com/user-attachments/assets/5688dca1-f47e-4c67-b196-820f6cc6ac7e" />

## Key Findings
- ST slope and Oldpeak are the strongest clinical predictors of heart disease
- Systolic blood pressure and age drive population-level cardiovascular risk
- SHAP analysis confirms model decisions align with established clinical knowledge
<img width="940" height="590" alt="image" src="https://github.com/user-attachments/assets/4b422636-25a5-4a69-af10-27335c4b398d" />
<img width="927" height="490" alt="image" src="https://github.com/user-attachments/assets/c793f62a-bbec-42a3-9e4a-a311f62dc934" />

## AI Disclosure
Claude and Gemini were used as coding assistants for debugging and algorithmic suggestions. All analysis and interpretations were written by the author.

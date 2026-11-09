# Healthcare Appointment No-show Prediction

## Project Overview
This project uses machine learning to predict whether a patient will miss a scheduled healthcare appointment. The objective is to identify appointment-related patterns and evaluate predictive models that could help healthcare providers improve appointment attendance and scheduling efficiency.

## Dataset
- **Source:** [Medical Appointment No Shows Dataset](https://www.kaggle.com/datasets/joniarroba/noshowappointments)
- **Origin:** Brazil, 2016
- **Original records:** 110,527
- **Records after cleaning:** 110,521
- **Target variable:** `No-show`
  - 0 = Patient attended
  - 1 = Patient missed the appointment

## Methodology
1. Data cleaning and preprocessing
2. Exploratory Data Analysis (EDA)
3. Feature engineering
4. Patient-level train-test splitting to prevent patient overlap
5. Feature encoding and scaling
6. Machine learning model development
7. Model evaluation and comparison

SMS notification was excluded from the booking-time prediction models because it may not be available at the time of booking.

## Machine Learning Models
- Logistic Regression
- Random Forest
- HistGradientBoostingClassifier

## Model Performance

| Model | Accuracy | Precision | Recall | F1-score | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | 64.84% | 31.26% | 59.92% | 41.09% | 66.57% |
| Random Forest | 58.78% | 30.92% | 82.20% | 44.94% | 73.14% |
| Gradient Boosting | 67.06% | 34.23% | 66.22% | 45.14% | 73.59% |

Gradient Boosting achieved the highest F1-score and overall accuracy among the evaluated models, while Random Forest achieved the highest recall.

## Key Findings
- Waiting days was the strongest predictive feature based on permutation importance.
- Appointment no-show patterns varied across age groups and waiting-time categories.
- The dataset had an overall no-show rate of approximately 20.19%.

## Tools and Technologies
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab
- Looker Studio

## Limitations
The dataset is observational and originates from Brazil in 2016. The findings should not be assumed to generalise to other healthcare systems or current appointment populations. Predictive feature importance does not establish causation.

## Author
Mehram Khaiser


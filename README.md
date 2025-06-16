# Sleep Disorder Prediction 

This project applies machine learning techniques to predict sleep disorders based on health and lifestyle factors. It includes data preprocessing, exploratory data analysis (EDA), model training, evaluation, and hyperparameter tuning using GridSearchCV.

##  Project Structure


  <pre> ``` 
  Sleep-Disorder-Prediction/ 
  ├── data/ 
  │ └── Sleep_health_and_lifestyle_dataset.csv 
  ├── notebooks/ 
  │ └── sleep_disorder_prediction.ipynb 
  ├── images/ 
  │ ├── Confusion Matrix.png 
  │ ├── Confusion Matrix after Hyperparameter Tuning.png 
  │ └── Top 10 Feature Importances.png
  ├── .gitignore 
  └── README.md ``` </pre>


##  Dataset Overview

- **Source**: Public health and lifestyle dataset
- **Features**:
  - Gender, Age, BMI Category
  - Sleep Duration, Quality of Sleep
  - Physical Activity, Stress Level
  - Heart Rate, Daily Steps, Blood Pressure
- **Target**: Sleep Disorder type

##  ML Models Used

- Logistic Regression
- Random Forest
- Gradient Boosting
- Hyperparameter tuning with **GridSearchCV**

##  Results

- **Final Accuracy**: **96%**
- High precision and recall achieved post tuning
- Feature importance plots available in `images/`

##  Insights & Observations

### Why Sleep Duration Has Lower Feature Importance?

Although *Sleep Duration* is intuitively expected to play a major role in determining sleep disorders, its feature importance was relatively lower compared to other variables like stress levels, occupation, or BMI. This could be due to:

- **Multicollinearity**: Other features such as physical activity level or stress may already capture the effects of sleep duration.
- **Data Distribution**: The range or variance in the recorded sleep durations might be limited in this dataset.
- **Model Dependency**: Tree-based models can sometimes deprioritize features that don’t provide clear splits in the data.

Therefore, while sleep duration is important in a general health context, its predictive power in this specific dataset and model setting was found to be less dominant.


# Car Price Prediction

## Oasis Infobyte Data Science Internship – Task 3

### Project Overview
This project aims to predict the selling prices of used cars using Machine Learning techniques. The model estimates car prices based on various features such as car make, model, manufacturing year, kilometers driven, fuel type, transmission, engine capacity, maximum power, and other vehicle specifications.

### Dataset Information
- **Dataset Name:** Car Details V4 (`car details v4.csv`)
- **Number of Records:** 2,059
- **Number of Columns:** 20
- **Target Variable:** Price

The dataset contains information about different cars, including their make, model, year, kilometers driven, fuel type, transmission, location, owner, engine specifications, and other features.

### Project Objectives
- Analyze used car data.
- Clean and preprocess the dataset.
- Handle missing values.
- Perform feature engineering.
- Train multiple Machine Learning regression models.
- Evaluate and compare model performance.
- Select the best model for predicting car prices.

### Data Preprocessing and Feature Engineering
The following steps were performed:

- Removed duplicate records.
- Handled missing values using imputation techniques.
- Removed records with missing or non-positive prices.
- Converted engine specifications into numerical features.
- Extracted engine capacity in CC.
- Extracted maximum power in BHP.
- Extracted maximum torque values.
- Created a new feature called `Car_Age`.
- Applied StandardScaler to numerical features.
- Applied OneHotEncoder to categorical features.
- Split the dataset into training and testing sets using an 80:20 ratio.

### Machine Learning Algorithms Used
Three regression algorithms were trained and compared:

1. Ridge Regression
2. Random Forest Regressor
3. Extra Trees Regressor

### Model Evaluation
The models were evaluated using the following metrics:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R-squared (R²) Score

#### Model Comparison Results

| Model | MAE | RMSE | R² Score |
|---|---:|---:|---:|
| Extra Trees | 276777.98 | 1058051.45 | 0.840 |
| Random Forest | 305850.30 | 1159218.65 | 0.808 |
| Ridge Regression | 630324.47 | 1342240.28 | 0.742 |

### Best Performing Model
The **Extra Trees Regressor** achieved the best performance on the test dataset.

**Performance:**
- MAE: 276,777.98
- RMSE: 1,058,051.45
- R² Score: 0.840

Hyperparameter tuning was also performed using RandomizedSearchCV with 5-fold cross-validation. However, the tuned model did not improve the original model's test performance. Therefore, the original Extra Trees model was selected as the final model.

### Model Saving and Prediction
The trained Extra Trees model pipeline was saved using Joblib.

The saved model was loaded again and tested with sample data to verify that it could successfully generate car price predictions.

### Project Screenshots
The `screenshots` folder contains the visual outputs generated during the project:

- Price distribution
- Correlation heatmap
- Model comparison
- Feature importance

### Technologies and Libraries Used
- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib

### Conclusion
This project demonstrates the application of Machine Learning techniques to predict used car prices based on vehicle characteristics.

After training and evaluating three regression models, the Extra Trees Regressor achieved the best test performance, with an R² score of 0.840.

The project provided practical experience in data cleaning, exploratory data analysis, feature engineering, model training, evaluation, and prediction.

### Internship Details
- **Organization:** Oasis Infobyte
- **Track:** Data Science
- **Task:** Task 3 – Car Price Prediction

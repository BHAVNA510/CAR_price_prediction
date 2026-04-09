🚗 Car Price Prediction App
 -Project Overview

The Car Price Prediction App is a machine learning project designed to estimate the selling price of used cars based on historical vehicle data.
The goal of the project is to help buyers and sellers make data-driven pricing decisions by understanding how factors such as car age, mileage, fuel type, and transmission impact resale value.

This project focuses not just on prediction, but also on data analysis, feature engineering, and model evaluation, making it relevant for data analytics and applied machine learning roles.

🎯 Problem Statement

Used car pricing often depends on multiple factors and can vary significantly based on condition, usage, and market trends.
Manual estimation can be biased or inconsistent.

Objective:

Predict used car selling prices accurately

Identify key factors influencing car prices

Build a reliable regression model with minimal prediction error

📊 Dataset Information

Source: Used Car Dataset (CSV file)

Number of records: 301

Target variable: Selling_Price

Features include:

Present price of the car

Kilometers driven

Fuel type

Seller type

Transmission

Number of previous owners

Car age (engineered feature)

🧹 Data Cleaning & Preprocessing

The dataset was first checked for missing values and inconsistencies.

Key steps:

Verified there were no missing values

Converted categorical variables (Fuel Type, Seller Type, Transmission) using one-hot encoding

Created a new feature car age by subtracting manufacturing year from current year

Removed redundant columns after feature transformation

Checked correlations to understand relationships between features and selling price

This ensured the data was clean, structured, and ready for modeling.

<img width="972" height="428" alt="_- visual selection" src="https://github.com/user-attachments/assets/11a5b8a7-6217-4815-985a-677643adb7bd" />


🔍 Exploratory Data Analysis (EDA)

EDA was performed to understand patterns and relationships in the data.

Key insights:

Present price has a strong positive correlation with selling price

Car age and kilometers driven negatively impact resale value

Diesel cars tend to retain higher resale value compared to petrol

Cars sold by individuals generally have lower prices than dealer-listed cars

Visualizations such as pair plots, correlation heatmaps, and scatter plots were used to validate these insights.

🛠 Feature Engineering

Feature engineering was a key part of the project.

Important engineered features:

Car Age (no_year): Current year – manufacturing year

Encoded categorical variables using dummy variables

Selected features based on correlation and importance analysis

Feature importance was later validated using ensemble models.

🤖 Model Selection

The primary model used was ExtraTreesRegressor, an ensemble learning algorithm.

Why ExtraTreesRegressor?

Handles non-linear relationships well

Reduces overfitting by averaging multiple randomized decision trees

Performs well with tabular data and mixed feature types

Less sensitive to noise and outliers compared to single-tree models

Additional models like Random Forest were also experimented with for comparison.

⚙️ Model Training & Hyperparameter Tuning

Steps involved:

Split data into training (70%) and testing (30%)

Trained ensemble regression models

Applied RandomizedSearchCV to tune hyperparameters such as:

Number of trees

Tree depth

Minimum samples per split

Feature selection strategy

This improved model stability and reduced prediction error.

📈 Model Evaluation

The model was evaluated using standard regression metrics:

MAE (Mean Absolute Error): Measures average prediction error

MSE (Mean Squared Error): Penalizes large errors

RMSE (Root Mean Squared Error): Overall prediction accuracy

Final RMSE was approximately ~2, indicating reasonable predictive performance for a small real-world dataset.

Scatter plots and residual distributions were used to visually assess prediction quality.

📊 Key Results & Insights

Present price is the strongest predictor of resale value

Older cars and higher mileage significantly reduce selling price

Ensemble models outperform simpler regression models

Feature engineering plays a major role in improving accuracy

🧰 Tools & Technologies Used

Python

Pandas, NumPy – Data manipulation

Matplotlib, Seaborn – Data visualization

Scikit-learn – Modeling & evaluation

Pickle – Model serialization

🚀 Future Improvements

Add more data for better generalization

Try gradient boosting models like XGBoost

Deploy the model as a web application

Include market trends and location-based features

👩‍💻 Author

Bhavna Meena
Aspiring Data Analyst / Data Science Professional

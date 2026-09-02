# Food Demand Forecasting Using Machine Learning

### 📌 Project Overview
Food demand forecasting is an important problem for food-service businesses because accurately estimating demand can help reduce food wastage, improve inventory planning, and ensure better resource allocation.
This project develops a machine learning regression model to predict weekly food demand (num_orders) using historical food-service data. The analysis explores patterns across meals, fulfilment centers, pricing, promotional activities, and time.
Multiple regression models are trained and evaluated using a time-based validation strategy, with the best-performing model selected for final demand prediction.

### 🎯 Objectives
  - Analyze historical food demand data.
  - Understand demand patterns across meals and fulfilment centers.
  - Perform data preprocessing and exploratory data analysis.
  - Identify important factors associated with weekly demand.
  - Build and compare multiple regression models.
  - Evaluate models using RMSE and R².
  - Use a time-based validation approach suitable for forecasting.
  - Select the best-performing model for predicting future demand.
  - Generate demand predictions for the provided test dataset.

### 📊 Dataset
The project uses the following datasets:

  - train.csv – Historical training data containing weekly food demand.
  - test.csv – Data for which demand predictions are generated.
  - meal_info.csv – Information about meals, including category and cuisine.
  - fulfilment_center_info.csv – Information about fulfilment centers.
  - sample_submission.csv – Sample format for the prediction output.
#### Dataset Size
Dataset	Rows	Columns
Train	456,548	9
Test	32,573	8
Meal Information	51	3
Fulfilment Center Information	77	5

The training data covers weeks 1–145, while the test data represents weeks 146–155.

### 🔍 Data Analysis
The project includes exploratory analysis to understand:

  - Weekly demand patterns
  - Demand across meal categories
  - Demand across fulfilment centers
  - Relationship between demand and pricing
  - Promotional effects
  - Featured meals and email promotions
  - Distribution of demand
  - Correlations between numerical variables
The datasets are also merged to enrich the analysis with meal and fulfilment-center information.

### 🧹 Data Preprocessing
The preprocessing workflow includes:

  - Loading the individual datasets.
  - Inspecting dataset dimensions and data types.
  - Checking for missing values.
  - Checking for duplicate records.
  - Merging relevant datasets for exploratory analysis.
  - Preparing numerical model features.
  - Separating the target variable (num_orders) from the input features.
  - Excluding id from the model because it is an identifier rather than a meaningful predictive feature.

The final model uses the following features:
```text
week
center_id
meal_id
checkout_price
base_price
emailer_for_promotion
homepage_featured
```
Target variable:
``` text
num_orders
```

### 🤖 Machine Learning Models
Three regression models were developed and compared:

Linear Regression
Decision Tree Regressor
Random Forest Regressor
Why Regression?
  The target variable, num_orders, represents the number of orders for a meal at a fulfilment center during a particular week. Since the target is continuous/numerical, regression algorithms are appropriate for the prediction task.

### ⏳ Validation Strategy
Because this is a forecasting problem, a random train-test split was avoided for final evaluation.
Instead, the training data was sorted chronologically by week and divided using a time-based split.
The earlier portion of the historical data was used for training, while the latest 20% was used as the validation set.
This approach better represents the real-world scenario of:
  Training a model using past demand and predicting demand for future periods.

### 📈 Model Evaluation
The models were evaluated using:
#### RMSE — Root Mean Squared Error
RMSE measures the average magnitude of prediction errors, with larger errors receiving greater importance.
Lower RMSE indicates better performance.
#### R² — Coefficient of Determination
R² indicates how much of the variation in the target variable is explained by the model.
Higher R² indicates better performance.

### Results
Model	RMSE	R²
Linear Regression	331.68	0.1789
Decision Tree Regressor	310.82	0.2789
Random Forest Regressor	243.53	0.5573
#### 🏆 Best Model
The Random Forest Regressor achieved the best validation performance:
RMSE: 243.53
R²: 0.5573
Therefore, Random Forest was selected as the final model.

### 🌲 Feature Importance

Feature importance from the final Random Forest model indicates the relative contribution of the input features to prediction.
``` text
Feature	Importance
checkout_price	23.69%
meal_id	22.74%
center_id	17.31%
base_price	13.88%
homepage_featured	8.69%
week	8.33%
emailer_for_promotion	5.36%
``` 
The results indicate that checkout price, meal identity, and fulfilment center were among the most influential features in the final model.
  Feature importance represents the model's learned predictive contribution and should not be interpreted directly as causal relationships.

### 🚀 Final Model & Prediction
After selecting Random Forest as the best-performing model, the final model was retrained using the complete historical training dataset.
The trained model was then used to predict demand for the test dataset.
Prediction Output
The final prediction file contains:
32,573 predictions
No missing prediction values
Predictions generated for the complete test dataset

The generated output is available in:
``` text
food_demand_predictions.csv
```

### 🛠️ Technologies Used
  Python
  Pandas
  NumPy
  Scikit-learn
  Matplotlib
  Seaborn
  Plotly
  Jupyter Notebook

### 📁 Project Structure
``` text
Food_Demand_Forecasting_Using_ML/
│
├── Food_Demand_Forecasting_Using_ML.ipynb
├── README.md
├── requirements.txt
├── LICENSE
│
├── train.csv
├── test.csv
├── meal_info.csv
├── fulfilment_center_info.csv
├── sample_submission.csv
│
└── food_demand_predictions.csv
```

### ▶️ How to Run the Project
1. Clone the repository
``` bash
git clone https://github.com/Kruti115/Food_Demand_Forecasting_Using_ML.git
```
2. Navigate to the project directory
``` bash
cd Food_Demand_Forecasting_Using_ML
```
3. Install the required libraries
``` bash
pip install -r requirements.txt
```
4. Launch Jupyter Notebook
``` bash
jupyter notebook
```
5. Open
``` bash
Food_Demand_Forecasting_Using_ML.ipynb
``` 
Run the notebook cells sequentially to reproduce the analysis and model results.

### 💡 Key Takeaways
  - Food demand varies considerably across meals and fulfilment centers.
  - Pricing and meal/center characteristics are important predictive variables.
  - Promotional and featured-meal indicators also contribute to demand prediction.
  - Random Forest performed better than Linear Regression and Decision Tree on the time-based validation set.
  - Using a chronological validation strategy provides a more realistic evaluation for a forecasting problem.
  - The final Random Forest model was retrained on all available historical training data before generating test predictions.

### 🔮 Future Improvements
The model could potentially be improved by incorporating additional information such as:
  - Weather conditions
  - Holidays and festivals
  - Regional events
  - More detailed historical demand trends
  - Lag-based demand features
  - Rolling demand statistics
  - Systematic hyperparameter optimization
  - Gradient boosting models
  - Advanced time-series forecasting approaches

### 👩‍💻 Author

Kruti Gupta
B.Tech — Artificial Intelligence & Data Science
GitHub: Kruti115

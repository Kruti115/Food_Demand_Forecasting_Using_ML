# 🍱 Food Demand Forecasting Using Machine Learning

A machine learning project that predicts weekly meal demand using historical order data to support inventory planning, resource allocation, and operational decision-making.

## 📌 Project Overview

Accurately forecasting meal demand can help food delivery and fulfillment operations optimize inventory, reduce food wastage, and prepare for fluctuations in customer demand.

This project develops and compares multiple machine learning regression models to predict weekly meal demand using historical data from fulfillment centers.

The project follows the workflow:

**Data Preprocessing → Feature Engineering → Exploratory Analysis → Model Training → Model Evaluation → Model Comparison**


## 🎯 Objectives

The main objectives are to:

* Analyze historical meal demand
* Identify important demand patterns
* Clean and preprocess the dataset
* Engineer useful predictive features
* Train multiple regression models
* Compare model performance
* Select the best-performing model
* Explore potential improvements for future forecasting


## 📂 Dataset
The project uses historical food order data containing information about fulfillment centers, meals, pricing, promotions, and weekly demand.

### Main Features

| Feature               | Description                                             |
| --------------------- | ------------------------------------------------------- |
| Center ID             | Identifier for the fulfillment center                   |
| Meal ID               | Unique identifier for the meal                          |
| Checkout Price        | Price at which the meal was sold                        |
| Base Price            | Original meal price                                     |
| Emailer for Promotion | Indicates whether the meal was promoted through email   |
| Homepage Featured     | Indicates whether the meal was featured on the homepage |
| Week                  | Week of the year                                        |
| Year                  | Year of the observation                                 |
| Number of Orders      | Historical weekly meal demand                           |

Additional information is available through the fulfillment center and meal information datasets.


## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook


## 🔄 Project Workflow

### 1. Data Preprocessing

The dataset was prepared for machine learning through:

* Missing-value analysis
* Data cleaning
* Outlier analysis
* Feature transformation
* Categorical variable encoding
* Numerical feature processing


### 2. Exploratory Data Analysis

EDA was performed to investigate:

* Weekly demand trends
* Demand across fulfillment centers
* Meal-level demand
* Pricing relationships
* Promotional effects
* Demand variation over time


### 3. Feature Engineering

Additional features were created to improve model performance and capture relationships within the historical data.

The analysis considered factors such as:

* Time-related information
* Fulfillment center characteristics
* Meal characteristics
* Pricing
* Promotional indicators


## 🤖 Machine Learning Models

Three regression algorithms were trained and compared.

### 1. Linear Regression

Used as a baseline model to establish a reference level of predictive performance.

### 2. Decision Tree Regressor

Used to capture nonlinear relationships between the input features and meal demand.

### 3. Random Forest Regressor

An ensemble model combining multiple decision trees to improve predictive stability and reduce variance.


## 📏 Evaluation Metrics

The models were evaluated using:

### Mean Squared Error (MSE)

Measures the average squared difference between predicted and actual demand.

### R² Score

Measures how well the model explains the variance in the target variable.


## 📊 Model Comparison

The experiments showed that the models performed differently depending on their ability to capture nonlinear relationships in the data.

**Random Forest Regressor achieved the strongest overall performance among the tested models**, outperforming the baseline Linear Regression and Decision Tree approaches in the project experiments.


## 💡 Key Findings

* Historical demand contains meaningful patterns that can be used for forecasting.
* Demand varies across fulfillment centers and meal types.
* Pricing and promotional information can contribute to demand prediction.
* Tree-based models can capture nonlinear relationships more effectively than a simple linear baseline.
* Random Forest provided the best performance among the evaluated models.


## 🚀 Potential Improvements

Future versions could improve the forecasting system by incorporating:

* Weather information
* Public holidays
* Regional events
* More advanced time-series features
* Hyperparameter optimization
* Gradient Boosting models
* XGBoost
* LightGBM
* Neural-network-based forecasting
* Model deployment through an API or web application


## 📁 Repository Structure

```text
Food_Demand_Forecasting_Using_ML/
│
├── fulfilment_center_info.csv
├── meal_info.csv
├── train.csv
├── test.csv
├── sample_submission.csv
├── proj_final.ipynb
├── LICENSE
└── README.md
```

## ▶️ How to Run

Clone the repository:

```bash
git clone https://github.com/Kruti115/Food_Demand_Forecasting_Using_ML.git
```

Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

Open:

```text
proj_final.ipynb
```

Run the notebook cells sequentially to reproduce the analysis and model training process.


## 🎯 Skills Demonstrated

* Machine Learning
* Regression
* Data Preprocessing
* Feature Engineering
* Exploratory Data Analysis
* Model Evaluation
* Python
* Pandas
* NumPy
* Scikit-learn
* Data Visualization


## 👥 Project Credits

This project was developed collaboratively.

Special thanks to **[Solanki Milan](https://github.com/Miilan13)** for their contributions to the project.


## 👩‍💻 Author

**Kruti Gupta**

GitHub: https://github.com/Kruti115

LinkedIn: https://www.linkedin.com/in/kruti-gupta-data/

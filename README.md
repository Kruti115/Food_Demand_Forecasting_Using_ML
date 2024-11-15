# Machine Learning Based Food Demand Forecasting

## Credits

This project was a collaborative effort. Special thanks to Solanki Milan (https://github.com/Miilan13) for their contributions and hard work on this project.

##  Introduction

Meal demand in different fulfillment centers is mainly forecasted using machine learning models for optimal management of resources and inventories. Such a forecasting will improve service efficiency in meal delivery and avoid lots of wastage.

The requirement for meals in advance is the best way to reduce waste, increase supply, and optimize the use of systems at play within the fulfillment center, especially during peak order surges. The right estimates enable the fulfillment center to use available resources to the best of their abilities. Good estimates are crucial because, especially in cases where there's a peak in orders, it's essential that this aspect can be well predicted. This project aims to develop a predictive model for weekly meal demand using historical data.

## Dataset
The historical orders dataset contains an amount of meals ordered across various fulfillment centers. Features are:
- **Center ID**: It is an identifier for the fulfillment center.
- **Meal ID**: Unique identifier of the meal.
- **Checkout Price**: Price at which meal has been checked out.
- **Base Price**: Original price of meal.
- **Emailer for Promotion**: Whether meal is mailed to them for promotion.
- **Homepage Featured**: Whether meal was featured on top of the page
- **Week**: Week of the year.
- **Year**: Year in which date is input.
Total Orders This is the total number of orders for the meal in the week. 

## Exploratory Data Analysis
EDA gave insight into the kind of data structure and trends involved. The most important visualizations include:
Weekly Demand Over Time: This was shown to account for the general pattern for demand.
Demand by Fulfillment Center: These accounted for which centers were more in demand.
Demand by Meal Type: This helped to identify which type of meals were in more demand.

## Research Approach
### Data Preprocessing
- **Data Cleaning**: Resolved the missing values and outliers in the data.
- **Feature Engineering**: Generated additional features to improve the accuracy of the model.
- **Data Transformation**: Normalized numeric features and encoded categorical features.

### Modeling
Three machine learning algorithms practiced were used to make predictions of demand in meals.
1.  **Linear Regression**: This is a simple model and used as a benchmark for comparison.
2.  **Decision Tree Regressor**: Such models will readily capture any non-linear pattern within the data.
3. **Random Forest Regressor**: An ensemble model where the output averaged from multiple decision trees helps in reducing the variance.

### Evaluation Metrics
The evaluation was done using the following metrics:
- **Mean Squared Error (MSE)**: Average of the squares of errors.
- **R-squared**: The R-squared value measures the goodness of fit of the model, that is, how well it explains the variance in the data.
## Results
We have for comparison:
- **Linear Regression**: The base. The accuracy is fairly moderate.
- **Decision Tree Regressor**: Now this is a model that has outperformed the previous ones, because now it will be able to capture some form of nonlinear relationship.
- **Random Forest Regressor**: Best result so far, more accurate and even less error due to averaging of the ensemble.
This project exhibits the capability of machine learning models for effective utilization in the task of demand forecasting based on historical data. The best performance was achieved by the Random Forest model, thus making the model suitable for actual applications in meal delivery services' demand forecasting.

### Future Improvements

- More Features: Weather, holidays, and regional events may all enhance the prediction results.
- Hyperparameter Tuning of Models' Parameters: The performance may increase with parameters being hyper-tuned for models.
- Try Other Models: Accuracy levels would probably be higher if one used Gradient Boosting or Neural Networks.

## Installing

Run with the following steps
1. Clone the repository: `git clone https://github.com/Kruti115/Food_Demand_Forecasting_Using_ML`
2. Install all packages: `pip install -r requirements.txt
3. Execute the notebook or script to view the findings and the results.

## References

- Scikit-learn Documentation
- Pandas Documentation
- Food Demand Prediction using Statistical and Machine Learning Models
- Demand Forecasting for Food Production Using Machine Learning Algorithms: A Case Study of University Refectory

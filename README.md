# Predictive Modeling for Retail Purchase Behavior

## Introduction

Understanding consumer behavior is crucial for business success in today's retail landscape. This project delves into a dataset comprising over half a million consumer transactions, encompassing key demographic and transactional attributes like User_ID, Product_ID, Gender, Age, Occupation, City_Category, Marital_Status, Product_Category, and Purchase amount.

We aim to develop a predictive model that accurately forecasts purchase amounts based on these attributes. The insights from this model will help businesses optimize marketing strategies, inventory management, and customer experiences.

### Central Question:
**Using machine learning techniques, how accurately can we predict purchase amounts based on demographic and transactional attributes?**  
This can help Walmart stock its inventory precisely.

## Data Collection Process

The dataset used in this project was sourced from Kaggle. The data collection process involved:
1. Searching for relevant datasets using keywords related to retail and Walmart on the Kaggle platform.
2. Downloading the selected datasets following Kaggle's terms of use and associated licensing agreements.
3. Thoroughly evaluating the datasets based on completeness, relevance to the research objectives, and data quality.
4. Uploading the dataset to Python for further analysis and preprocessing.

You can check the data here: https://www.kaggle.com/datasets/sachinbagale/walmart-data/data

## Data Summary and Visualization

### Dataset Columns:
1. **User_ID**: Unique identifiers for users.
2. **Product_ID**: Unique identifiers for products.
3. **Gender**: Gender of the users.
4. **Age**: Age of the users.
5. **Occupation**: Occupation of users.
6. **City_Category**: Category of the city where users reside.
7. **Stay_In_Current_City_Years**: Duration of users' stay in their current city.
8. **Marital_Status**: Marital status of users.
9. **Product_Category**: Category of the purchased product.
10. **Purchase**: Purchase amount or price of the product.

### Data Insights:
- The dataset contains 3631 unique products spread across 20 categories.
- The most prevalent product category is category number 5.
- The largest demographic of customers is males, aged 26-35, with occupations in level 4.
- Most purchases originated from Type B cities, and the highest number of purchases was made by unmarried individuals.

### Feature Engineering:
1. **Gender Conversion**: Transformed from categorical values ('M' and 'F') to binary (1 for 'M', 0 for 'F').
2. **Marital Status Conversion**: Converted from categorical values ('Married' and 'Unmarried') to binary (0 for 'Married', 1 for 'Unmarried').
3. **Age Conversion**: The age column was cleaned by removing symbols and converted into a median age for more accurate representation.
4. **Stay_In_Current_City_Years**: Replaced all values above 4 with 4, indicating customers staying for more than 4 years.

## Machine Learning Model

### Chosen Model:
We chose a **Neural Network** for the following reasons:
1. **Complex Patterns**: Neural networks excel at capturing intricate relationships in data, making them suitable for predicting purchase amounts.
2. **Feature Learning**: They automatically learn relevant features from raw data, reducing the need for manual feature engineering.
3. **Scalability**: Neural networks efficiently handle large datasets, ideal for processing over half a million consumer transactions.
4. **Performance**: Neural networks often outperform traditional models in regression tasks like predicting purchase amounts.
5. **Adaptability**: Neural networks can adapt to changing consumer preferences and market trends.

### Model Architecture:
- We used **linear activation** for the output layer and **ReLU activation** for hidden layers, with a dense network structure.

## Model Evaluation Metrics

1. **Mean Absolute Error (MAE)**: 0.4518, indicating the model's predictions are, on average, off by $0.45.
2. **Mean Squared Error (MSE)**: 0.3636, showing low variance in prediction errors.
3. **Root Mean Squared Error (RMSE)**: 0.6030, reflecting the average error magnitude in dollars.
4. **R-squared (R²)**: 0.6349, meaning the model explains 63.49% of the variability in purchase amounts.

### Model Performance:
- The model does well in terms of generalization, with a higher R² value indicating that the model captures significant patterns in consumer spending behavior.
- The training loss being higher than the validation loss suggests that the model generalizes well to unseen data and avoids overfitting.

## Visualization

- **Regression Plot**: Shows that the relationship between predictor variables and purchase amounts is somewhat nonlinear. Outliers significantly influence the regression line, particularly at higher purchase amounts.
- **Loss Curve**: Training loss is higher than validation loss, indicating the model does not overfit the training data.

## Results and Conclusions

- The model is effective in predicting purchase amounts, with good performance in MAE, MSE, and R².
- The insights from the model can be used to optimize inventory levels, personalize marketing efforts, and improve pricing strategies.

### Suggestions Based on Predictions:
1. **Optimize Inventory and Supply Chain**: Forecast demand to optimize inventory levels, reduce carrying costs, and enhance supply chain efficiency.
2. **Customer-Centric Approach**: Use predictions for personalized recommendations, targeted promotions, and better customer experiences.
3. **Pricing Strategies**: Adjust prices based on predicted consumer behavior to maximize revenue and minimize stockouts or overstock situations.

## Future Recommendations

- **Outlier Treatment**: Proper treatment of outliers could help improve the model’s efficiency and prediction accuracy, particularly for higher purchase amounts.
- **Model Enhancements**: Implementing more advanced models or hyperparameter tuning may improve the model’s performance further.



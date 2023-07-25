## Simple Linear Regression for Dollar Value Prediction

### Introduction
This project aims to perform a simple linear regression analysis to predict the future dollar value based on historical data spanning from 1800 to 2021. The dataset contains columns for year, dollar value, buying power, and inflation rate. The primary focus is to establish a linear relationship between the year and dollar value and use it to predict the dollar value for the year 2022.

### Dataset
The dataset used for this analysis is stored in a CSV file named "dollar_inflation.csv." obtained from kaggle. It contains historical data for different years and their corresponding dollar values. The dataset has been cleaned to remove the year 2022, which had a value labeled as #VALUE.

### Dependencies
To run this project, the following libraries are required:
- pandas
- numpy
- seaborn
- matplotlib
- scikit-learn (for the Linear Regression model)

### Methodology
1. Data Loading and Exploration:
   - The data is loaded into a pandas DataFrame.
   - Initial exploration of the data is performed by viewing the first and last five rows of the dataset to ensure proper loading.
   - The dimension of the dataset is checked using the `shape` attribute.
   - Information about the data columns, non-null value counts, and data types are obtained using the `info()` method.

2. Data Cleaning:
   - The year 2022, which had a #VALUE entry, is removed from the dataset to ensure data consistency and reliability.

3. Data Visualization:
   - The correlation matrix is visualized using a heatmap from the seaborn library to understand the relationships between different variables. The primary focus is on the correlation between the year and dollar value.

4. Model Training:
   - The dataset is split into training and testing sets using a 70-30 split ratio.
   - The linear regression model from scikit-learn is imported, and the model is trained on the training set.

5. Model Evaluation:
   - The model's performance is evaluated using the R-squared (R2) score, which measures how well the model predicts the dollar value based on the year.
   - The R2 score is calculated for the test set and presented as a percentage.

6. Prediction for 2022:
   - The trained model is used to predict the dollar value for the year 2022 based on the linear regression equation.

### Results and Discussion
The linear regression model achieved an accuracy of approximately 54% in predicting the dollar value based on the year. This suggests that the year and dollar value have a moderate linear correlation. The R-squared score of 54% indicates that 54% of the variance in the dollar value can be explained by the year.

### Future Improvements
To improve the accuracy of the prediction model, several enhancements can be considered:
- Feature Engineering: Introduce additional relevant features, such as economic indicators, GDP, or interest rates, to capture more complex relationships.
- Polynomial Regression: Explore polynomial regression models to capture nonlinear relationships between the year and dollar value.
- Larger Dataset: Obtain a larger dataset spanning a more extended period to improve the model's training and generalization.

### Conclusion
This project demonstrates the application of simple linear regression to predict future dollar values based on historical data. The model's accuracy at 54% indicates a moderate linear correlation between the year and dollar value. While the model shows promising results, further improvements and explorations into more sophisticated modeling techniques could yield even better predictions.

---

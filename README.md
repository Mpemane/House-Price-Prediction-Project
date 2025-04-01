# House Price Prediction Project

## Overview

This project aims to predict house prices using machine learning models. The dataset contains various features related to property characteristics, and the goal is to build a model that accurately predicts the price. The project covers data preprocessing, exploratory data analysis, model selection, training, and evaluation.

## Dataset

The dataset used is `Inca Tribe House Prices.csv`. It includes the following features:

-   `Type`: The type of property (e.g., apartment, house, villa).
-   `Price`: The price of the property (target variable).
-   `Bedrooms`: The number of bedrooms.
-   `Bathrooms`: The number of bathrooms.
-   `Area`: The size of the property.
-   `Furnished`: Indicates whether the property is furnished.
-   `Level`: The floor level of the property.
-   `Compound`: The compound or community where the property is located.
-   `Payment_Option`: Available payment options.
-   `Delivery_Date`: Expected or actual delivery date.
-   `Delivery_Term`: Terms of delivery.
-   `City`: The city where the property is located.

## Libraries Used

-   `pandas`: For data manipulation.
-   `numpy`: For numerical operations.
-   `seaborn` and `matplotlib`: For data visualization.
-   `scikit-learn`: For machine learning models and evaluation.
-   `missingno`: For visualizing missing data.

## Project Structure

-   `Inca Tribe House Prices.csv`: The dataset.
-   `House_Project.ipynb`: Jupyter Notebook containing the code and analysis.
-   `README.md`: Project documentation.

## Methodology

1.  **Data Loading and Exploration:**
    -   Loaded the dataset using `pandas`.
    -   Explored the data using `info()` and `describe()`.
    -   Visualized data distributions and correlations using `seaborn` and `matplotlib`.

2.  **Data Preprocessing:**
    -   Handled missing values by identifying and imputing or dropping columns based on the percentage of missing data.
    -   Converted "unknown" values to `NaN`.
    -   Imputed missing numerical values with the mode.
    -   Encoded categorical variables using `LabelEncoder`.

3.  **Model Selection and Training:**
    -   Selected three regression models: Linear Regression, Decision Tree, and Random Forest.
    -   Split the data into training and testing sets.
    -   Trained the models on the training data.

4.  **Model Evaluation:**
    -   Evaluated the models using Root Mean Squared Error (RMSE).
    -   Performed k-fold cross-validation to assess model robustness.
    -   Visualized predictions vs. actual values.

## Results

-      Random Forest performed the best, exhibiting the lowest RMSE in both single train test split and cross validation.
-      Linear regression performed reasonably well, but the large difference between the single train test split and cross-validation shows that the model is very sensitive to the training data.
-   Decision Tree showed the highest RMSE, indicating it was the least accurate.

## Conclusion

The Random Forest model is the most effective for predicting house prices in this dataset, demonstrating a superior balance of accuracy and robustness.

**Key Findings:**

-   **Significant Factors:** The number of bathrooms and the area of the property are the most significant factors influencing house prices. The city and property type also play notable roles.
-   **Model Reliability:** Given the variability in Linear Regression results, relying on Random Forest is recommended for more consistent and accurate predictions.
-   **Data Complexity:** The Random Forest model's success highlights the importance of capturing complex, non-linear relationships within the data.

**Recommendations:**

-      Further investigation into feature interactions could potentially enhance the model's performance.
-   Exploring additional data preprocessing techniques may also lead to improved accuracy.
-   Given the Random Forest models' proven reliability, it should be the model of choice for future predictions.

## How to Run

1.  Ensure you have Python and the required libraries installed.
2.  Clone the repository.
3.  Place `Inca Tribe House Prices.csv` in the same directory as `House_Project.ipynb`.
4.  Open and run the Jupyter Notebook `House_Project.ipynb`.

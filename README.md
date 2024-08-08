# Project Title: House Sales Price Prediction in King County, USA using Feed Forward Neural Networks

## About Dataset:

This dataset contains house sale prices for King County, which includes Seattle. It includes homes sold between May 2014 and May 2015.


| Column            | Type        | Description                                                                                      |
|-------------------|-------------|--------------------------------------------------------------------------------------------------|
| `id`              | Categorical | Unique identifier for each house.                                                                |
| `date`            | Numerical   | Date when the house was sold.                                                                    |
| `price`           | Numerical   | Sale price of the house.                                                                         |
| `bedrooms`        | Numerical   | Number of bedrooms in the house.                                                                 |
| `bathrooms`       | Numerical   | Number of bathrooms in the house.                                                                |
| `sqft_living`     | Numerical   | Size of the living area in square feet.                                                          |
| `sqft_lot`        | Numerical   | Size of the lot in square feet.                                                                  |
| `floors`          | Numerical   | Total number of floors in the house.                                                             |
| `waterfront`      | Categorical | Indicates whether the property has a waterfront (`1` for yes, `0` for no).                      |
| `view`            | Categorical | Index from 0 to 4 representing the quality of the view.                                          |
| `condition`       | Categorical | Condition of the house, ranked from 1 to 5.                                                      |
| `grade`           | Categorical | Classification by construction quality, referring to the materials used and quality of workmanship. |
| `sqft_above`      | Numerical   | Square footage of the house above ground.                                                        |
| `sqft_basement`   | Numerical   | Square footage of the basement.                                                                  |
| `yr_built`        | Numerical   | Year when the house was built.                                                                   |
| `yr_renovated`    | Numerical   | Year when the house was renovated (0 if never renovated).                                        |
| `zipcode`         | Categorical | 5-digit zip code of the house location.                                                           |
| `lat`             | Numerical   | Latitude coordinate of the house.                                                                |
| `long`            | Numerical   | Longitude coordinate of the house.                                                               |
| `sqft_living15`   | Numerical   | Average size of interior living space for the 15 closest houses, in square feet.                 |
| `sqft_lot15`      | Numerical   | Average size of land lots for the 15 closest houses, in square feet.                             |


Link : [https://www.kaggle.com/datasets/mssmartypants/paris-housing-price-prediction](https://www.kaggle.com/datasets/harlfoxem/housesalesprediction/data)


## Table of Contents:
1. Preliminary Data Analysis
2. Exploratory Data Analysis
3. Data Splitting
4. Data Preprocessing
5. Complete Model Workflow Definition
6. Hyperparameter Definition and Workflow Execution
7. Results
8. Conclusion


## Results and Plots:

**Best Model according to highest R2 Score:** 
![image](https://github.com/user-attachments/assets/149da8f2-3187-4cfd-9cd8-20f718f5ef5b)

|model|	model5|
|-----|-------|
|MAE	|80623.663126|
|R2	  |0.822598|

**Best Model according to lowest MAE Score:** 

![image](https://github.com/user-attachments/assets/4bba1365-506b-4ba3-bc36-6edb253537aa)


|model|	model5|
|-----|-------|
|MAE	|78426.093104|
|R2	  |.818078|

## Conclusion and Future Improvement:

In this project, I followed a comprehensive approach to house price prediction, focusing on the following aspects:

1. **Data Preprocessing:**
   - Normalization was not used during preprocessing.
   - Performed standard data analysis and exploratory data analysis (EDA) to understand and prepare the data.

2. **Model Building Workflow:**
   - Defined a structured workflow for building, compiling, fitting, and evaluating the model.
   - Created a function for data splitting to streamline the model training process.

3. **Model Architecture and Hyperparameters:**
   - Designed and tested a hyperparameter grid consisting of 11 models with various architectures and configurations. This included:
     - Different numbers of hidden layers and neurons.
     - Variations in dropout rates, batch normalization, and regularization methods.
   - Evaluated models based on Mean Absolute Error (MAE) and R-squared (R²) scores.

4. **Best Model Selection:**
   - Chose the final model based on the highest R² score, indicating the best explanation of variance in house prices.
   - The selected model features the following architecture:
     - **Hidden Layers:** 5 layers with [256, 128, 64, 32, 16] neurons.
     - **Activation Function:** ReLU.
     - **Dropout Rate:** None.
     - **Batch Normalization:** Not used.
     - **Kernel Regularization:** L1L2 with \( l1 = 1e-3 \) and \( l2 = 1e-3 \).

5. **Model Performance:**
   - The final model has a high R² score and a relatively low MAE difference (around 2000) compared to other models, indicating that there is no significant error rate in predicting house prices.

6. **Future Improvements:**
   - There is potential for further enhancement by exploring a wider range of hyperparameters, testing larger model architectures, and incorporating normalization techniques.
   - Removing Outliers and using Normalization, may perform better result!

This structured approach ensures that the model is robust and effective in predicting house prices, while also providing a solid foundation for future improvements and refinements.

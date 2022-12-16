# A_B_Testing
Perform post-hoc correction using pairwise chi-square tests on five tested website versions based on the Montana Library case study

![grafik](https://user-images.githubusercontent.com/100354393/208067598-55360558-c73a-4246-a0ae-36bb607f7603.png)

# Use Case

Data and use case for this project is taken from a Case study that tried to improve library user experience with A/B testing. Process and principles of this
study have been published in the Journal of Library Usere Experience here: (https://doi.org/10.3998/weave.12535642.0001.101)



# Goal
The task is to create a model that predicts the price of a house based on its characteristics
The project will be divided into two major phases:
1. Create a model to predict whether a house is expensive or not. 
2. Create a model to predict the exact price of a house.


# Data Set 
The Ames Housing dataset was compiled by Dean De Cock for use in data science education. It's analternative for data scientists looking for a modernized and expanded version of the often cited Boston Housing dataset. 
This Dataset is used in the following Kaggle Competition: 
> "House Prices - Advanced Regression Techniques. Predict sales prices and practice feature engineering, RFs, and gradient boosting"

The dataset contains 79 explanatory variables describing (almost) every aspect of residential homes in Ames, Iowa
The datsate contains the prices and explanatory variables for a sample of 1460 houses. 

[Here you can find the dataset and also an overview of the competition](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques)

# Skills/Methods
- Creative feature engineering 
- Advanced regression techniques like random forest and gradient boosting
- Apply One-Hot-Encoding for preprocessing
- Use scikit-learn Pipelines 
- Use GridSearch in combination with cross validation for model tuning
- Implementation with scikit-learn
- Deploy classification performance metrics for classification task
- explore feature selection techniques and dimensionality reduction with PCA
- first deployment wit streamlit  


## Basic Steps in this Project: 

![grafik](https://user-images.githubusercontent.com/100354393/205448382-c7258c89-05cf-4d90-ae76-f30fe592669d.png)

1. Explore & clean the data 
2. Data preprocessing
3. Modelling 
4. Model Tuning using GridSearch in combination with Cross Validation
5. Model Evaluation      
--> [Associated notebook for classification task: Predicting if house is expensive or not](../main/housing_prices_model_classification.ipynb)      
--> [Associated notebook for regression task](../main/housing_prices_model_regression.ipynb)  
5. Further exploratuons: Performance after dimensionality reduction with PCA 
--> [Associated notebook](../main/housing_prices_regression_pca.ipynb) 
4. Further explorations: Feature selection techniques 
--> [Associated notebook](../main/feature_selection_housing_prices.ipynb) 
5. Take part at kaggle competion
--> [Associated notebook](../main/kaggle_competition_feature_selection_housing_prices_model.ipynb)
6. Deploy the model using streamlit 

## Files in this repository
- [Description of the features](../main/data_description.txt)
- [Notebook for classification task: Predicting if house is expensive or not](../main/housing_prices_model_classification.ipynb)      
- [Notebook for regression task](../main/housing_prices_model_regression.ipynb)  

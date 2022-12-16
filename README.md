# A_B_Testing
Perform post-hoc correction using pairwise chi-square tests on five tested website versions based on the Montana Library case study

![grafik](https://user-images.githubusercontent.com/100354393/208067598-55360558-c73a-4246-a0ae-36bb607f7603.png)

# Use Case
Data and use case for this project is taken from a Case study that tried to improve library user experience with A/B testing. Process and principles of this
study have been published by the author Scott W. H. Young in the Journal of Library User Experience here:   
[Young, Scott W.H. (2014). Improving Library User Experience with A/B Testing: Principles and Process. Weave, Journal of Library User Experience, Volume 1(Issue 1), doi:https://doi.org/10.3998/weave.12535642.0001.101.](https://doi.org/10.3998/weave.12535642.0001.101)

The library tried to improve their website. The analysing team found the following interaction pattern: Below the library picture, there was search bar and three big items: “Find”, “Request” and “Interact” (like in the picture at the top of this file). All three of them contained access to important information and services that the library prides itself in offering. However, the Website Analytics show that the “Interact” button has, ironically, almost no interactions. 

We cite from the report:       

      The click-through rate for Find was 35%, Request was 6%, and Interact was 2%. This observation prompted a question: “Why are Interact clicks so low?”   
      At this time, the content beneath Interact included links to Reference Services, Instruction Services, Subject Liaisons, Writing Center, About,    
      Staff Directory, Library FAQ, Give to the Library, and Floor Maps. The library’s web committee surmised that introducing this category with the    
      abstract term “Interact” added difficulty and confusion for users trying to navigate into the library website homepage. Four    
      different category titles were then proposed as variations to be tested: Connect, Learn, Help, and Services.

So after conduction further interviews with the users and some brainstorming, the website team settled on 4 different new versions to test against the original “Interact” button:
- Connect
- Learn
- Help
- Services

The metrics that were deemed relevant enough to be tracked were the following: 
- Click-through rate (CTR) for the homepage. Amount of clicks on the button divided by the total visits to the page. Selected as a measure of the initial ability of the category title to attract users
- Drop-off rate for the category pages. Percentage of visitors who leave the site from a given page, selected as a measure of the ability of the category page to meet user expectations.
- Homepage-return rate for the category pages. Percentage of users who navigated from the library homepage to the category page, then returned back to the homepage. This sequence of actions provides clues as to whether a user discovered the desired option on the category page; if not, the user would likely return to the homepage to continue navigation. Homepage-return rate was therefore selected as a measure of the ability of the category page to meet user expectations.   

# Goal
While all the metrics will be relevant for the decision-making process, it was decided that for a version to be considered superior, a **minimum increase in click-through rate of 30%** had to be detected.   

The hypotheses to be tested in the experiment are the following:
- Null Hypothesis: all versions have the same Click Through Rate (CTR).
- Alternative Hypothesis: there is a difference in the CTR for the different versions.

The desired Statistical Significance was chosen to be 90%: it is a bit lower than the usual scientific standard of 95% because the consequences of rejecting the null hypothesis when it is true (i.e. concluding there is an effect when there is none) are not tragic, and there are constraints in the amount of time the team of experimenters have: quickness was prioritized over certainty.


# Data Set 

The data can be downloaded also on the Montana State University library webpage, [here](https://scholarworks.montana.edu/xmlui/handle/1/3507).
It has been extracted from [crazyegg](https://www.crazyegg.com/), a service that tracks traffic to websites and provides insights and well-structured data. 

The data has been sampled from April 3, 2013 – April 10, 2013 and included 10.819 visits to the library homepage,


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

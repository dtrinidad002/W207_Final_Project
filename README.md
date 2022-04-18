 # Kaggle: House Prices - Advanced Regression Techniques
 https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/overview
 ## W207 Final Project- David Trinidad (Fall 2022)

## Project scope:
For my final project I chose the housing prices prediction competition. The goal is to develop a machine learning model to predict the sales price from the testing data set. I chose this project because it is pretty straight forward and I anticipate that I will be utilizing Linear Regression for the majority of my Data Science Career. 

### Proeject Files:

**PowerPoint Presentation** (Presentation.pptx)

   **-----------Data------------------**

    a. original test data (test.csv)
    b. orignal training data (train.csv)
    c. Baseline Sales prediction data (baseline_submission.csv
    d. Final Submission (final_Submission1.csv)
    e. Cleaned Data (clean_df.csv)

**-------Jupyter Notebooks-------**
   
## Notebook 1: Baseline Submission 
The goal in this notebook was merely just to load the data, do some minor cleaning, then plugging it into a basic linear model using sklearn. My kaggle score for was 0.20640 ranking me 3518 out of 4312. 

##  Notebook 2: EDA, DataCleaning, Feature Engineering, Regression Model Development   
In this notebook I read and explore the data set deeply to establish a strategy for my feature engineering. This is a continuation from my initial baseline notebook where i did a soft EDA, mainly addressing null values, then running a basic linear regression to predict the 'SalesPrice' from the test training set. Below is an outline summarizing the two main parts of this notebook

**Pt.1 Reading the dataset**
The data set included from Kaggle includes a training.csv (1460x81) and a test.csv file (1459x80). The data types include floats (3), integers(35) and categorical objects (43). 

**Pt.2 Missing Data**
The majority of the NA/missing data is observed within the object data type. It's my assumption that most of these are a mix of Nominal data where the entries carry no numerical value and Oridinal which do (i.e OverallQuality)

**Pt.3 Data Visualization** 

<u>*a.Sales Price Distribution*</u> To visualize the sales data i created a distribution plot and a box-plot. The distribution plot displays a a semi-bell shape which is slightly skewed to the right, indicating that the data follows a normal distribution which should work well with machine learning models. The box plot shows that there are some outliers in the data which I may consider removing from the training data set.
 
<u>*a.Correlation Heatmap*</u> I executed a correlation matrix with the training data set and the features that demonstrated the highest correlation to Saleprice is  ['GrLivArea','OverallQual', '1stFlrSF', 'GarageCars']  

<u>*b.Pairwise Plots:*</u> I executed a pairwise plot utilizing the features with the highest correlation to sales price to gather additional insight.

<u>*c.Linear regression Plot:*</u> GrLivArea(X), with SalesPrice(Y). We noticed two data outliers where an extremely high Ground Living Area resulted to an extremely low sales price. This is something I'll consider addressing when doing feature engineering. 

<u>*d.Scatter Plot for New Feature "TotalSF" [total Square footage]

**Pt.4 Data Cleaning and Data engineering**  
    a. handling missing values
    b. converting categoricals to numerical using label-encoding. 

**Pt.5 Regression Modelling** - Calculating Root Mean Squared using default parameters for the models below. We then determine the best parameters to get the lowest root mean squared error using GridSearchCV method. 
     a.Lasso  
     b.RandomForestRegressor  
     c.ElasticNet  
     d.KernelRidge  
     e.GradientBoostingRegressor

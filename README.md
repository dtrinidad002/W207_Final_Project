 # Kaggle: House Prices - Advanced Regression Techniques
 https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/overview
 ## W207 Final Project- David Trinidad (Fall 2022)

## Project scope:

Ask a home buyer to describe their dream house, and they probably won't begin with the height of the basement ceiling or the proximity to an east-west railroad. But this playground competition's dataset proves that much more influences price negotiations than the number of bedrooms or a white-picket fence.

With 79 explanatory variables describing (almost) every aspect of residential homes in Ames, Iowa, this competition challenges you to predict the final price of each home.

Practice Skills
Creative feature engineering 
Advanced regression techniques like random forest and gradient boosting

### Proeject Files:
   **-----------Data------------------**

    a. original test data (test.csv)
    b. orignal training data (train.csv)
    c. Baseline Sales prediction data (baseline_submission.csv
    d. Final prediction outpiut data (test_score.csv)

**-------Jupyter Notebooks-------**
    
   
## ---------------------- Summary of Notebook 2: Baseline Submission --------------------- 
The goal in this notebook was merely just to load the data, do some minor cleaning, then plugging it into a basic linear model using sklearn. My kaggle score for was 0.20640 ranking me 3518 out of 4312. 

## ---------------------- Summary of Notebook 2: EDA, DataCleaning, Feature Engineering, Regression Model Development ---------------------    
In this notebook I read and explore the data set deeply to establish a strategy for my feature engineering. This is a continuation from my initial baseline notebook where i did a soft EDA, mainly addressing null values, then running a basic linear regression to predict the 'SalesPrice' from the test training set. Below is an outline summarizing the two main parts of this notebook

**Pt.1 Reading the dataset**
The data set included from Kaggle includes a training.csv (1460x81) and a test.csv file (1459x80). The data types include floats (3), integers(35) and categorical objects (43). 

**Pt.2 Missing Data**
The majority of the NA/missing data is observed within the object data type. It's my assumption that most of these are a mix of Nominal data where the entries carry no numerical value and Oridinal which do (i.e OverallQuality)

**Pt.3 Data Visualization** 

<u>*a.Sales Price Distribution*</u> To visualize the sales data i created a distribution plot and a box-plot. The distribution plot displays a a semi-bell shape which is slightly skewed to the right, indicating that the data follows a normal distribution which should work well with machine learning models. The box plot shows that there are some outliers in the data which I may consider removing from the training data set.
 
<u>*a.Correlation Heatmap*</u> I executed a correlation matrix with the training data set and the features that demonstrated the highest correlation to Saleprice is  ['GrLivArea','OverallQual', '1stFlrSF', 'GarageCars']  

<u>*b.Pairwise Plots:*</u> I executed a pairwise plot utilizing the features with the highest correlation to sales price to gather additional insight. The output of the Pairwise plot included histograms, and scatter plots. Each histogram resembles a bell shape of some sort which is indicative of a normal distribution. Each scatter plot displayed a positive increase directionally. 

<u>*c.Linear regression Plot:*</u> GrLivArea(X), with SalesPrice(Y). We noticed two data outliers where an extremely high Ground Living Area resulted to an extremely low sales price. This is something I'll consider addressing when doing feature engineering. 

<u>*d.Plotting OverallQual with Sales Price:*</u> We observe a positive with an increase which makes a lot of sense
Since this feature is ordinal, I will utilize dummy variables encoding during the feature engineering

**Pt.4 Data Cleaning and Data engineering**  

    a. handling missing values  
    b. handling missing values   


**Pt.5 Regression Modelling** 

     a.Lasso  
        b.RandomForestRegressor  
        c.ElasticNet  
        d.KernelRidge  
        e.GradientBoostingRegressor



(Link to video explanation??)

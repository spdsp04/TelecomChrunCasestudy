# Telecom Churn Prediction Group Case Study
![model_770_450](https://user-images.githubusercontent.com/93203186/162379677-1c04dcae-e48e-4790-b7ea-c7ab74101faf.jpg)

## Problem Statement
### Business Problem Overview
In the telecom industry, customers are able to choose from multiple service providers and actively switch from one operator to another. In this highly competitive market, the telecommunications industry experiences an average of 15-25% annual churn rate. Given the fact that it costs 5-10 times more to acquire a new customer than to retain an existing one, customer retention has now become even more important than customer acquisition.

For many incumbent operators, retaining high profitable customers is the number one business
goal. To reduce customer churn, telecom companies need to predict which customers are at high risk of churn. In this project, you will analyze customer-level data of a leading telecom firm, build predictive models to identify customers at high risk of churn.

In this competition, your goal is to build a machine learning model that is able to predict churning customers based on the features provided for their usage.

## Main Goals:
The main goal of the case study is to build ML models to predict churn. The predictive model that you’re going to build will the following purposes:
- It will be used to predict whether a high-value customer will churn or not, in near future (i.e. churn phase). By knowing this, the company can take action steps such as providing special plans, discounts on recharge etc.

- It will be used to identify important variables that are strong predictors of churn. These variables may also indicate why customers choose to switch to other networks.

- Even though overall accuracy will be your primary evaluation metric, you should also mention other metrics like precision, recall, etc. for the different models that can be used for evaluation purposes based on different business objectives. For example, in this problem statement, one business goal can be to build an ML model that identifies customers who'll definitely churn with more accuracy as compared to the ones who'll not churn. Make sure you mention which metric can be used in such scenarios.

- Recommend strategies to manage customer churn based on your observations.

Note that it's highly likely that you'll need to build multiple models to fulfil the objectives mentioned in Points 1 and 2.  Since here, you have a large number of attributes, and thus you should try using a dimensionality reduction technique such as PCA and then build a predictive model. After PCA, you can use any classification model.

The above model will only be able to achieve one of the two goals - to predict customers who will churn. You can’t use the above model to identify the important features for churn. That’s because PCA usually creates components that are not easy to interpret.

Therefore, build another model with the main objective of identifying important predictor attributes which help the business understand indicators of churn. A good choice to identify important variables is a logistic regression model or a model from the tree family. 

### Suggested Steps

In the competition link, check the Code tab for the Starter Notebook that you can use as a reference for this entire case study. Some of the steps that you can use are as follows:
- Data Understanding, Preparation, and Pre-Processing:
  - Data understanding, identification of potentially useful and non-useful attributes and variable importance and impact estimation
  - Data preparation, performing data cleaning, missing values imputation, outlier removal, and column level standardization (for e.g., date, etc.) into one format
- Exploratory Data Analysis:
  - Performing basic preliminary data analysis including finding the correlation between variables and scatter plots to identify relationships between variables
  - Performing advanced data analysis, including plotting relevant heatmaps, histograms, and basic clustering to find patterns in the data
- Feature Engineering and Variable Transformation:
  - Feature engineering and performing one or more methods on attributes that can lead to the creation of a new potentially useful variable; for e.g., day from the date
  - Variable transformation and applying categorical variable transformations to turn into numerical data and numerical variable transformations to scale data
- Model Selection, Model Building, and  Prediction :
  - Identifying the type of problem and making a list of decisive models from all available choices
  - Choosing a training mechanism; for e.g., cross-validation, etc., and tuning hyperparameters of each model
  - Testing each model on the respective model evaluation metric
  - Choosing the best model based on the fit of the data set and output variable
  - Using ensemble options to improve the efficacy based on the evaluation metric stated in the problem


### Understanding Customer Behaviour During Churn
Customers usually do not decide to switch to another competitor instantly, but rather over a period of time (this is especially applicable to high-value customers). In churn prediction, we assume that there are three phases of customer lifecycle :

The ‘good’ phase: In this phase, the customer is happy with the service and behaves as usual.

The ‘action’ phase: The customer experience starts to sore in this phase, for e.g. he/she gets a compelling offer from a competitor, faces unjust charges, becomes unhappy with service quality etc. In this phase, the customer usually shows different behaviour than the ‘good’ months. Also, it is crucial to identify high-churn-risk customers in this phase, since some corrective actions can be taken at this point (such as matching the competitor’s offer/improving the service quality etc.)

The ‘churn’ phase: In this phase, the customer is said to have churned. You define churn based on this phase. Also, it is important to note that at the time of prediction (i.e. the action months), this data is not available to you for prediction. Thus, after tagging churn as 1/0 based on this phase, you discard all data corresponding to this phase.

In this case, since you are working over a four-month window, the first two months are the ‘good’ phase, the third month is the ‘action’ phase, while the fourth month is the ‘churn’ phase.

## Technologies Used

- NumPy version: 1.21.5

- Pandas version: 1.3.5

- Seaborn version: 0.11.2

- Sklearn

- Statsmodels

- matplotlib

- All libraries are fully updated as homework was done on Google colab later file was uploaded to github. 

## Top 10 High customer predicting churn variable

- arpu_6 : Average revenue per user on month_6 
- offnet_mou_8 : outside the operator network with Minutes of usage voice calls on month_8 
- roam_og_mou_8 : outgoing roaming calls minutes of usage in month_8 
- loc_og_t2t_mou_8 : Local call outgoing within same network in month_8 
- std_og_t2t_mou_8 : standard outgoing call within same network in month_8 
- loc_ic_t2f_mou_8 : Local incoming call on operator to fixed lines on month_8 
- loc_ic_mou_8 : Local incoming call on month_8 
- std_ic_t2f_mou_8 : standard incoming call on operator to fixed lines on month-8 
- total_ic_mou_6 : total incoming call on month_6 
- spl_ic_mou_8 : special incoming call on month_8 

## Conclusion 

- Providing discounts or offers to local incoming and outgoing calls will decrease customers from churning. 
- Age on network is also a key indicator for identifying the churn, if aon is less number of days and their usage is reduce then the customer is going to be churned

### Contact
Created by __Durgesh Chaubey__ 


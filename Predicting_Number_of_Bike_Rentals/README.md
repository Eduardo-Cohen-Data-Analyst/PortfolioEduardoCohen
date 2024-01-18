<h1>Determining Which Regression Approach is Best for Predicting The Number of Bike Rentals </h1>

<h3>Chosen Domain: Customer Services</h3>

<br> </br>

By 

Sue Amoreira 

Eduardo Cohen 

Eugen Efros 

Lorna Sinclair 

Marie Garron 

<br> </br>

<h3>Higher Diploma in Science in Data Analytics for Business </h3>

<h3>Machine Learning </h3>

<h3>Dr. Muhammad Iqbal </h3>

<h3>CCT College </h3>

<h3>Dublin, Ireland</h3>

<br> </br>

**Introduction/Abstract 4** 

**Business Understanding 4** 

**Organisation & Business Needs 4** 

**Hypothesis 4**

**General Goal 5** 

**Success Criteria/Indicators 5** 

**Data Understanding 5**

**Technologies Used 5**

**Programming Tools 5**

**Models 6**

**Libraries 6**

**Dataset Description 6** 

**Data Preparation 6**

**Exploratory Data Analysis and Cleaning 6**

**Descriptive Statistics 7**

**Dependant Variable 7**

**Independent Variables 7**

**Categorical Variables 7**

**Numeric Variables 10**

**Feature Reduction 11**

**Principal Component Analysis 11** 

**Modelling 11**

**Evaluation Measures 12**

**Selection of Machine Learning Models 12**

**How The Model Works (Mathematical Theory) 13** 

**Evaluation Phase 14**

**Challenges Encountered 14** 

**Strategies Used to Overcome Challenges Encountered 15** 

**Deployment Phase 15**

**Results and Analysis 15**

**Recommendations 16**

**Reasoning for Selecting Model 19**

# Business Understanding 

**Organisation & Business Needs**

Transport for London (TfL) is a government body responsible for the management of various modes of transportation in the Greater London area. One of the modes of transportation managed by TfL is London’s bike hire scheme, Santander Cycles. Originally introduced in 2010 as a way to alleviate congestion and reduce the levels of pollution in London, this scheme has seen widespread success.(Centre for Public Impact, 2016). 

The cycle hire scheme has seen record use in 2021 with 10.9 million bikes being hired by over 1 million individual customers (Transport for London, 2021). This is an encouraging trend for London’s congestion and for its environmental footprint as transport is a major contributor to CO2 emissions. In the UK, transport accounts for 27% of total CO2 emissions, 91% of this comes from road transport vehicles. (Department for Transport, 2021). 

Further encouraging the use of bikes and reducing the number of car journeys in London is a significant part of the government’s policy on climate change, to reduce CO2 emissions. While the use of cars is discouraged through congestion charges in London, the introduction of segregated cycle lanes aims to further encourage the use of cycles. Furthermore, although the cycle rental scheme has been hugely successful, the continual growth of adoption of this service remains a focus for TfL. (Transport for London, 2022). Thus, TfL can optimise its service by ensuring the adequate supply of rental cycles during peak hours, while also further promoting the use of cycles outside of peak hours. 

# Hypothesis 

With the use of machine learning regression techniques, it is possible to predict future counts of bicycle rentals with an accuracy of 90% by analysing the impact of several independent factors on the number of rentals. 

# General Goal 

By using the count of bicycles rented as a target variable, the aim of this project is to utilise regression machine learning models, to predict future numbers of bicycle rentals with an accuracy exceeding 90%. To achieve the highest accuracy from these models, the data will be cleaned and analysed with the use of EDA (Exploratory Data Analysis) techniques. (if  necessary) while also implementing dimensionality reduction with the use of PCA (Principal  Component Analysis) to reduce training time and improve overall accuracy (Velliangiri, S., et  al., 2019). The modelling stage would involve the use of several machine learning models for  this prediction and the results of this stage will be evaluated and compared to determine  which model yields the highest accuracy score. In the evaluation stage, cross validation  techniques will be used to provide a more certain indication of the predictive capabilities of  the model by

determining how the model performs when it encounters unseen data, rather than existing data used to train the model initially. 

Creating a model to predict future bicycle rentals with a reliable degree of accuracy would allow TfL to provide high quality customer service by ensuring the widespread availability of bicycles even as the number of rentals continues to grow in London. Additionally, it would allow TfL to prudently schedule maintenance for bicycles while causing minimal disruption for customers and bicycles availability. 

# Success Criteria/Indicators 

● Finding the correlations between dependent variables and independent variables using exploratory data analysis (EDA) and statistical analysis of the data. This will determine which variables will be used in the machine learning model for prediction. 

● Creating a machine learning model using regression techniques to accurately predict future numbers of bicycle rentals with an accuracy of at least 90%. 

● Determining which training and testing split of the data will result in the best performance of the machine learning model. 

● Evaluating using cross validation which model is most effective to achieve the goal outlined. 

# Data Understanding 

**Technologies Used**

**Models**

The aim of this project is to predict future numeric values based on historic data and regression models will be used for this prediction. Among the models considered for this Machine Learning project were Random Forest, Linear Regression and K-Nearest Neighbour (KNN). 

# Dataset Description 

The dataset used for analysis and prediction is the “London Bike Sharing Dataset” sourced from Kaggle. It was compiled by merging data from three open data sources, including bike hire data from TfL, weather data from freemeteo.com and bank holiday data from https://www.gov.uk/bank-holidays. (Mavrodiev, 2018). The data set contains a total of 10 features and 17414 observations. 

# Data Preparation 

Exploratory Data Analysis and Cleaning 

Through the use of EDA, the following observations were made regarding the dataset:

● The “Cnt” (count of bike rentals) variable was identified as the target variable for this analysis and machine learning prediction. 

● “timestamp” column had data relating to date and time. This data was split into multiple columns, including “Year”, “Month” and “Period”. The “Year” and “Month” columns would contain data relating to date, while the “Period” columns contained data relating to time, where this data was converted into 6 classes to reflect 6 periods of the day (of 4 hours each). 

● The dataset contained data across three different years, 2015 to 2017, although the year 2017 contained much fewer observations compared to the other two years. 

# Descriptive Statistics 

**Dependant Variable**

● With the use of a boxplot graph, it was clear that outliers were present in the observations of the target variable, “Cnt” 

(Graph 1) 

● The mean and median values of this variable also indicated that the data in “Cnt” was skewed. The skewness score of the data was 1.33 which indicated that the 

distribution of the data was highly skewed. 

● As the range of the data in this variable was very high, a logarithmic scale was used to visualise the data distribution (see Graph 2), rather than a linear scale. 

(Graph 2)

**Independent Variables**

**Categorical Variables**

● The “Year” variable showed no significant change in trends depending on the year so this variable was removed from the data. 


(Graph 3 & Graph 4) 

● The “season” variable showed showed a correlation with “humidity” and “month” and so this feature was removed. was not adding any value to the exiting pattern. The correlation with the others features was low (average below |0.20|), so we dropped that features 

● For “weather\_code, there” was a negative correlation with the target variable - the lower the weather code number, the higher the number of bike rentals. 

(Graph 5) 

● Within the “Windspeed” variable the extreme outliers were assessed and found to account for 1% of the data. It was decided that outliers were to be removed to improve the performance of the machine learning model so the feature followed the distribution of the 99% of the data. Because we have 2 types of features: categorical  like is holidays or weather code and numerical like wind speed. We will harmonized  all the numerical features to match the categorical features range. The new size of  the dataset following removal of outliers is 17155. The “wind\_speed” feature was  numeric, but using the Beaufort Scale this was transformed into categorical data.  Rather than having a range of values from 0 to 56.5 km/hr, the scale would use  binning to group values into 13 classes, ranging from 0 (calm) to 12 (hurricane) as  per the Beaufort Scale, where higher wind speed ranges relate to higher values on to just reslted in a more even distribution of the data (see Graph 7). 6. This the scale. As the data was heavily skewed (see Graph 6) due to outliers, these 13  classes were further reduced  

(Graph 6) 

(Graph 7) 

● Below boxplots summarises the categorical independent variable data. It shows that: ○ Holiday days and weekends saw a reduction in the number of bicycle rentals. ○ Morning and evening periods were the peak periods for rentals (commuting hours)

(Graph 8) 

**Numeric Variables**

● Heatmap was used to visualise the correlation between all numeric variables - this mainly included variables relating to weather . Temperature (“t1”) and temperature feel (“t2”) had the strongest correlation to the target variable. The correlation between “t1) and “t2” was very high, and the fact that temperature has a higher correlation to the target variable, it was decided to remove “t2”, while keeping “t1”. T1 was then assessed for outliers and they were found to account for only 0.37% of the data. The decision was taken to floor the data to the upper bridge as this would not give a major misrepresentation of the data but would create a more normal distribution. 

(Graph 9) 

● For the “humidity” feature, the values range from 1 to 100 and the maximum value is much higher than in the other numeric variables (for example “t1” with a maximum value of 34.0). The data was converted to a ratio, with a range of 0 to 1. As per Graph 10 below, the correlation between the variables was not altered.

(Graph 10) 

● T1 was scaled using min-max scaler. Confirmation that no information was lost via a confusion matrix. 

● Encoding was carried out using the on the data frame whereby additional columns were introduced to replace a feature with a number of categories. Therefore “Month” was converted from 1 feature containing values 1 to 12 into 12 columns labelled “month\_1”,”month\_2”...”month\_12. Within each column, 0 indicates the observation is not in this category and 1 indicates it is in this category. This method prevents the model from interpreting this data as ordinal data. This method was also applied to other columns, including “period”, “holiday”, “week” and “season”. (Bateman et al., ) 

**Feature Reduction**

Principal Component Analysis 

Feature reduction was then carried out using Principal Component Analysis (PCA) which maps the original features to a smaller number whilst retaining the information from the original features. The information is captured by the variance. The optimal number of features as identified in the PCA is 22. The machine learning will be carried out on two datasets: 

● The baseline data prior to the PCA 

● Data with the 22 components reduced using PCA

Graph to change

(Graph 11) 

# Modelling 

As the aim of the project is to predict a continuous number from the target variable, this problem would use supervised learning by applying regression models (Müller and Guido, 2016). For supervised learning problems, data is split between Training and Testing, where the training sample is used to train the model for making predictions, while the testing is a smaller sample which introduces unseen data to the trained model to test its prediction. The optimal split percentage is determined by evaluating the results of the model for various Test/Training splits. (Müller and Guido, 2016). 

**Evaluation Measures**

**Performance Metrics**

● **R2- testing score**

● **Mean Absolute Error**

Mean Absolute error is the absolute difference between the predicted values and the training values of each observation. (Gollapudi and Laxmikanth, 2016) 

● **R Squared**

The Mean squared error is impacted by feature scaling and higher values therefore an alternative performance measure which is often deemed to be a more accurate representation is the r squared measure. This can be considered a scaled version of the mean squared error. This falls between 0 and 1 for the split of the data devoted to training. (Raschka and Mirjalili, 2019) 

● **Mean Squared Error**

Mean Squared Error is the square of the difference between the actual and predicted values of each record. (Gollapudi and Laxmikanth, 2016) 

● **Cross Validation**

As mentioned the Train- test - split function works by splitting the data into a larger training set and a smaller testing split. Different splits can then be used to assess the different performance metrics to identify the best split of the data. This split, for example 20% testing and 80% training, is taken from a specific point in the data controlled by the random state 

variable within the function. Cross Validation can be adopted which takes the 20% split from several different places as determined from the function to confirm the accuracy of the model with different sets of observations included in the training set and the testing set when there is a different 20% selected. 

# Selection of Machine Learning Models 

A data frame was constructed which contained the results of the different performance metrics mentioned above for different regression machine learning models. This provided the train score and test score from 07 different machine learning models as outlined in below figure X. One set of hyperparameters was used within each model for the initial comparison as can be seen in column “Parameters”. Note: "None" in parameters means the model will  use the defaults parametres. 

The accuracy of the training set and the training accuracy of the testing set for each of the machine learning models can be seen in figures X. Random Forest Regressor and KNeighbours Regressor were selected due to having the highest training accuracy scoring for both the baseline data and the PCA reduced data. and the lowest MSE. 

**How The Model Works (Mathematical Theory)**

**Random Forest Model for Regression**

The random forest works by repeatedly splitting the data into two branches based on the features to create trees and repeating this process until we have a “forest”. The test observation is then inputted into all the trees within the forest and the average value is then assigned to the test observation. (Subramanian, 2015) 

**KNeighbours Regression Model**

For a KNeighbours Regression Model the features of the testing data observation determine where it is in the feature space and based on the centre of the K nearest training data points calculated using the euclidean distance the dependent variable is predicted. K is determined by the hyperparameters set within the model. For example in the case of an x value of -0.8 

the K training data points nearest the line are captured and the predicted value of the test data is determined from the centre of the K training data points. In the case illustrated in below figure X the predicted value of the testing data observation using K=3 would be -47.

**Evaluation Phase**

Grid Search was completed to identify the most suitable hyperparameters for the two models. 

**KNN Machine Learning Model**

● R2 

● Train Score 

● Cross Validation & RMSE 

● Hyperparameter Grid Search 

● Training, Validation, Testing- 3 set split- references in whatsapp Random Forest Model for Regression 

● R2 

● Train Score 

● RMSE 

● Cross Validation 

● Hyperparameter Grid Search & Random Search 

# Challenges Encountered 

**Bias in the data**

**Limitations of the Method and Preparation:**

Binning the data can lead to a loss of information as the small differences between data within the same bin is now ignored as they are considered all one value. Despite the assessment of each of the variables prior and post the binning of the features it may be that information has been lost and affect the accuracy of the model.

**Limitations of Dataset:**

The weather data is taken from freemeteo.com. This website sources weather reports from “thousands of certified online stations around the world”. However it may be prudent to analyse alongside weather data from an alternative source such as the met office weather data which is a government website. The credibility of the weather website may be questioned. 

# Strategies Used to Overcome Challenges Encountered 

● **Overcoming Bias**

● **Using additional resources**

# Deployment Phase 

**Results and Analysis**

From the two models assessed, XX is better equipped to predict the number of bike rentals in London based on Weather forecasts. This is based on a higher training accuracy. With an accuracy of X the target accuracy of 90% as outlined within the goal of this project was not met. 

The Training and Testing score for the two models as shown in figures X and X differ with a higher value of training score. As such it can be assumed that the models are overfitted and therefore may not be capable of accurately predicting future bike rental numbers based on the weather data. 

**High Variance**

**Overfitting**

If a model is too complex for a given training dataset—there are too many degrees of freedom or parameters in this model—the model tends to overfit the training data and does not generalise well to unseen data. Often, it can help to collect more training examples to reduce the degree of overfitting. Estimating generalisation performance Please note that a detailed discussion of how the variance of the generalisation performance is estimated in cross- validation is beyond the scope of this book, but you can refer to a comprehensive article about model evaluation and cross- validation However, in practice, it can often be very expensive or simply not feasible to collect more data. By plotting the model training and validation accuracies as functions of the training dataset size, we can easily detect whether the model suffers from high variance or high bias, and whether the collection of more data could help to address this problem. But before we discuss how to plot learning curves in scikit-learn, let's discuss those two common model issues by walking through the following

illustration: The graph in the upper-left shows a model with high bias. This model has both low training and cross-validation accuracy, which indicates that it underfits the training data. Common ways to address this issue are to increase the number of parameters of the model, for example, by collecting or constructing additional features, or by decreasing the degree of regularisation, for example, in support vector machine (SVM) or logistic regression classifiers. The graph in the upper-right shows a model that suffers from high variance, which is indicated by the large gap between the training and cross-validation accuracy. To address this problem of overfitting, we can collect more training data, reduce 

# Recommendations 

How will this model be applied to solve the customer service problem identified in Business Understanding by TfL? 

# Individual Contributions

**Eduardo**

Following Marie’s review of the different machine learning models, I then implemented the RandomForest Regressor on the data. My initial results for the machine learning model were a relatively low training accuracy and a high error. As there was a large difference between training and testing accuracy it was evident from the initial analysis that there was variance within the model. Therefore I had to carry out a number of iterations of the model. These iterations included altering the feature selection process, and adjusting the hyperparameters within the model. I did significant research into the effects of altering the different hyperparameters to better understand the outcome of each iteration with different sets of hyperparameters. Implementing grid search helped me to identify the best set of hyperparameters. I reviewed the feature selection and identified a number of features that if adjusted might improve the outcome and worked with Marie and Lorna to update the data preparation and rerun the model. After achieving an initial accuracy of X I performed cross validation to ensure that across a number of different splits of the training and testing data  an acceptable level of accuracy could be achieved. I reached a level of accuracy of XX for  the final version of the RandomForest Regressor model.

<br> </br>

**Eugen**

My contribution to this project included researching to find data for the chosen category for this project. I researched the adoption of the TfL cycle rental scheme by consumers and the

possible effects this could have on the future, and what the future objectives of the organisations would be, to help determine the goals and objectives for this project. I was responsible for conducting the EDA, where I aimed to characterise the data and assess the quality of the data. Using statistical analysis, I searched for patterns and trends within the data to find if there were meaningful relationships and correlation between the various features of the data set. I assessed the distribution of the data to find the impact of outliers. I created visualisations through the use of charts and graphs and presented these findings to the team and linked with Lorna, who was handling the data cleaning aspect of the project to communicate my findings which allowed her to address these findings in the data preparation and cleaning phase. As part of the Deployment phase, I assisted in generating the report for this project, detailing my findings from my research in the Business Understanding phase and my contribution to EDA in the Data Preparation phase. 

<br> </br>
 
**Lorna**

I was tasked with conducting data cleaning and addressing the issues identified by Eugen in the EDA phase. The data cleaning involved splitting columns into multiple features and implementing feature reduction by removing certain features from the dataset. A major issue found in EDA was the skewed distribution of the data and the presence of outliers in the data. After the initial testing of the model, I suggested removing certain outliers and testing the model to determine if the accuracy improved. I had to determine the best course for dealing with outliers in order to improve the performance of the models. I used various techniques to tackle outliers in the data, by binning and grouping values together, capping outliers or removing them from the dataset where this would result in minimal loss of observations. I also worked closely with Marie and Eduardo to test the performances of the models after removing certain outliers, and finding ways to improve the performance of the model through additional data cleaning, feature reduction or removing other outliers. As I was working predominantly on data cleaning, I contributed to the Data Preparation section of the report, while also assisting with researching the organisation for the Business Understanding phase. 

<br> </br>

**Sue** 

In this project I assisted Lorna with the data cleaning and I was tasked with implementing PCA on the data before the modelling stage. I suggested that we should implement normalisation by rescaling the numeric features of the dataset in order to improve the performance of the machine learning model. I suggested converting the data in the humidity feature to a ratio where the minimum value would be 0.0 and the maximum would be 1.0. The other numeric features like temperature, wind speed and weather code were also rescaled, where the values would be rescaled according to their position between the minimum and maximum values, 0.0 and 1.0. I then used a correlation matrix to ensure that the correlation values and patterns were not affected during the normalisation. Regarding PCA, it was decided to retain at least 95% of the variance in the data. After plotting the data, I determined the number of features required to retain this variance. I implemented PCA and created a new dataset, however I suggested using the pre-PCA data and PCA data for modelling and comparing the results. In the report, I contributed to the Data Preparation phase and explained my reasoning for data cleaning and PCA.

<br> </br>

**Marie**

My individual contribution was developing the selection criteria of the machine learning models and the implementation of the KNeighbours Regression model for prediction. I was able to create a dataframe which captured 7 different machine learning models for both a PCA reduced dataset and a baseline dataset and showed the evaluation metrics for each. This allowed the graphing and analysis of the different models against one another and drove the decision to select KNeighbours Regressor and RandomForest Regressor for implementation and further development. The selection criteria I included in the dataframe were training accuracy, R squared, root mean square error and mean squared error. From  my research these were the best metrics to evaluate a regression problem. When trying to implement the KNeighbours Regressor initially, the accuracy and metrics I was able to achieve were not meeting the goal and therefore I worked with Lorna and Eduardo to identify the how the feature selection could be altered and would subsequently improve the outcome of the KNeighbours Regressor. I was able to tune the hyperparameters and also perform cross validation on the model to achieve a final accuracy of 65% which was not a significant improvement from the initial running of the model. 

My approach was to use a validation test for all parameters tuning. This method will prevent  any informations leakage from the training to the testing.  

From the learning curve we can see that the model is highly biased. and the sensitivity  analysis confirm that the model is over-fitting. Despite the back and forth with the EDA team,  we did not manage to improve the model.  


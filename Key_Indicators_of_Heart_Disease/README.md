<h1>﻿**Predicting Whether Heart Disease is Present Based on Lifestyle, Pre-existing Health Factors and Demographic Factors Using Machine Learning**</h1>



By

Eduardo Cohen

Eugen Efros

Lorna Sinclair

Marie Garron







﻿
<h3> Higher Diploma in Science in Data Analytics for Business﻿</h3>


<h3>Strategic Thinking﻿</h3>

<h3>James Garza﻿</h3>

<h3>CCT College</h3>

<h3>Dublin, Ireland</h3>


[**Introduction/Abstract](#_heading=h.b0dp68q5j7se)	**4**

[**Business Understanding](#_heading=h.46ng2xj0yo75)	**4**

[Organisation & Business Needs](#_heading=h.t4959c2ljlg)	4

[Hypothesis](#_heading=h.9zmnmxjzv5z7)	4

[Success Criteria/Indicators](#_heading=h.yyahyqskbqbx)	5

[**Data Understanding](#_heading=h.39jxsnx9vk9o)	**5****

[Technologies Used](#_heading=h.yumuamttf7jk)	5

[Dataset Description](#_heading=h.t6a25f6y0xnd)	5

[**Data Preparation](#_heading=h.8vilr2utj412)	**6****

[Exploratory Data Analysis (EDA)](#_heading=h.nk61raupdit3)	6

[Demographic Variables](#_heading=h.leya252zzmmg)	6

[Gender](#_heading=h.deskdddn3y4x)	6

[Generation/Age](#_heading=h.82r1w7pckm4q)	7

[Lifestyle Variables]( h)	8

[History of Smoking/Alcohol Drinking](#_heading=h.u0q1u9gmx9fg)	8

[Health Variables](#_heading=h.jsn0v1cvmizm)	8

[History of Stroke/Difficulty Walking/Kidney Disease](#_heading=h.f0fvfj8d3nhc)	8

[Changing Continuous Numeric Variables](#_heading=h.4jd4e58oqniu)	8

[Changing Boolean/Categorical Data](#_heading=h.j5ndsop3dfn)	9

[Dealing With Outliers - Sleeptime](#_heading=h.lc96gdeydsen)	9

[Correlation Between Dependant and Independent Variables](#_heading=h.6huu4kattff6)	10

[**Modeling](#_heading=h.duaa3tksq9ss)	**10****

[**Evaluation Phase](#_heading=h.1cza2r9ibebe)	**11****

[Evaluating Model](#_heading=h.8ltyfn8a0qcp)	11

[Challenges Encountered](#_heading=h.ouz80uwkye2h)	12

[**Deployment Phase](#_heading=h.nmvnnz1kmo3u)	**13****

[Results and Analysis](#_heading=h.qplf303qrso)	13

[Recommendations](#_heading=h.1njtj12ixr3n)	14

[**References](#_heading=h.n77a1ojui0n)	**15****

[**Individual Contributions]( h)	**16****
#



# Introduction/Abstract
With 20% of deaths being directly attributed to heart disease, it is the main cause of death in the United States. Advancements in medicine and research of the underlying causes of heart disease has resulted in a declining rate of heart disease among older adults, however new studies now show that heart disease is becoming more common among younger people (Centers for Disease Control and Prevention, 2021). Using data from the Centres for Disease Control and Prevention (CDC), it is possible to analyse the relationship between heart disease and various factors relating to general health, lifestyle and demographics and make predictions based on these relationships and patterns to determine the likelihood of developing heart disease. Using the Cross-Industry Standard Process for Data Mining (CRISP-DM) methodology, this report aims to predict whether the likelihood of having coronary heart disease or myocardial infarction can be determined based on a person’s lifestyle, health and demographic factors. 
# Business Understanding
## Organisation & Business Needs 
The Centers for Disease Control and Prevention (CDC) is a US government agency whose purpose is to conduct research on matters concerning public health in the United States, and inform the Department of Health and Human Services of its findings, while also educating the public on health related matters.  (Centers for Disease Control and Prevention, 2019). Data collection and analysis is a key component of CDC’s research, which is performed through it’s Behavioral Risk Factor Surveillance System (BRFSS), where telephone based surveys are conducted annually, consisting of 400,000 adults in all 50 US states. (Centers for Disease Control and Prevention, 2019). 

Within the telephone survey the respondent is asked whether they have ever reported having coronary heart disease (CHD) or myocardial infarction (MI). In the United states, 20% of all deaths can be directly attributed to heart disease and is the main cause of deaths in the US. Existing health factors such as high blood pressure and high blood cholesterol are strongly linked to the development of heart disease, although other medical conditions, such as obesity, and lifestyle habits of alcohol drinking and smoking also increase the risk. (Centres for Disease Control and Prevention, 2021).
## Hypothesis
With the use of machine learning algorithms and survey data collected during the BRFSS, it is possible to determine the likelihood of heart disease based on Lifestyle, Pre-existing Health Factors and Demographic Factors. In particular, pre-existing health factors have a significant impact on the likelihood of heart disease. Those with past habits such as smoking, drinking, low levels of physical activity and lower sleep time would see a greater likelihood of heart disease. Additionally Pre-existing health factors such as diabetes would lead to a higher likelihood of heart disease in individuals. 

General Goal

The aim of this project is to investigate the hypothesis above with the use of data analysis and machine learning techniques. By analysing the correlation between Lifestyle, Pre-existing Health Factors and Demographic Factors (dependant variables) and the Respondents that have ever had coronary heart disease or myocardial infarction (independent variable), the aim is to predict future trends in the data through the use of classification techniques, to provide an accurate prediction of heart disease based on lifestyle, health and demographic factors.
## Success Criteria/Indicators
With the project goal defined, the success of this project will be assessed on the below criteria:

- Finding the correlations between dependent variables and independent variables using exploratory data analysis (EDA).
- Creating a machine learning model using classification which will accurately predict likelihood of heart disease at an accuracy of at least 85% and a recall of at least 95%. 

# Data Understanding
#
## Technologies Used
**Models**

As the objective of the project is to predict whether or not a respondent has heart disease, a classification machine learning approach was used. 
## Dataset Description 
The “Personal Key Indicators of Heart Disease” dataset is an open source dataset available on Kaggle which contains data from the The Behavioral Risk Factor Surveillance System (BRFSS) survey of 2020. The Behavioral Risk Factor Surveillance System (BRFSS) dataset contains data collated from the results of the annual CDC survey and is publically available on the CDC website. The original dataset contains all the responses of the 207 questions posed in the 2020 annual survey, and contains 401,958 records of responses. Thus, the original dataset contained 279 features and 401,958 observations. 

The survey assesses the impact of multiple diseases, illnesses and health conditions, therefore not all of these features can be linked to heart disease. Additionally, extensive demographics and lifestyle related data was collected from the respondents which was not directly relevant to the development of heart disease.

The modified “Personal Key Indicators of Heart Disease” dataset uses the data from the 2020 BRFSS survey while only retaining features which were deemed most pertinent to the development of heart disease, and thus from 279 features, just 18 were retained in the modified dataset. Additionally, further data cleaning reduced the number of observations from 401,958 in the original dataset, to 319,795. 

**Features**

From the 18 features contained in the “Personal Key Indicators of Heart Disease” dataset:

- 4 features contained numeric data
- 10 features contained boolean data
- 4 features contained categorical data


# Data Preparation
## Exploratory Data Analysis (EDA)
#

**Duplicates**

It was observed from the data that 18,078 rows were duplicated (5.65% of the data). It was decided to remove the duplicates from the dataset. 

**Imbalance Data**

It was found that the dataset was imbalanced as there was a substantial disparity in the ratio of “No” to “Yes” responses, with a ratio of 10:1. As such, the algorithm will likely be biased towards predicting an outcome of “No” heart disease.  

(Figure 1.1 - “Ratio of No/Yes Responses in the Data”

### **Demographic Variables**
#### **Gender**
It was observed that the Gender data was imbalanced, with a Female:Male ratio of 53:47. This may indicate the presence of bias in the data. Male’s are significantly more likely to develop heart disease (58.9% of respondents with heart disease were male). 

(Figure 1.2 “Gender Distribution of Survey)  & (Figure 1.3 “Gender vs Heart Disease Comparison”)
#### **Generation/Age**
The “Age” variable was also categorical, as respondents were given several age ranges to choose from. To limit the number of categories, the ages were binned into 5 categories based on the definitions defined by the Pew research centre. (Dimock, 2019): 

- Boomer: Born between 1946 and 1964
- Generation X:Born between 1965 and 1980
- Millennial Generation: Born between 1981 and 1996
- Generation Z: Born between 1997 and 2012 
- All those born before 1945 were grouped into a single “Elderly” group. 


(Figure 1.4 “Age/Generation vs Heart Disease”)



(Figure 1.5 “Ratio of Persons with Heart Disease per Age Category”)

When comparing these age categories with the prevalence of heart disease, a pattern emerged with a positive correlation between heart disease and age. The clear pattern from this observation shows that as a respondent gets older, he/she is more likely to develop heart disease. 


### **Lifestyle Variables**
#### **History of Smoking/Alcohol Drinking**
Smoking was shown to have a notable correlation with heart disease - 58.6% of people with heart disease had a history of smoking. Of people without a history of heart disease, 59.4% had no history of smoking, compared to 40.6% who did.



(Figure 1.6 “Heart Disease vs History of Smoking”)
### **Health Variables**
#### **History of Stroke/Difficulty Walking/Kidney Disease**

(Figure 1.7 “History of Stroke/Difficulty Walking/Kidney Disease vs Heart Disease”)

- History of Stroke and heart disease are heavily linked - 16.1% of respondents who had heart disease also had a stroke, while just 2.8% of respondents with no history of heart disease had a stroke. A respondent who had a stroke is much more likely to also have heart disease. 
- A very similar relationship was seen with two other health variables: “Difficulty Walking” and “Kidney Disease” suggesting that these variables are strongly linked with heart disease. 

### **Changing Continuous Numeric Variables**
Continuous numeric variables, such as BMI were categorised and binned into groups which would improve the performance of the model by limiting the impact of outliers. “BMI” was binned into four groups: underweight, healthy weight, overweight and obese (Centres for Disease Control and Prevention, 2022).

(Figure 1.8 “Percentage of Heart Disease Compared to BMI”)
### **Changing Boolean/Categorical Data**
To improve the performance of the machine learning model, the features with boolean observations were replaced with numeric data. These observations contained either “Yes” or “No” data, which was changed to 1 and 0 respectively. Other variables such as: “Race”, “Diabetic” and “General Health” contained categorical data, but this data was also changed to numeric categories. 
### **Dealing With Outliers - Sleeptime** 
It was observed that the “Sleeptime'' variable contained outliers, where in responses the average sleep time was up to 24 hours a day. See the below box plot indicating these outliers.

(Figure 1.9 “Boxplot of “Sleeptime” Before Flooring”)

(Figure 1.10 “Boxplot of “Sleeptime” After Flooring”)

It was determined that these were not reliable responses and therefore would impact the accuracy and effectiveness of the machine learning model. The percentage of outliers within “Sleeptime” above the upper bridge was 1.06% and the percentage of outliers below the lower bridge was 3.78%. Pathological lack of sleep is under 3 hours on average while pathological oversleep is above 12 hours on average (Healthline, 2016). Therefore, taking these as an upper and lower value to floor and ceiling the sleep feature values, 0.33% of the data is above this upper ceiling value and 0.44% is below the flooring value. 
### **Correlation Between Dependant and Independent Variables**

(Figure 1.11 “Heatmap of Correlation Between Variables”)

The above heatmap shows which variables have the strongest correlation to one another and specifically to the target variable, heart disease. “Age”, “History of Strokes” and “Difficulty Walking” are most closely correlated with heart disease. 
# Modeling
As this is a classification problem the K Nearest Neighbours (KNN) Algorithm was selected. KNN classification computes the class of the testing data based on the class of a number of the nearest neighbours. The number of nearest neighbours used to determine the class is set by the parameter K within the model. The value of K can strongly influence the accuracy and effectiveness of the model however in general when a higher number of neighbours is selected the effects of noise can be reduced. (scikit-learn.org, n.d.)

To assess the effectiveness of the EDA the machine learning was carried out with both the raw baseline data and the scaled dataframe. 
# Evaluation Phase
## Evaluating Model
The accuracy achieved with both the baseline data and the scaled data when utilising the KNN algorithm was high with a value of 96.5% for the baseline and 97.4% for the scaled and processed data for prediction of heart disease. However, with 91% for the data in the dataset representing a “No” response for a history of heart disease this is to be expected. This is because the model functions on the assumption that the data is balanced and has learnt based on a much larger number of respondents without heart disease. The model will default to predictions of no heart disease and with 91% of the data being for respondents with no heart disease the model will always be at least 91% accurate.

Therefore a better measure is recall. Recall is the measure of positive predictions that were correct i.e. how many predictions of those with heart disease from the ML model did have a history of heart disease. In the case of medical data this is also more essential as the consequence of not diagnosing heart disease can be fatal. The recall of the KNN model on the baseline data was 62% versus a recall of 74% for the scaled dataframe. This is an improvement however would require further work as there are still 1431 instances where the respondent had a history of heart disease and the model predicted they did not. In these cases, if the model was being used to predict someone has heart disease, they would go undiagnosed. 

(Figure 1.12 “Confusion Matrix of Original and Scaled Data Respectively”)


##

## Challenges Encountered
- Race Representation
  - The data showed a significant disparity in the responses of certain age categories, with an overwhelming majority of respondents identifying as “White” (75%). This raised serious questions of whether the data was biased by over representing this race demographic compared to the others. To evaluate if this was the case, the data was compared to the US Census data.
  - In the Census data, it was found that:
    - 75.8% of respondents identified themselves as “White”. 
    - 13.6% of Census respondents identified as Black or African American.
    - 6.1% identified as Asian.
    - 1.3% identified as American Indian and Alaska Native.
    - 0.3% identified as Native Hawaiian and Other Pacific Islander.
    - In Summary, it appears that the White and Black demographics are under-represented in the data when compared to the ratio of US population, while the Asian and Native American demographics are over-represented. 

(Figure 1.13 “Racial Distribution in the BRFSS Survey) 


(Figure 1.14 “Racial Distribution in the US Census”)

- Impact of Covid-19 on the Survey Data
  - Another source of bias is the impact of Covid-19. The first reported cases of Covid-19 in the US were at the start of March 2020, while a significant increase in case numbers was noted from October 2020 (Statista, 2022). 
  - The survey took place throughout the year of 2020, across the 12 months of the year. Thus, it can be concluded that some respondents may have had contracted Covid-19, especially by the later months of 2020 which saw a sharp rise in the number of cases. Thus, the responses relating to health factors may have been affected by Covid-19. 
- Gender Representation
  - The dataset also contains a disparity for the Gender category, with a Female to Male ratio of 53:47 (U.S. Census Bureau, 2020).
  - According to the 2020 US Census, 50.5% of respondents identified as Female, and the remaining 49.5% as Male. This means when compared to the US Census of 2020, men were under-represented in the BRFSS survey. 

(Figure 1.15 “Gender Representation in the BRFSS survey”)
# Deployment Phase 
## Results and Analysis
As detailed above, the success of this project was to be assessed on the below criteria:

- Finding the correlations between dependent variables and independent variables using exploratory data analysis (EDA).
- Creating a machine learning model using classification which will accurately predict likelihood of heart disease at an accuracy of at least 85% and a recall of at least 95%.

The strongest correlations within the features in the dataset were with history of Stroke, Difficulty Walking and history of Kidney Disease.The aim of identifying the likelihood of heart disease based on Lifestyle, Pre-existing Health Factors and Demographic Factors therefore suggests the strongest factors are those concerned with pre existing health factors. These features were more correlated with the dependent variable of heart disease than the lifestyle factors such as smoking and the demographic factors such as gender and race. 

A machine learning model was developed using the KNN classification algorithm and an accuracy of 97.4% was achieved therefore satisfying the success criteria set for accuracy. However upon review of the dataset and the identification of how imbalanced the dataset was with the number of those responding “No” accounting for 91% of the dataset an accuracy of 91% minimum was expected.

The key evaluation metric was the recall. In the case of prediction of heart disease a correct prediction of those with heart disease is essential as the alternative could be fatal. The recall achieved with the scaled data was 74% and was a significant improvement on the baseline data which was 62%. However this does not meet the success criteria set and therefore further work must be done to improve the model. 
## Recommendations
A recall of 74% was achieved with the scaled data. As mentioned this did not meet the goal set for the success criteria and therefore further feature engineering or additional data may be needed. 

As discussed above the dataset was imbalanced and therefore addressing this to reduce the bias within the model would be recommended. 

Other examples of bias were disparity in the gender and race features against census data for the United States. To gather more data and survey a diverse range of respondents that are representative of the US general public may improve the outcome and therefore improve the prediction. 
#
#
#
#
#
#
#
#


# References
CDC. “CDC Organization.” Centers for Disease Control and Prevention, 2019, www.cdc.gov/about/organization/cio.htm?CDC\_AA\_refVal=https%3A%2F%2Fwww.cdc.gov%2Fabout%2Forganization%2Findex.html.

Centers for Disease Control and Prevention. “CDC - Behavioral Risk Factor Surveillance System Behavioral Risk Factor Surveillance System.” CDC, 2019, www.cdc.gov/brfss/index.html.

` `“Heart Disease: It Can Happen at Any Age | Cdc.gov.” Centers for Disease Control and Prevention, 26 Jan. 2021, www.cdc.gov/heartdisease/any\_age.htm#:~:text=Heart%20disease%20doesn%27t%20happen. Accessed 6 Dec. 2022.

Centres for Disease Control and Prevention. “Defining Adult Overweight and Obesity.” Centers for Disease Control and Prevention, 3 May 2022, www.cdc.gov/obesity/basics/adult-defining.html#:~:text=If%20your%20BMI%20is%20less.

“Heart Health Information: About Heart Disease.” Centers for Disease Control and Prevention, 14 May 2019, www.cdc.gov/heartdisease/about.htm.

Healthline. “Oversleeping: Causes, Health Risks, and More.” Healthline, 9 Dec. 2016, www.healthline.com/health/oversleeping#oversleeping-causes.

Statista. “U.S. COVID-19 New Cases by Day.” Statista, 1 Nov. 2022, www.statista.com/statistics/1102816/coronavirus-covid19-cases-number-us-americans-by-day/.

U.S. Census Bureau. “U.S. Census Bureau QuickFacts: United States.” Www.census.gov, 2020, www.census.gov/quickfacts/fact/table/US/LFE046221.

Centers for Disease Control and Prevention (2019). Our History - Our Story. [online] Center for Disease Control and Prevention. Available at: https://www.cdc.gov/about/history/index.html.

Dimock, M. (2019). Defining generations: Where Millennials End and Generation Z Begins. [online] Pew Research Center. Available at: https://www.pewresearch.org/fact-tank/2019/01/17/where-millennials-end-and-generation-z-begins/.

National Institute Of Diabetes And Digestive And Kidney Diseases (U.S (2018). Diabetes in America. Bethesda, Md.: National Institutes Of Health, National Institute Of Diabetes And Digestive And Kidney Diseases.

scikit-learn.org. (n.d.). 1.6. Nearest Neighbors — scikit-learn 0.23.1 documentation. [online] Available at: https://scikit-learn.org/stable/modules/neighbors.html#classification.

Tube and train strikes: Commuters face travel disruption. (2015). BBC News. [online] 9 Jul. Available at: https://www.bbc.com/news/uk-england-london-33456830 [Accessed 20 Nov. 2022].

World Health Organization (2021). Cardiovascular Diseases (CVDs). [online] who.int. Available at: https://www.who.int/news-room/fact-sheets/detail/cardiovascular-diseases-(cvds).

Zhang, Q., Zhou, H., Jiang, Y., Cao, B., Li, Y., Song, Y., Chen, J., Zhang, J. and Wang, M. (2019). A Simple Joint Modulation Format Identification and OSNR Monitoring Scheme for IMDD OOFDM Transceivers Using K-Nearest Neighbor Algorithm. Applied Sciences, 9(18), p.3892. doi:10.3390/app9183892.


# Individual Contributions
Marie Garron

As an apprentice data scientist, I learnt about managing unbalanced data sets throughout this project. Unfortunately, this can lead to several problems, including poor model performance, biased results, and difficulty evaluating the model.

There are many approaches in the literature. The most common method is to collect more data for the underrepresented class. However, this can be time-consuming and is not always possible. This is not an option for this project.

Another option is to use oversampling, undersampling or a hybrid method (oversampling and undersampling) to adjust the class balance. These techniques can be effective but can also introduce biases and distort relationships between characteristics and the target variable. For this project, we opted for undersampling using the Near miss estimator.

In addition to these techniques, I learned the importance of evaluating model performance in the medical context. The goal is to deploy a machine learning model to predict whether a person will develop heart disease. Traditional assessment measures, such as accuracy, can be misleading, especially when classes are unbalanced. It is, therefore, essential to use other metrics, such as precision, recall and F1 score. For this project, we focused on a recall of 1, because the consequences of misdiagnosis are too high.   

For a medical dataset, using a recall value of 1 prioritises the model's ability to find all occurrences of a particular class (in this case, a medical condition). This can be crucial when diagnosing life-threatening disorders, for example, where the effects of false negatives (missed detections) are extremely severe. However, it is crucial to take the trade-off of selecting a high recall value into account. For instance, a recall of 1 will probably lead to a greater number of false positives, meaning the model will have a higher rate of incorrect identification of the target class. As a result, patients may experience unneeded stress and may need extra testing or therapy.

As a result, it's crucial to carefully weigh the trade-offs between the various recall values and the F1 score as well as the context and unique model objectives. Although our findings were not meeting our expectations at this point in the machine learning model's development.

The second phase will require us to concentrate on selecting a model that satisfies these two criteria and perhaps study additional research articles on an imbalanced dataset, like employing weighted loss functions to analyse unbalanced datasets.

Overall, dealing with unbalanced datasets requires careful consideration of the various options and techniques available. However, by understanding the pros and cons of each approach and using appropriate evaluation measures, we will see if I could effectively correct the class imbalance and improve the performance of ML model. This is a crucial skill for any data scientist, as unbalanced data sets are standard in many real-world applications.

Finally, on a more personal level and as a project manager, I have long understood the importance of effective teamwork and the challenges that can arise when one of the team members does not function to their full potential. When one team member is not doing their job, it can have a negative impact on the entire team and the project.

The most effective approach is proactive and collaborative. First, it is essential to try to understand the underlying cause. Then, It is is often possible to identify a solution or develop a plan to solve the problem. Another critical step is communicating with the team member about their performance and any identified concerns.   However, when the problem persists despite these efforts, it may be necessary to adjust the team member's responsibilities to match his skills and abilities better and allow the project to be completed in the allotted time.

Ultimately, the goal is to find a solution that allows team members to take responsibility and contribute to the project's success while using a proactive and collaborative approach. It might not always worked but at least we tried.**                       

Lorna Sinclair

Embarking on the higher diploma in data analytics was the first experience I had of using python. It was also the first experience of processing large unclean datasets through machine learning models to predict outcomes. This project allowed me to take the technical skills learnt within the data preparation, machine learning and statistical techniques modules and explain the findings. By doing this it changed from a “going through the motions” activity of copying the python script to a level of understanding.

The team was split into the python team and the report team. Those who were more experienced in python were in the python team and I was part of the report team. This meant each team member was in the best position to contribute. As part of the report team communication with the python team was key. The python team were required to explain and outline their methodology so it could be captured within the report. With this collaborative approach, new and different techniques were shared and utilised. This sharing of the methodology was a key part of each of the project meetings which took place once or twice a week. Ensuring each team member understood and could each explain the approach taken was key. 

The first challenge as a team was to decide on a dataset to analyse. As a team with different backgrounds, levels of python ability and sectors to work in, this was a crucial stage of the project. Identifying an area that the whole team had an interest in and could provide interesting outcomes was essential. The approach taken was to each select several datasets and outline the reasons for choosing them. This allowed us to understand what area of analysis the other team members were interested in. It also highlighted the key strengths of each team member when outlining why this was a good dataset to analyse. The decision was taken to analyse the heart disease dataset. With a background in the medical sector this was of interest. 

It was a requirement of the report to give the reader an understanding of where the dataset came from and how it was produced. As such, the research into the CDC and the BRFSS was necessary and this then needed to be clearly communicated to the reader. With such a large initial dataset with an enormous number of features and an extensive data dictionary, significant research was also needed into the initial unclean dataset. Reviewing the documentation and understanding of which features were selected for review and why was carried out and outlined within the report. These findings also made up a significant portion of the team meetings as the research fed into the python methodology. 

The hypothesis and goal were set prior to the machine learning being completed and therefore this meant that a realistic review of the team’s work could be done. Different techniques were discussed at the team meetings to improve the accuracy and recall. Despite the inability to reach the required recall the improvement in the recall is a testament to the teamwork and collaborative approach. Further work to improve the outcome has been discussed and with more knowledge of machine learning and data preparation in semester 2 a better result is expected. 


Eugen Efros

As one of my first projects in Data Science and Python, this project, while posing several challenges, was ultimately a great opportunity to apply my learning from all the classes taken this semester. As a Python novice, the machine learning aspect was the most challenging for me, but the strength of the group proved to be our collaborative attitude and extraordinary teamwork, which allowed all of us to work to our strengths and help one another in areas one struggled with. 

The first stage of the project (after choosing a topic and finding the data) was the research and Business understanding phase. This was a crucial phase which helped us understand the company/organisation and it’s needs, find uses for the data collected which will benefit the company, and ultimately take into consideration the fact that this was sensitive medical data which would require a high degree of accuracy in the model prediction.

The next stage was the Data Understanding phase, which was challenging in many ways. Here we researched the validity and quality of the data source, and the data itself. We noticed that while the dataset used was a modified dataset from the CDC, and thus we checked to ensure that no features were left out which would be critical to our project. We thoroughly researched the original data and the questionnaire which it was based on and found that while almost all features in the modified dataset were relevant to heart disease, other features would have been useful but were removed. 

The Data Preparation phase involved EDA and data cleaning, and the biggest challenge encountered was an imbalance in data and bias. As we were working with several demographic data features, it was our responsibility to ensure that the data was not biased against any group. We decided to compare the data with Census data to ensure the data was representative of all these groups. Unfortunately, we found several instances of bias in the data where we could not find a way to resolve due to time constraints. 

The Modelling and Evaluation stage requires us to select a Classification machine learning model and apply this to the data. Unfortunately in this stage, we did not achieve the performance and results we were expecting as the prediction returned a high number of false negatives. Considering that the application of the prediction may include medical treatment for heart disease, this number had to be minimal, and we determined that the model needs to be improved (through further data cleaning or by collecting additional data). 

Relating to individual contributions, Eduardo, Marie and Lorna showed an extraordinary work ethic and collaborative attitude, which made this project a tremendous learning experience. Each of them contributed according to their strengths but always showed a willingness to contribute in every aspect of the project. It was clear that each of them showed the commitment, responsibility and empathy required to successfully complete a group project. The remaining member in the group failed to show the same attitude and willingness to contribute, and as a team we had to adapt to this and collectively pick up the slack. 







Eduardo Cohen

In my experience during this project, I have learned several things that will contribute to my future professional development as a data analyst.

Among the different relevant points regarding this topic, I can highlight the importance of understanding the selection of a dataset.

Performing a preliminary data analysis and data correlation on the features that could give us a hint of the issues that may appear later as unbalanced data, the implications of how this would affect later more work involved in data cleaning, EDA, data engineering and data normalisation to fix these issues and adapt the data to be more adjusted for a better machine learning performance.

We also found features with biased information (data more inclined to one result than another) that can possibly lead to a major impact on the prediction and accuracy of the machine learning model.

Considering these difficulties presented and learning how to overcome them after the project finalisation I believe help us to become better data analyst professionals, the ones that can be one step ahead to find or build the solution to at least reduce the possible issues that may appear on a data analyst project journey and reach to improved machine learning models.

The other point for me that was really relevant was the workgroup. I can honestly say being in this team of colleagues with Marie, Eugen and Lorna was an amazing experience. I have learned a lot from them, and seeing the commitment, effort, empathy, fellowship, and symbiosis among us make me realise how important it is for our personal and group to grow to have these people around me.

Unfortunately, there were other people I have not mentioned their name in this report that have not contributed or helped very little in the whole project. They did not show any effort to be involved in the meetings, sprints, and presentations despite we give them a lot of opportunities. Sadly, this only shows us, in the end, the lack of commitment or care about the project and they were not following the good values of the group we set almost from the beginning.



# Home_Insurance

![Home Insurance](https://user-images.githubusercontent.com/63940535/132376911-b5ae39cf-8f61-48e4-86da-00fc94742e63.gif)


[![kaggle logo](https://svgshare.com/i/_xT.svg)](https://www.kaggle.com/frukkurt/home-insurance)
[![python_kaggle](https://svgshare.com/i/_x5.svg)](https://www.kaggle.com/frukkurt/home-insurance-demonstration-with-python)
[![R_kaggle](https://svgshare.com/i/_wb.svg)](https://www.kaggle.com/frukkurt/home-insurance-demonstration-with-r)

This project was to predict whether customers made a decision to cancel their policy or renew their home insurance policy. This is because home insurance changes when it expires, for example, the lack of premium payments. Renewal within the period specified in the policy contract Policy waiver at the end of the contract That is, the insurance will no longer pay any benefits or provide any insurance coverage after the expiration of the term. Using the Home Insurance dataset from the Université de Technologie de Troyes (UTT), France.


## I.Introduction
From the collection of information from the insurance industry, it is regarded as the heart of the management and issuance of policies in insurance companies all along. As data changes and is constantly being created, new ones are created. The type of insurance that most people overlook is important. Insurance for houses, residential buildings It is an insurance that covers residential buildings. When an incident damages the house or property within the house, The insurance company assesses the damage and compensates for the loss according to the specified policy, which looks no different from the popular life insurance. Usually, home insurance is a necessity. Most people should pay attention to this because the benefit of insurance is to compensate for the damage to the house. High value assets If an unexpected accident occurs due to negligence such as fire, flood, gas explosion, etc., there will be compensation to deal with the incident. Especially in the case that the house has not exhausted the debt burden. If you have to lose the house, You can still get money from insurance to pay off the bank's loan balance.

When a dataset called Home Insurance collects 66 variables for residential insurance sales, the data is manipulated to create new policies that are more tailored to the customer's needs. by using the information to predict the renewal of the contract. Based on information collected retrospectively from customers who have purchased housing insurance policies, indicates the characteristics of customers who often have problems when purchasing insurance, such as lack of premium payment. Renewal of insurance policies and finding out the tendency of customers to renew the policy contract after the expiration date

## II.Methodology
This study used a home insurance dataset from the R-Studio class at the university "Université de Technologie de -Troyes (UTT), France". Data collection spanned 2007 to 2012 from Kaggle.com. This dataset was written and analyzed by Yabir Canario, containing a total of 256,173 rows and a total of 66 variables studied.

### DATA
**Variables Description**
* QUOTE_DATE: Day where the quotation was made
* COVER_START: Beginning of the cover payment
* CLAIM3YEARS: 3 last years loss
* P1EMPSTATUS: Client's professional status
* P1PTEMP_STATUS: Client's part-time professional status
* BUS_USE: Commercial use indicator
* CLERICAL: Administration office usage indicator
* AD_BUILDINGS: Building coverage - Self damage
* RISKRATEDAREA_B: Geographical Classification of Risk - Building
* SUMINSUREDBUILDINGS: Assured Sum - Building
* NCDGRANTEDYEARS_B: Bonus Malus - Building
* AD_CONTENTS: Coverage of personal items - Self Damage
* RISKRATEDAREA_C: Geographical Classification of Risk - Personal Objects
* SUMINSUREDCONTENTS: Assured Sum - Personal Items
* NCDGRANTEDYEARS_C: Malus Bonus - Personal Items
* CONTENTS_COVER: Coverage - Personal Objects indicator
* BUILDINGS_COVER: Cover - Building indicator
* SPECSUMINSURED: Assured Sum - Valuable Personal Property
* SPECITEMPREM: Premium - Personal valuable items
* UNSPECHRPPREM: Unknown
* P1_DOB: Date of birth of the client
* P1MARSTATUS: Marital status of the client
* P1POLICYREFUSED: Police Emission Denial Indicator
* P1_SEX: customer sex
* APPR_ALARM: Appropriate alarm
* APPR_LOCKS: Appropriate lock
* BEDROOMS: Number of bedrooms
* ROOF_CONSTRUCTION: Code of the type of construction of the roof
* WALL_CONSTRUCTION: Code of the type of wall construction
* FLOODING: House susceptible to floods
* LISTED: National Heritage Building
* MAXDAYSUNOCC: Number of days unoccupied
* NEIGH_WATCH: Vigils of proximity present
* OCC_STATUS: Occupancy status
* OWNERSHIP_TYPE: Type of membership
* PAYING_GUESTS: Presence of paying guests
* PROP_TYPE: Type of property
* SAFE_INSTALLED: Safe installs
* SECDISCREQ: Reduction of premium for security
* SUBSIDENCE: Subsidence indicator (relative downwards motion of the surface )
* YEARBUILT: Year of construction
* CAMPAIGN_DESC: Description of the marketing campaign
* PAYMENT_METHOD: Method of payment
* PAYMENT_FREQUENCY: Frequency of payment
* LEGALADDONPRE_REN: Option "Legal Fees" included before 1st renewal
* LEGALADDONPOST_REN: Option "Legal Fees" included after 1st renewal
* HOMEEMADDONPREREN: "Emergencies" option included before 1st renewal
* HOMEEMADDONPOSTREN: Option "Emergencies" included after 1st renewal
* GARDENADDONPRE_REN: Option "Gardens" included before 1st renewal
* GARDENADDONPOST_REN: Option "Gardens" included after 1st renewal
* KEYCAREADDONPRE_REN: Option "Replacement of keys" included before 1st renewal
* KEYCAREADDONPOST_REN: Option "Replacement of keys" included after 1st renewal
* HP1ADDONPRE_REN: Option "HP1" included before 1st renewal
* HP1ADDONPOST_REN: Option "HP1" included after 1st renewal
* HP2ADDONPRE_REN: Option "HP2" included before 1st renewal
* HP2ADDONPOST_REN: Option "HP2" included afterrenewal
* HP3ADDONPRE_REN: Option "HP3" included before 1st renewal
* HP3ADDONPOST_REN: Option "HP3" included after renewal
* MTA_FLAG: Mid-Term Adjustment indicator
* MTA_FAP: Bonus up to date of Adjustment
* MTA_APRP: Adjustment of the premium for Mid-Term Adjustmen
* MTA_DATE: Date of Mid-Term Adjustment
* LASTANNPREM_GROSS: Premium - Total for the previous year
* POL_STATUS: Police status
* Police: Police number

### Analyirc

The data analysis model uses Decision tree (DT) , K-nearest Neighbors Algorithm (KNN) , Logistic Regression (LOG), Naive Bayes classifier (NB) , Random forest (RF) , Support. Vector Machine Classifier (SVM) , XGBoost (XG) and remember to divide train 70 % and test 30 % data.


Starting from studying and understanding the current status of the policy customers both before and after preparation, the information can be divided into 4 types: still in the policy (Live), the policy contract expired (Lapsed), canceled (Cancelled) and unknown (Unknow). ) which the information before the data preparation There are total gaps of 26.2%, as shown in Fig. 1. When examined, it is found that there are multiple gaps in the table that we cannot analyze further. Therefore, cut off this row as shown in Figure 2 and replace the other spaces in the data using various techniques. The graph data from Piechart will be created as The new variable is Resiliated (renewal) and Non_Resiliated (non-renewal) gives the example in Figures 3 and 4 indicating the percentage renewal of the policy, where 0 means the customer does not renew the policy and 1 is the customer renews the policy.

**Figure 1 Before**
<p align="left">
  
  <img height ="300" width="450"  src="https://user-images.githubusercontent.com/63940535/132387060-2fb189a0-f5a7-4114-abf4-9f126fe64adb.png">

  
</p>

**Figure 2 After**
<p align="left">
 
  <img height ="300" width="450"  src="https://user-images.githubusercontent.com/63940535/132387124-085dd55a-6611-4f4d-8cb8-83acf2ac7546.png">

  
</p>

**Figure 3 Before**
<p align="left">
  

  <img height ="300" width="450"  src="https://user-images.githubusercontent.com/63940535/132387418-56c0dc23-a8a3-4936-8771-7a7a1f8c3413.png">
  
</p>

**Figure 4 After**
<p align="left">
 

  <img height ="300" width="450"  src="https://user-images.githubusercontent.com/63940535/132387427-9674863f-69d9-4323-bc52-1b8a4f93e028.png">
  
</p>

Then use the data to analyze the necessary data from the relationship of the variables by using Exploratory Data Analysis (EDA) on the data variables that are Qualitative Variable or Categorical Variable.

All data will be obtained in 2 types, namely, the selected variable data to be analyzed as shown in Figure 5, the variable data that cannot be analyzed as shown in Figure 6, which is the method of selection from the percentage difference of the policy contract renewal and non-renewal of the policy contract. If the percentage difference is large (more than 1.5 %), the variable will be used for analysis and the last type is the data that must be converted before being analyzed by means of changing the data to One Hot Encoding, which will be used with the data. with more than 2 answers class as shown in picture 7.

**Figure 5**
<p align="left">
 

  <img  width="1000"  src="https://user-images.githubusercontent.com/63940535/132388256-b55ef9af-7bf7-46cf-99b3-ac5f2ed41adf.png">
  
</p>

**Figure 6**
<p align="left">
 

  <img  width="1000"  src="https://user-images.githubusercontent.com/63940535/132388358-66dd7c34-1a81-46f0-af84-56008c4f6c39.png">
  
</p>



**Figure 7**
<p align="left">
 

  <img  width="1000"  src="https://user-images.githubusercontent.com/63940535/132388661-749a4f47-dfca-490b-a215-151d1b2a342f.png">
  
</p>

 
 Quantitative variables compare the data by choosing the mean and median of the data replacing blanks and changing the variables to Category. After selecting the variables, all 28 selected variables are obtained as follows: CLAIM3YEARS , P1_EMP_STATUS . , P1_PT_EMP_STATUS, AD_BUILDINGS, SUM_INSURED_BUILDINGS, SUM_INSURED_CONTENTS, CONTENTS_COVER, SPEC_SUM_INSURED, SPEC_ITEM_PREM, P1_MAR_STATUS, P1_SEX, APPR_LOCKS, MAX_DAYS_UNOCC, SEC_DISC_REQ, PAYMENT_METHOD, LEGAL_ADDON_PRE_REN, LEGAL_ADDON_POST_REN, HOME_EM_ADDON_PRE_REN, HOME_EM_ADDON_POST_REN, GARDEN_ADDON_PRE_REN, GARDEN_ADDON_POST_REN, KEYCARE_ADDON_PRE_REN, KEYCARE_ADDON_POST_REN, HP2_ADDON_PRE_REN, HP2_ADDON_POST_REN, MTA_FAP, MTA_APRP. , LAST_ANN_PREM_GROSS All prepared data were then used to make predictions from the selected variables.


## III.Result

| **Model**            | **Accuracy (%)**      | **Precision (%)**        |**Recall (%)**     |**Specificity (%)**       |**F1-score (%)**       |**RANK**       |
| -----------          | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- |
| Logistic Regression (LR)             | 69 | 93 | 70 | 40 | 80 | 7 |
| K-nearest Neighbors (KNN)            | 66 | 100| 61 | 0 | 76 | 10 |
| Support Vector Machine (Gaussian)    | 70 | 70 | 97 | 30 | 81 | 2 |
| Support Vector Machine (Linear)      | 69 | 69 | 97 | 27 | 81 | 4 |
| Support Vector Machine (Poly)        | 70 | 70 | 96 | 32 | 81 | 3 |
| Support Vector Machine (Sigmoid)     | 55 | 65 | 69 | 68 | 67 | 11|
| Decision Tree (DT)                   | 68 | 68 | 99 | 21 | 81 | 5 |
| Naive Bayes Classifier (NBC)         | 66 | 66 | 99 | 62 | 79 | 8 |
| Random Forest (RF)                   | 71 | 72 | 90 | 37 | 80 | 6 |
| XGboost Classifier (XGB)             | 72 | 72 | 93 | 34 | 81 | 1 |


Which from the selection. The model with the predicted result received the F1-Score. The model with the highest F1-Score was XGBoost, Decision Tree, SVM (Gaussian), SVM (Linear), and SVM (Poly) had an F1-Score percentage. Then look at Accuracy. The result is XGBoost. Accuracy is 71%. Then look at Precision. It is XGBoost. Precision is 72%. The most suitable model for this prediction is XGBoost, which descends in descending order based on rank.



Next, when analyzing which variables affect our model, we select from feature importance, which indicates which variable affects our model by selecting feature importance from the XGBoost model.


**Figure 7**

<p align="center">
 

  <img  width="800"  src="https://user-images.githubusercontent.com/63940535/132390750-82ff74d0-b31b-4f9e-909d-2f965760c3bd.png">
  
</p>


The variables that affect our model are PAYMENT_METHOD After that, when knowing which variable has importance and what is the Partial Dependence Plot (PDP), which is a method used to find the marginal effect of each feature that affects the model output (probability in the case of classification), which can see which features are more or less effective And how do the features correlate with the model's predictive results? According to the example in Figure 8,



**Figure 8**

<p align="center">
 

  <img  height="300" width="400"  src="https://user-images.githubusercontent.com/63940535/132391044-79ebe969-6cc1-4f12-8e0f-679441344f73.png">
  <img  height="300" width="400"  src="https://user-images.githubusercontent.com/63940535/132391102-7459ee7f-8398-4d18-b89d-7610553ee68d.png">
  
</p>


From Figure 8, it shows that when this variable PAYMENT_METHOD_is_PureDD has a value of 0, it will result in Resiliated, meaning that if the customer chooses not to pay by PureDD method, it will increase the chances of renewing the policy. When a customer pays a legal fee before renewal, they are more likely to renew their policy.


## IV.Conclusion & Discussion

From a study on the prediction of whether or not to cancel or renew a home insurance policy. Each model was used to see how accurate the prediction was.

The results of the analysis can be concluded that the ideal model for this dataset was XGBoost, looking at F1-Score, accuracy, precision, recall, and specificity, respectively. The prediction was 81 percent F1-Score, 71% Accuracy, 72% Precision, Recal 93 percent and Specificity 34 percent.

Usually the F1-Score or Accuracy should be greater than 90%, but the analyst's prediction was 81 percent F1-Score and 71 percent Accuracy, which is much less than the expected value. Based on the data obtained prior to the clean data, the Resiliated value (20.51 percent) was lower than that. Resiliated means that the data has an imbalance, and when cleaned, the data that may actually be usable is only 10 percent of the original value. The resulting value is therefore 33.81% and the non-resilient is 66.19 percent, with imbalances occurring anyway, and some features have inconsistent data collection and a lot of gaps. This may cause the subject to be less accurate.

A previous study [kaggle.com](https://www.kaggle.com/ycanario/home-insurance-in-r) suggested using the Decision Tree to make predictions, but looking at the previous study's decision tree, it didn't predict Resiliated at all, whereas the Analyzers' decision tree yielded only 68% Accuracy. Only, however, the Analyst's Decision tree model was predicted to be resiliated, meaning the Analyst's model was very effective. But when compared to the accuracy of the XGBoost, there is a 3% difference in accuracy, which is not much difference, but taking the parameters into account makes the XGBoost better.

As for the variables that most affect the model XGBoost are PAYMENT_METHOD_is_PUREDD, followed by LEGAL_ADDON_PRE_RENT, respectively, meaning that when customers choose not to pay by the PureDD method, they will have more chances to renew the policy, and when customers who pay legal fees before renewal are more likely to renew their policy contracts, for example.


## V.References

**BUNDLE & UNBUNDLE PRICING**

[1] forbes,*How AI And Machine Learning Are Used To Transform The Insurance Industry*,strategic business & technology advisor to governments and companies. [Online] Available: [forbes](https://www.forbes.com/sites/bernardmarr/2017/10/24/how-ai-and-machine-learning-are-used-to-transform-the-insurance-industry/#2e8b3a7913a1)

[2] lifeant,*What Happens When A Life Insurance Policy Lapses* ,Life Ant was started by Thomas Rockford in January 2014, with the goal of fitting each of our educated clients with the lowest-cost life insurance policy. [Online]Available: [lifeant](https://www.lifeant.com/happens-life-insurance-policy-lapses/)

[3] kaggle,*Home insurance in R*,Yabir Canario. [Online]Available: [kaggle](https://www.kaggle.com/ycanario/home-insurance-in-r)


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
 

  <img  width="1000"  src="https://user-images.githubusercontent.com/63940535/132388256-b55ef9af-7bf7-46cf-99b3-ac5f2ed41adf.png">
  
</p>


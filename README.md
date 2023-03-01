# 💳 Credit-Card-Default-Prediction
> Building a classification model for predicting whether a person is a defaulter or not.
## ❓ Need of a model
> - #### 1. Risk Management: 
A credit card default prediction model can help lenders manage their risk by identifying customers who are likely to default on their credit card payments. By predicting the likelihood of default, lenders can take preemptive measures to reduce their exposure to risk, such as adjusting credit limits or increasing interest rates.
> - #### 2. Cost Reduction: 
Defaulted credit card payments can be a significant cost to lenders, not just in terms of the money owed but also the cost of collections and legal actions. By predicting which customers are likely to default, lenders can take steps to prevent defaults, thereby reducing these costs.
> - #### 3. Customer Retention: 
Defaulted credit card payments can also lead to unhappy customers and lost business. By identifying customers who are at risk of defaulting and proactively working with them to find solutions, lenders can improve customer satisfaction and retention.
> - #### 4. Compliance: 
Regulatory authorities often require lenders to implement risk management processes that include credit risk models. A credit card default prediction model can help lenders comply with these requirements.
## :clipboard: Case Background:
> Global Waterhouse Consulting has been approached by American Express, one of the leading Financial Institutions all over the globe to solve a burning issue at their organization: Customers getting defaulted. AmEx is unable to make use of huge data of their customers to make business decisions to create a measurable economic benefit - increased revenue or reduced expenses or reduce the risk by minimizing loss . A Dataset has been provided with total 18 Features. The variable of interest is Credit Card Default.

## :bar_chart: Variables:
| Column ID |           Column Name           | Data type |             Description            |
|:---------:|:-------------------------------:|:---------:|:-----------------------------------:|
|     0     |          customer_id            |   object  | unique identification of a customer |
|     1     |             name                |   object  |      name of a customer|
|     2     |             age                 |   int64   |  Continous  |         age of a customer ( in years)|
|     3     |             gender              |   object  |gender of a customer( F means Female and M means Male )|
|     4     |           owns_car              |   object  |whether a customer owns a car (Y means Yes and N means No )|
|     5     | owns_house                      |   object  |whether a customer owns a house ( Y means Yes and N means No )|
|     6     |   no_of_children                |   float64 |number of children of a customer|
|     7     |   net_yearly_income             |   float64 |yearly income of a customer|
|     8     |  no_of_days_employed            |   float64 |no of days employed|
|     9     |      occupation_type            |   object  |occupation type of a customer ( IT staff, Managers, Accountants, Cooking staff, etc )|
|     10    |       total_family_members      |   float64 |number of family members of a customer|
|     11    |  migrant_worker                 |   object  |  float64  |whether a customer is a migrant worker( 1 means Yes and 0 means No )|
|     12    |  yearly_debt_payments           |   float64 |yearly debt payments of a customer ( in USD )|
|     13    | credit_limit                    |   float64 |credit limit of a customer ( in USD)|
|     14    | credit_limit_used(%)            |   int64   |percentage of credit limit used by a customer|
|     15    |     credit_score                |  float64  |credit score of a customer|
|     16    |     prev_defaults               |   int64   |number of previous defaults|
|     17    |     defaults_in_last_6months    |   int64   |whether a customer has defaulted in the last 6 months (1 means Yes and 0 means No)|
|     18    |     credit_card_default         |   int64   |whether there will be credit card default ( 1 means Yes and 0 means No )|

## 🛣️ Roadmap Followed:
> - ### 1.Preliminary data analysis:
Edit the data to prepare it for further analysis, describe the key features of the data, and summarize the results.
> - ### 2.Exploratory data analysis:
Investigate data sets and summarize their main characteristics, often employing data visualization methods.
> - ### 3.Data pre-processing:
The dataset is preprocessed in order to check missing values, noisy data, and other inconsistencies before executing it to the algorithm.
> - ### 4.Model development & classifictaion:
An iterative process, in which many models are derived, tested and built upon until a model fitting the desired criteria is built.

## :chart_with_upwards_trend: Conclusion of Preliminary Data Analysis:
> - #### 1.Missing Values:
Replacing nan values with the mode of the corresponding column.
> - #### 2.Irrelevant Values:
Replacing irrelevant values such as “XNA” or “Unknown” with mode of the corresponding column.
> - #### 3.Data Types Conversion:
Converting all datatypes to “int” for ease of model training.
> - #### 4.Categorical Division:
Transforming columns to categorical ones for improved understanding using encoding.

### ℹ️ Data Insights:
- The dominant values are of Female class which proves out to be a positive change in the society as more females are getting the opportunity of securing their income.
- Mostly people do not own a car. It reflects that car being considered as a luxury item does not limits people's ability to secure their money in a bank account which is good for the society.
- Around 30% of people do not own a house(considered a basic necessity) still have a bank account. It is a commendable increase in numbers since the last 10 years.
- Laborers being considered as not capable of having a bank account are the most contributing customers of the bank. This is improving the economy of the country.
- Most of the population comes under the category of migrant workers as people are always in search of better paying jobs and keep in looking after them.
- 92% of the population does not have a credit card default and only 8% of them have it.
- The citizens of the country are responsible and do understand the necessity of maintaining there bank accounts as:
  - 95% of the people do not have any previous default.
  - 5% of the population has 1 previous default.
  - 1% of the population has 2 previous defaults. 

## :handshake: Correlations:
![image](https://user-images.githubusercontent.com/95099754/222168148-a866cd8f-6782-4142-871a-d35a0c7abd60.png)

We will drop the three highly positively correlated columns with the target variable namely:
  - Credit_limit_used(%)
  - Defaults_in_last_6months
  - Prev_defaults

so as to avoid multicollinearity.

## :scroll: Models Used:
> - Random Forest: 0.997524118500811
> - GaussianNB: 0.5487919405788441
> - DecisionTreeClassifier: 0.9781439426278494
> - Adaboost: 0.8786818065397421
> - Xgboost: 0.9390420899854862
> - LGBM: 0.8960129770340647

## 🥇: Analysis Results:
![image](https://user-images.githubusercontent.com/95099754/222169970-b1610c2a-6ca8-4d3d-91fd-117449fc0103.png)

## 🧐:Recommendations:
### 🕴️:Business suggestions:
- ##### Improve customer segmentation:
A credit card default prediction model can help businesses to identify high-risk customers. Businesses can use this information to segment customers based on their creditworthiness and tailor their marketing and communication strategies accordingly.
- ##### Offer targeted credit counseling: 
For customers who are identified as high-risk by the credit card default prediction model, businesses can offer targeted credit counseling. This can include personalized recommendations for managing their credit card debt, setting up a payment plan, or reducing their credit utilization.
- ##### Adjust credit limits: 
Based on the credit card default prediction model's predictions, businesses can adjust the credit limits for individual customers. This can help to minimize credit risk while still providing customers with the credit they need.
- ##### Refine underwriting criteria: 
By analyzing the factors that contribute to credit card defaults, businesses can refine their underwriting criteria. This can include setting stricter credit score requirements, analyzing payment history more closely, or considering alternative data sources.

### 🛑:Limitations:
- ##### Changes in economic conditions: 
Credit card default prediction models are based on historical data, which may not reflect current economic conditions. Changes in the economy, such as a recession or changes in interest rates, can impact credit card defaults and make it difficult for the model to accurately predict credit risk.
- ##### Changes in customer behavior:
Credit card default prediction models assume that customers will continue to behave in a similar manner to how they have in the past. However, if a customer's behavior changes, such as if they start using their credit card more frequently or make larger purchases, the model's accuracy may be compromised.

### 🆕:Future Work:
##### Alternative data sources:
While credit score, payment history, and credit utilization are essential predictors of credit card defaults, businesses can also explore alternative data sources such as social media activity, online shopping behavior, and mobile phone usage data. By analyzing these data sources, businesses can gain additional insights into a customer's creditworthiness.

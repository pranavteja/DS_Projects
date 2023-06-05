Many people struggle to get loans due to insufficient or non-existent credit histories. And, unfortunately, this population is often taken advantage of by untrustworthy lenders.

Home Credit strives to broaden financial inclusion for the unbanked population by providing a positive and safe borrowing experience. In order to make sure this underserved population has a positive loan experience, Home Credit makes use of a variety of alternative data--including telco and transactional information--to predict their clients' repayment abilities.

While Home Credit is currently using various statistical and machine learning methods to make these predictions, they're challenging Kagglers to help them unlock the full potential of their data. Doing so will ensure that clients capable of repayment are not rejected and that loans are given with a principal, maturity, and repayment calendar that will empower their clients to be successful.


Evaluation
Submissions are evaluated on area under the ROC curve between the predicted probability and the observed target.

Datasets
![Screenshot_20230605_152658](https://github.com/pranavteja/DS_Projects/assets/45447693/8cb2146f-d867-4457-bacb-d429ead2da4b)
Process followed
Out of the many data tables provided here, each table is connected with another with a key id. First of all, we need to start analysis from the bottom tables.

For example, Bureau Balance table is connected to Bureau table with a key as SK_ID_BUREAU and also Bureau table is connected to Application Train/Test tables with a key as SK_ID_CURR.

We will start to analyze Bureau Balance first! Then, we will deduplicate the data according to the SK_ID_BUREAU variable and generate new variables to use on Bureau table. After that, the same processings should apply from Bureau table to Application Train/Test tables by using SK_ID_CURR.

When Bureau and Bureau Balance is done, we need to start analysis other bottom tables again to transfer information up!

Steps
Investigate intersections to key ids of tables!
All tables have different number of observations and variables. Moreover, when we merge two tables, some ids might not connect. That's why, sometimes we will see missing values naturally. The purpose of this step is to raise awareness for intersections. Also, a classification problem can include unbalanced target variable. If we work on a classification problem, we must look at target variable.

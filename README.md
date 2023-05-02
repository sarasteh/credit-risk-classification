# credit-risk-classification
Here we use various techniques to train and evaluate a model based on loan risk. The dataset includes historical lending activity from a peer-to-peer lending services company. We want to build a model that can identify the creditworthiness of borrowers. 
## Data Analysis
As shown in Figure.1, the dataset includes 7 columns. We use the first six columns as our feature set and the last column, *loan_status* is our label. The loan_status has two values, 0 and 1. A value of 0 means that the loan is healthy while a value of 1 shows that the loan has a high risk of defaulting. Here we mainly need to identify unhealthy loans (loan_status: 1). In order to have an accurate model we need to have a balance of data, in our case, we need to have enough risky loans in our dataset. If we look at the value_counts of "loan_status" we will see the total number of high risk loans is about 3% of the whole data (Figure.1).

![Figure.1](images/data_overview.png)

## Machine Learning Process
In the first part, data are splitted into training and testing datasets. Next, we fit a logistic regression model by using the training data and predict the testing data labels. Finally the model's performance is evaluated by using **accuracy score, confusion matrix and classification report**.

In the second part, we resample the date before training using the RandomOverSampler module. Then we do the same training and testing process to fit and evaluate the model.


# Supervised Machine Learning - Predicting Credit Risk

LendingClub is a peer-to-peer lending services company that allows individual investors to partially fund personal loans as well as buy and sell notes backing the loans on a secondary market. LendingClub offers their previous data through an API.

This data is used to create machine learning models, speicifally Logistic Regression model and Random Forest Classifier, to classify the risk level of given loans.



### Retrieving the data

In the `Generator` folder in `Resources`, there is a [GenerateData.ipynb](/Resources/Generator/GenerateData.ipynb) notebook that will download data from LendingClub and output two CSVs: 

* `2019loans.csv`
* `2020Q1loans.csv`

1 year of data (2019) is used to predict the credit risk of loans from the first quarter of the next year (2020).

Note: these two CSVs have been undersampled to give an even number of high risk and low risk loans. In the original dataset, only 2.2% of loans are categorized as high risk. To get a truly accurate model, special techniques need to be used on imbalanced data. Undersampling is one of those techniques. 


##  The models
Both models were initially trained with unscaled data. The random forest classifier performed better than the logistic regression in the first test. However, the random forest classifier model is overfitted to the training data (with a training score of 100%) and may not be the best representation for the 2020 test data.
The models were also trained with scaled data, and the results for the logistic regression test improved. Additionally, the logistic regression performed better for the scaled data than random forest classifier model, with scores of .72 and .62 respecitvely.

### References

LendingClub (2019-2020) _Loan Stats_. Retrieved from: [https://resources.lendingclub.com/](https://resources.lendingclub.com/)



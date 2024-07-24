# Credit Card Fraud Project
This project covers credit card fraud and is meant to look at a dataset of transactions and predict whether it is fraudulent or not.
There are 30 features in this dataset, each in a separate column. Features V1-V28 is result of a PCA Dimensionality reduction to protect user identities and sensitive information. The Time column details the number of seconds elapsed between this transaction and the first transaction in the dataset.
The CSV included in this repository is a sampled version to reduce the file size. Here is the link to the original CSV: https://www.kaggle.com/code/mendozav/credit-card-fraud-detection-project/input 

1. The data is biased. The label for the data is Class of transaction. This can take value 1 if fraudulent, else value 0. Value 0 are overwhelmingly large, representing 99.85% of the data. 
  
2. The project already has a high accuracy but I changed the code to include Isolation Forest in the classifier before fitting the model. This increased the accuracy to 99%. 
   
3. I then handled the bias in the dataset by adding a Random Forest Classifier. Random Forest handles bias in data by Class weighting - assigning different weights to classes, making the model more sensitive to the minority class. This is done by setting the class_weight parameter to 'balanced', which automatically adjusts weights inversely proportional to class frequencies. It also uses bagging to create diverse trees by training each on a subset of data. Lastly, it evaluates the importance of each feature for making accurate predictions, enabling it to focus on the most informative features. The accuracy increased to 99.95%.
   
4. We then reduced the amount of features, by only including the 2 most important ones. The accuracy slightly reduced to 99.92%. 

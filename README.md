# ML_FinalProject_BreastCancer
This project uses data (features) computed from a digitized image of a fine needle aspirate (FNA) of a breast mass to train a neural network that can help diagnose breast cancer. 

## Disclaimer - Data Source:
### Creators: 

1. Dr. William H. Wolberg, General Surgery Dept. 
University of Wisconsin, Clinical Sciences Center 
Madison, WI 53792 
wolberg '@' eagle.surgery.wisc.edu 

2. W. Nick Street, Computer Sciences Dept. 
University of Wisconsin, 1210 West Dayton St., Madison, WI 53706 
street '@' cs.wisc.edu 608-262-6619 

3. Olvi L. Mangasarian, Computer Sciences Dept. 
University of Wisconsin, 1210 West Dayton St., Madison, WI 53706 
olvi '@' cs.wisc.edu 

### Donor: 
Nick Street

## Group Member
Jianhong Zhang;  
Stephen Ho;  
Kewei Chen;  
David Wang;  


## Prerequisites

Python 3 is required and a series of Python packages

```
Python 3 can be downloaded from here: https://www.python.org
Python packages can be installed in various different ways. One of the simple ones is using Anaconda where some of the frequently used Python packages are installed as part of the installation of Anaconda. https://www.anaconda.com
```

## 1. Data Preparation and Pre-prediction Exploratory Data Analysis
The data we selected is computed from a digitized image of a fine needle aspirate (FNA) of a breast mass. The goal is to use this data to predict whether the tumor is cancerous (Malignant) or not (Benign).  

This is a typical classification problem.  

We loaded the data and did some basic checks which includes:  

a. initial data scaning to understand the structure  
b. some basic statiscal check to spot any potential data issue  
c. added the necessary data columns and created a dataframe  
d. changed the categorical name (M/B) to categorical code (1/0)  
e. used seaborn charts to scan through the relationships between these data features as well as their relationship to categorical results (diaganosis results)  


## 2. Apply Classification and Plot the ROC

Since this is a classification problem (predict whether a tumor is cancerous or not), various different classification techniques from sikit learn can be used. We tried a few different ones (KNN, SVM, Random Forest, LogisticRegression, etc) and we found SVM produces better results.

In this exerciese, we also used 5 fold cross valiation to find the best parameters.
Another technique we employed is adding noise. Adding noise expands the size of the training dataset. Each time a training sample is exposed to the model, random noise is added to the input variables making them different every time when it's exposed to the model. This makes the training process more robust and reduce generalization error.


## 3. Feature Selection

This ranks the importance of each feature using Decision Tree Regressor.
We found 'perimeter_worst' feature is the most important one. This feature is the mean of the three largest tumor perimeter values. The bigger the tumor, the greater the risk that it is cancerous.

We also plot the ROC using only the selected important features for training. Comparing the result with the previous one, it shows just a little improvement.

## 4. Create a Confusion Matrix using the Testing Dataset

## 5. Apply PCA

We applied the PCA and created a new dataframe. We then used SGD classifier on the newly created dataframe. GridsearchCV is used to find the best parameters that explain the training dataset. (including the ideal number of PCA components)

Further more, we explored the top 3 principle components.
We graphed these principle components with Malignant / Benign values show which principle component is more important to determine whether the tumore is Malignant or Benign.

## 6. Visualising high-dimensional datasets t-SNE (t-distributed Stochastic Neighbor Embedding)

Just for fun, we employed t-SNE technique to see how it can visually cluster the data. 
t-SNE takes the high dimentional dataset and reduces it to low dimentional graph but retains a lot of the original information.

## 7. Create Neural Network (Keras)

	

 Conclusions and Recommendations
State your major findings from different sections. 
State your recommendation to the company that they can put into place to solve their problem.
Recommend the improvement techniques for better prediction results

Datasets
Provide the dataset link in the Google sheet shared with you and write the title and short description of the project there. Please inform your instructor and CC the teammates about it. One of you in the group should send the email.

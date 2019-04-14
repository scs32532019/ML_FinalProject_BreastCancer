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


## 3. 

3. Conclusions and Recommendations
a. Visualizing the data and results 
b. Recommend your future steps for improving the resuls
c. Apply cluster analysis (k-Means and DBSCAN)


Data Preparation and Pre-prediction Analysis (Exploratory Data Analysis) 

The first and foremost step of data mining process is to understand the data and identify the research question(s). Here are some suggestions to explore and understand datasets:

Look at the attribute type; e.g., categorical, ordinal or quantitative.
Find max, min, mean and standard deviation of attributes.
Determine any outlier values (records) for each of the attributes or attributes under
consideration (min, max, std. dev, scatter plots, box plots or others can be used).
Analyze the distribution of numeric attributes (normal or other). 
Plot histograms for attributes of concern and analyze whether they have any influence on the class
Try to answer these questions by different visualization techniques:
Which attributes seem to be most linked to the class attribute?
Which attributes seem to be most linked to the class attribute?
Which attributes do you think can be eliminated or included in the analysis?
Determine whether the dataset has an imbalanced class distribution (same
proportion of records of different types or not).
 Predictive Modeling
After an overall understanding about the dataset, you can use classification algorithms/ Also, choose a classification algorithm of your own choice, explain it a at a high level and compare your results
You will predict the class attribute by using each classification algorithm
Determine the right strategy for dataset split: simple training or testing, 10-fold cross validation, 3-fold cross validation, predictive model hyperparameters, etc
Use the dimensionality reduction algorithms in the preprocessing step and make
Determine your performance measures (accuracy, precision, recall, etc.).
Identify which algorithm performs well and in which settings.
	

 Conclusions and Recommendations
State your major findings from different sections. 
State your recommendation to the company that they can put into place to solve their problem.
Recommend the improvement techniques for better prediction results

Datasets
Provide the dataset link in the Google sheet shared with you and write the title and short description of the project there. Please inform your instructor and CC the teammates about it. One of you in the group should send the email.

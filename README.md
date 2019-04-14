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

First of all, we created a plotting function that can plot the loss/accuracy against the number of epochs on the training and validation dataset. This works similar as tensor board.

We then created a Sequential netwrok with 5 layers (input/output + 3 hidden layers). Another feature we added is 'dropout' which can help adjust weights to avoid over fitting and reduce running time.
	
In the end, we compared the Keras prediction results with the SVM results using ROC. It shows the Keras result is slightly better.

## Conclusions and Recommendations

We found the size of the tumor is the most important deterministic factor to conclude whethter the tumor is Malignant or Benign. Both Keras and SVM have been performing well to predict whether the tumor is cancerous or not. (with Keras being slightly better)

In this exercise, we found adding noise generally helps the training process. 

This dataset only has 568 samples, a larger amount of samples could help with better prediction results. This classification technique (either neural network or scikitlearn) can be employed to analyze the tumor once standard data collection, cleaning pipeline is established. 



# Breast Cancer Classification

![](https://static01.nyt.com/images/2019/11/05/smarter-living/24gubar-AI/24gubar-AI-articleLarge.jpg?quality=75&auto=webp&disable=upscale.png)

## Overview + Purpose

The purpose of building and analyzing 2 machine learning classifier models is to determine which classifier model most accurately diagnoses patients with breast cancer, defined as a person who encompasses a malignant tumor. Along with that, the breast cancer dataset was used to analyse which factors caused breast tumors to be “malignant” through exploratory data analysis. 


## Motivations

As someone who is interested in going into healthcare field, learning about effective systems to more accurately diagnose patients and/or find early signs of cancer can significantly reduce rates of tumors going malignant and offer better treatment faster. 


## Dataset

The dataset used for this project is the Breast Cancer Wisconsin (Diagnostic) Data Set https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic) obtained by the University of California, Irvine. This dataset contains about 32 features. 


## Dependencies

Scipy

Numpy

Matplotlib

Pandas

Sklearn

Seaborn


## Data Visualization for EDA

### Starters

1. Import dataset and read
2. Create new dataframe with pandas
3. Functions df.head() and df.describe() used to get an overview of the dataset
4. missingno.matrix() used to check for missing data (by visual gaps in graphic) 
5. Deleted irrelevant columns (‘Unnamed : 32’  and ‘id) 
6. Plot histograms for each variable to check each distribution
7. Check correlation between different variables
   
   a.Scatter matrix
  
   b. df.corr() function


### Feature Exploration

The following features were further investigated: 

‘Radius_worst’

‘Texture_worst’

‘Perimeter_worst’

The following features were selected because the features selected are strongly correlated with women diagnosed with a malignant tumor. I mainly wanted to further see how the following features are distributed by various graphs.



## Testing Classification Models + Results

In this project, two learning models were created, such as the support- vectoring model and K- nearest neighbors in order to compare how accurate the models when it came to classifying patients’ diagnoses as ‘benign’ or ‘malignant.’ 

### Support Vector Machine

A support vector machine is a supervised learning model that either classifies or uses a regression task to analyze a set of data. In this case, since this project classifier that determines a class (benign or malignant) based on where the data point falls on the hyperplane. SVMs are based on the idea of finding a hyperplane that best divides a dataset into two classes. The hyperplane is determined by where the 2 classes get divided. How far the hyperplane is to the 2 closest class points is considered the margin. In this case, since the 2 classes in this project are ‘benign’ (identified as the number 2) and ‘malignant’ (identified as number 4), we need to determine, using the features where the 2 classes can be divided in order to predict behavior. 

![](https://imgur.com/NPL9gsJ.png)

### K- Nearest Neighbors

K- Nearest Neighbor is a non- parametric (lazy) learning algorithm that either uses classification or regression on data sets given. It’s considered “lazy” because this machine learning model does not make generalizations about the datasets. Thus, it requires minimal training because the model keeps all the data when classifying data. Mainly, “the kNN algorithms find the k nearest neighbors of a query point and compute the class label (classification) based on the k nearest (most “similar”) points.” 

![](https://imgur.com/9wkAKXC.png)

### ML Task

The steps in which we tested classification models

1. Test and training data were split (80/20)

2. Models are defined to be trained (in this case SVM and KNN), using training data

3. After the models were defined and trained, then test data was given to models in order to determine how accurate the models are in diagnosing patients with breast cancer. 

### Results

![](https://imgur.com/F0x6RQ4.png)


## Improvements

One thing I didn't do was tune the parameters when implementing the ML models. Leaving parameters untuned can potentially make the results from the models skewed and favor one ML model over the other.

## Resources

https://towardsdatascience.com/a-gentle-introduction-to-exploratory-data-analysis-f11d843b8184

https://github.com/dformoso/sklearn-classification/blob/master/Data%20Science%20Workbook%20-%20Census%20Income%20Dataset.ipynb

https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic)

??? Banner


# KNN Car Classifier

This project is an exploration of the KNN classfier including data processing and analysis.

#
## Author

- Kenji Alford [Git](https://www.github.com/333kenji)

Notebook(s) for this project can be found [here](https://github.com/333Kenji/CarClassifier_KNN/tree/main/Notebooks).

---

<!-- TABLE OF CONTENTS -->
<details>
    
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>


---

![alt text](https://github.com/333Kenji/CarClassifier_KNNCarClassifier_KNN/blob/main/Images/banner.jpg "Final")
The notebook(s) for this project can be found here.


## Motivations

As part of a series of basic projects, I'm using this project to build intuition in the process of applying the KNN algorithm as a classifier.

### Real World Problem
It'd be great to be able to look at a large number of vehicles and find a particular class based on its features.

### ML Problem
The problem will be to build a model capable of discerning the highest quality vehicles from the test set.

### Solution
- After examing and preparing the data I will build a pipeline that'll encode the independent feature values into ordinal categorical features. I'll then use this pipeline for hyperperameter tuning, training, and testing/evaluating the optimal KNN model.

#### Target
The target for this project will the highest class of car in the dataset, classed as the 'vhigh' value.

#### Goals: Project Objectives
- A classification model that has an optimal number of k and an accuracy of at least 95%

#### Evaluation Metrics:
* Accuracy: .97
* Precision: 1
* Recall: .41
* F1 Scores: .58

Also,
    - elbow method
![alt text](https://github.com/333Kenji/CarClassifier_KNN/blob/main/Images/elbow.jpg "Elbow Method")

#### Optimal Hyperperamters:
k = 5


---
# Methodologies
- Feature Analysis and Comparison with Pandas, Numpy, SciPy stats module, and matplotlib/Seaborn.
- Encoding string-type ordinal categorial variable values as numeric values using the scikit-learn encoding module.
- Hyperperameter Tuning and Model Selection using the scikit-learn implementation of KNN Classifier algorithm within a pipeline built using the scikit-learn pipeline module.
- Training and Testing/Evalution of model using the scikit-learn metrics module and a specialized score/confusion matrix visualization.

## Libraries and Technologies
- Python
- Numpy, Pandas
- Scikit-learn modules
  * neighbors
  * metrics
  * preprocessing
  * pipeline/compose
  * model_selection
- SciPy Stats
- Seaborn/Matplotlib
- Jupyter/VSCde

---
# Project Description
 ## The Data
 
The data for this project comes from Kaggle. Although I wrangle raw data in other projects I wanted to focus on the rest of preprocessing via pipelining. The the data features car evaluation metrics for classification, such as number of doors, safety, and maintenance cost - each bearing a range of 3-5 categorically ordered values like 'unacc', 'acc', 'vgood', and 'good' for the car_class feature.
![alt text](https://github.com/333Kenji/CarClassifier_KNN/blob/main/Images/rawdata.jpg "Final")


### Data Dictionary
* price    overall price
* buying   buying price
* maint    price of the maintenance
* doors    number of doors
* persons  capacity in terms of persons to carry
* lug_boot the size of luggage boot
* safety   estimated safety of the car The dataset is simple with some minor variation amongst feature variations



### Collection Date
- 4/5/2022

### Data Source
* The UC Irvine data archive is a repository of publicly-accessible data sets for research.

https://archive.ics.uci.edu/ml/datasets/Car+Evaluation


## Preprocessing
The 1728 row of data have 7 features. Since this is a classification problem I'll be selecting one to be the target, leaving me with 6 features to work with.

This data is extremely clean, which is great for a simple project. Although the mostly even splits throughout the data are initially concerning, there doesn't seem to be any significant overlap, at this time.
## Feature Analysis and Comparison
Since I'd like this to remain a simple KNN classifier project I will need to generate a new column for the specific value I'm training the model to find.

Since all my independent features are ordinal categorical variables I won't need to scale the data. Despite this meaning I *could* seperate out the target and create the train and test splits I'm going to keep to good practice and handle this now.

Since I'm using 'car_class' as the model's target I'll need to deal with its four labels, unacc, acc, good, and vgood by  converting them to numeric values and selecting one for each test I'd like to run.

What the Chi2 contingency scores look like prior to preprocessing and selecting a specific class as the target.*<br />*
![alt text](https://github.com/333Kenji/CarClassifier_KNN/blob/main/Images/chibefore.jpg "Final")

And after. Note the closeness of car_class and target.*<br />*
![alt text](https://github.com/333Kenji/CarClassifier_KNN/blob/main/Images/chiafter.jpg "Final")

Values for features remaining in X after encoding.*<br />*
![alt text](https://github.com/333Kenji/CarClassifier_KNN/blob/main/Images/xafterprocessing.jpg "Final")

## Hyperperameter Tuning and Model Selection
Having built successfully built a pipline that encodes text values into numeric while reserving order I can now add one last pipleine layer which will also include the classifier. Using cross validation and the elbow method of visualy analyzing the optimal train and test scores I'll select the final k.

Using the elbow method.
![alt text](https://github.com/333Kenji/CarClassifier_KNN/blob/main/Images/elbow.jpg "Final")

Looks like a k of 5 is the best.*<br />*
![alt text](https://github.com/333Kenji/CarClassifier_KNN/blob/main/Images/kscores.jpg "Final")

## Model Evalution
The model with a  or 5 scores .97*<br />*

![alt text](https://github.com/333Kenji/CarClassifier_KNN/blob/main/Images/predictionsandprobs.jpg "Final")

Some of these probabilities are interesting (.8 vs .2 and .6 vs .4)*<br />*
This might bear further investigation as to whether these probabilities correspond to additional populations within the data.

And finally, confusion matrix.*<br />*
![alt text](https://github.com/333Kenji/CarClassifier_KNN/blob/main/Images/matrixscores.jpg "Final")




  - Choosing the 'class' feature as my target this becomes a multilabel classification probem because that feature has four possible ordinal values: 'unacc' (unacceptable), 'acc' (acceptable), 'good', and 'vgood' (very good).
  - By using the KNN algorithm I'm able to leverage it's grouping ability to classify across more than to labels as would be the cade with a simple application of logistic regression.
- Data Visualization
    - Using Seaborn for my primary analysis and I also use Pandas to view the data as it moves through each preprocessing and transformation phase wih evaluaion (elbow) produced via a simple matplotlib plot.
- Predictive Modeling
- etc.
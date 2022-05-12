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
- Feature Analysis and comparison with Pandas, Numpy, SciPy stats module, and matplotlib/Seaborn.
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
 
![alt text](https://github.com/333Kenji/CarClassifier_KNN/blob/main/Images/rawdata.jpg "Final")
The data for this project comes from Kaggle. Although I wrangle raw data in other projects I wanted to focus on the rest of preprocessing via pipelining. The the data features car evaluation metrics for classification, such as number of doors, safety, and maintenance cost - each bearing a range of 3-5 categorically ordered values like 'unacc', 'acc', 'vgood', and 'good' for the car_class feature.

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


How Sources May Be Related
Variables Directory
- column headings
- types
- number of variables
- units of measurement
- Definition of missing data
Directory Tree
Description of Methods of Data Processing
- Wrangling
- Transformation
- Encoding
- Scaling

---
## Summary
### Noteworthy Findings w/Graphics
- this
- that
- and another thing


Information About Model
Model Evaluation
    - [Model Card](https://arxiv.org/pdf/1810.03993.pdf)
Predictions
Real World Applications

---
<!-- ROADMAP -->
## Roadmap

- [x] Add Changelog
- [x] Add back to top links
- [ ] Add Additional Templates w/ Examples
- [ ] Add "components" document to easily copy & paste sections of the readme
- [ ] Multi-language Support
    - [ ] Chinese
    - [ ] Spanish



    - Choosing the 'class' feature as my target this becomes a multilabel classification probem because that feature has four possible ordinal values: 'unacc' (unacceptable), 'acc' (acceptable), 'good', and 'vgood' (very good).
    By using the KNN algorithm I'm able to leverage it's grouping ability to classify across more than to labels as would be the cade with a simple application of logistic regression.
- Data Visualization
    - Using Seaborn for my primary analysis and I also use Pandas to view the data as it moves through each preprocessing and transformation phase wih evaluaion (elbow) produced via a simple matplotlib plot.
- Predictive Modeling
- etc.
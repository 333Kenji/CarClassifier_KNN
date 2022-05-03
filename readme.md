??? Banner


# KNN Car Flassiier

This project is an exploration of the KNN classfier including data processing and analysis.

## Authors

- Kenji Alford [GIT](https://www.github.com/333kenji)

??? Embiggen (or not)
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
??? Linky
The notebook(s) for this project can be found here.


## Motivations

As part of a series of basic projects, I'm using this project to build intuition in the process of applying the KNN algorithm as a classifier.

My target for this project will be the datasets 'class' feature which denotes vehicle quality. The problem then will be to build a classifier that can discern a car's quality by looking at its features.
The Solution
- Since the dataset is quite clean, I will simply have to encode and scale the data before applying the algorithm which will then discern the typical features belonging to each class.
- Evaluation Metrics.
    - Using the elbow method.
    
Goals: Project Objectives
- A classification model that has an optimal number of k and an accuracy of at least 95%



---
## Methodologies
### Methods Employed
- Feature Analisys
- Machine Learning
    - Choosing the 'class' feature as my target this becomes a multilabel classification probem because that feature has four possible ordinal values: 'unacc' (unacceptable), 'acc' (acceptable), 'good', and 'vgood' (very good).
    By using the KNN algorithm I'm able to leverage it's grouping ability to classify across more than to labels as would be the cade with a simple application of logistic regression.
- Data Visualization
    - Using Seaborn for my primary analysis and I also use Pandas to view the data as it moves through each preprocessing and transformation phase wih evaluaion (elbow) produced via a simple matplotlib plot.
- Predictive Modeling
- etc.
## Libraries and Technologies
- Python
- Numpy, Pandas
- Scikit-learn
- Jupyter, VSCde

---
## Project Description
### Technical Aspect
This project is broken ito two parts.
1. stages of what you’re doing
2. can be broken down
    1. into
    2. a tree
 ### Experimental Design
 - target
 - the control/test split
 - the validation set
 - ML algorithm stack
 ### The Data

Description of Data Acquisition
Date of collection
Description of each data source
- Source
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
# EWHA_ML_07
This is the repository of team 7 기괴학습.
We classify 

## 📌Introduction
### Closed-world scenario
For the closed-world experiments, the objective is to classify the 95 monitored websites.

We run three models for closed-world setting, the file starts with the prefix `closed_`.

### Open-world scenario
For the open-world experiments, two goals will be achieved using `binary classification` and `multi-class classification`.
In both cases, monitored website instances are treated as positive samples, and unmonitored website instances are treated as negative samples.

1) `Binary Classification`: Determine whether the web traffic trace corresponds to a monitored website.   
 To do this, we reassign the label '1' to all monitored website instances (positive samples) and assign the label '-1' to all unmonitored website instances (negative samples). 

2) `Multi-Class Classification`: Classify 95 monitored website traces with unique labels against additional unmonitored websites.
   In the multi-class setting, we label the monitored website instances with {0, 1, 2, ..., 94} and the unmonitored website instances with the label '-1'.

We run three models for each binary and multi-class classification. 
For binary classification, the file starts with the prefix `open_binary`. 
For multi-class classification, the file starts with the prefix `open_multi`.

## 📌Models
We use three models for the project.
### RandomForest

### k-NN

### Decision Tree

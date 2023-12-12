# EWHA_ML_07
This is the repository of the team 7 기괴학습.</br>

## 📌Introduction
The aim of this project is to create machine learning models using Tor network packet flow data, to determine whether an instance is communicating with a monitored website or an unmonitored website, and to identify its destination if it is a monitored website.

### 🌐Closed-world scenario
For the closed-world experiments, the objective is to classify the 95 monitored websites.</br>
We run three models for closed-world setting with the files that starts with the prefix `closed_`.

### 🌐Open-world scenario
For the open-world experiments, two goals will be achieved using `binary classification` and `multi-class classification`.</br>
In both cases, monitored website instances are treated as positive samples, and unmonitored website instances are treated as negative samples.

1) `Binary Classification`: Determine whether the web traffic trace corresponds to a monitored website.   
 To do this, we reassign the label '1' to all monitored website instances (positive samples) and assign the label '-1' to all unmonitored website instances (negative samples). 

2) `Multi-Class Classification`: Classify 95 monitored website traces with unique labels against additional unmonitored websites.</br>
   In the multi-class setting, we label the monitored website instances with {0, 1, 2, ..., 94} and the unmonitored website instances with the label '-1'.

We run three models for each binary and multi-class classification. </br>
Files for binary classification start with the prefix `open_binary`. </br>
Files for multi-class classification start with the prefix `open_multi`.

## 📌How to run
- You need `colab` to run the files.
- If you run `load_pickle_code_hw.ipynb` in `Feature Engineering` folder, you can obtain the file `mon.csv` which is used for the files that start with the prefix `closed_`.
- If you run `load_pickle_code_hw_unmon.ipynb` in `Feature Engineering` folder, you can obtain the files `unmon.csv` and `unmon2.csv` which are used for the files that start with the prefix `open_`.
- You can find this code below in the files named `load_pickle_code_hw.ipynb` and `load_pickle_code_hw_unmon.ipynb`.
```
with open('/content/drive/MyDrive/Colab Notebooks/2023_2_ML/mon_standard10.pkl', 'rb') as f: 
```
```
with open('/content/drive/MyDrive/Colab Notebooks/2023_2_ML/unmon_standard10.pkl', 'rb') as f:
```
You need to replace the path in this code with the absolute path of the files `mon_standard10.pkl` and `unmon_standard10.pkl` on your drive.</br> </br>
⚠️If there's any problem when running files in `Feature Engineering` folder, you can use the results of feature engineering in the `Features` folder for following steps.
- After obtaining the files `mon.csv`, `unmon.csv`, and `unmon2.csv`, you should upload them on your google drive.
- You can find this code below in every file in `DecisionTree`, `KNN`, `RandomForest` folders.
  ```
  pd.read_csv("/content/drive/MyDrive/Machine Learning/팀 과제/mon.csv", header=None)
  ```
  Please replace the path with the absolute path of the files `mon.csv`, `unmon.csv`, and `unmon2.csv` on your drive.

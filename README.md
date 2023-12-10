# EWHA_ML_07
This is the repository of the team 7 기괴학습.</br>

## 📌Introduction
The aim of the project is to create a machine learning model using network packet flow data detected by Tor, to determine whether the arbitrary data is being monitored by Tor and to identify its destination.
### 🌐Closed-world scenario
For the closed-world experiments, the objective is to classify the 95 monitored websites.</br>
We run three models for closed-world setting, the file starts with the prefix `closed_`.

### 🌐Open-world scenario
For the open-world experiments, two goals will be achieved using `binary classification` and `multi-class classification`.</br>
In both cases, monitored website instances are treated as positive samples, and unmonitored website instances are treated as negative samples.

1) `Binary Classification`: Determine whether the web traffic trace corresponds to a monitored website.   
 To do this, we reassign the label '1' to all monitored website instances (positive samples) and assign the label '-1' to all unmonitored website instances (negative samples). 

2) `Multi-Class Classification`: Classify 95 monitored website traces with unique labels against additional unmonitored websites.</br>
   In the multi-class setting, we label the monitored website instances with {0, 1, 2, ..., 94} and the unmonitored website instances with the label '-1'.

We run three models for each binary and multi-class classification. </br>
For binary classification, the file starts with the prefix `open_binary`. </br>
For multi-class classification, the file starts with the prefix `open_multi`.

## 📌How to run
- You need `colab` to run the files.
- If you run `load_pickle_code_hw.ipynb` in `Feature Extraction` folder, you can obtain the file `mon.csv` which is used for the files starts with the prefix `closed_`.
- If you run `load_pickle_code_hw_unmon.ipynb` in `Feature Extraction` folder, you can obtain the files `unmon.csv` and `unmon2.csv` which are used for the files starts with the prefix `open_`.
- You can find this code in file named `load_pickle_code_hw.ipynb` and `load_pickle_code_hw_unmon.ipynb`.
```
with open('/content/drive/MyDrive/Colab Notebooks/2023_2_ML/mon_standard10.pkl', 'rb') as f: 
```
```
with open('/content/drive/MyDrive/Colab Notebooks/2023_2_ML/unmon_standard10.pkl', 'rb') as f:
```
You need to replace the name of the path in this code with the absolute path in the file `mon_standard10.pkl` and `unmon_standard10.pkl` on your drive.
- After obtain the files, you should upload them on your google drive.
- You can find this code in every file in `DecisionTree`, `KNN`, `RandomForest` folder.
  ```
  pd.read_csv("/content/drive/MyDrive/Machine Learning/팀 과제/mon.csv", header=None)
  ```
  Please replace `"/content/drive/MyDrive/Machine Learning/팀 과제/mon.csv"` with the absolute path in the file `mon.csv`, `unmon.csv`, `unmon2.csv` on your drive.

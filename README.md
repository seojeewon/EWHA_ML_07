# EWHA_ML_07
This is the repository of team 7 기괴학습.</br>

We classify 95 websites in closed-world scenario. </br>
In open-world scenario, we classify whether the site is monitored or not and classify if the site is monitored, and if it is monitored, we classify which site it is. It depends on the dataset.

## 📌Introduction
### 🌐Closed-world scenario
For the closed-world experiments, the objective is to classify the 95 monitored websites.
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
- After obtain the files, you should upload them on your google drive.
- You can find this code in every file exclude the files in Feature Extraction folder.
  ```
  pd.read_csv("/content/drive/MyDrive/Machine Learning/팀 과제/mon.csv", header=None)
  ```
  Please replace `"/content/drive/MyDrive/Machine Learning/팀 과제/mon.csv"` with your file path.

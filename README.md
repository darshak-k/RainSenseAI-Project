# RainSenseAI (Group 18)

This project name combines the elements of rainfall and AI while emphasizing the notion of sensing or detecting rain. "RainSenseAI" implies the use of artificial intelligence to develop a sophisticated sensing system for rainfall in Australia. The name suggests a focus on leveraging AI algorithms and techniques to enhance the understanding and detection of rain patterns. It conveys the idea of utilizing AI to sense and analyze rainfall data, potentially leading to improved weather classification and predictions.

#Dataset Reference
https://www.kaggle.com/datasets/jsphyg/weather-dataset-rattle-package

| Parameters       | Statistics |
| ---------------- | ---------- |
| Total Records    | 145,460    |
| Total Features   | 23         |
| Date Field       | 1          |
| Text Fields      | 10         |
| Numeric Fields   | 12         |
| Missing values   | Yes        |


## Results

| Model Name                             | Accuracy | Precision | Recall | F1-Score | ROC  |
| -------------------------------------- | -------- | --------- | ------ | -------- | ---- |
| Supervised W/O parameter                | 97.4%    | 0.983     | 1.0    | 0.991    | 1.0  |
| Supervised With parameter               | 99.50%   | 1.0       | 1.0    | 1.0      | 1.0  |
| Semi-Supervised                         | 97.4%    | 1.0       | 1.0    | 1.0      | 1.0  |
| Recurrent Neural Network                | 100%     | 1.0       | 1.0    | 1.0      | 1.0  |

Table: Comparison of 4 models.


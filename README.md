# RainSenseAI

This project name combines the elements of rainfall and AI while emphasizing the notion of sensing or detecting rain. "RainSenseAI" implies the use of artificial intelligence to develop a sophisticated sensing system for rainfall in Australia. The name suggests a focus on leveraging AI algorithms and techniques to enhance the understanding and detection of rain patterns. It conveys the idea of utilizing AI to sense and analyze rainfall data, potentially leading to improved weather classification and predictions.

#Dataset Reference
https://www.kaggle.com/datasets/jsphyg/weather-dataset-rattle-package

#Initial draft:

```python
import pandas as pd
from sklearn.preprocessing import MinMaxScaler

# Load dataset
fullFileName = ''

df = pd.read_csv(fullFileName)

# Convert the date column to integer format
ref_date = pd.Timestamp('1900-01-01')
df['Date'] = (pd.to_datetime(df['Date']) - ref_date).dt.days

# Create a MinMaxScaler object
scaler = MinMaxScaler()

# Min-Max scale the 'Total Volume' column
df['AveragePrice'] = scaler.fit_transform(df[['AveragePrice']])

# Print the scaled dataframe
print(df) 

import pandas as pd
from sklearn.tree import DecisionTreeClassifier
from sklearn.model_selection import train_test_split
from sklearn.metrics import accuracy_score

X = df.values[:,1:13]
Y = df.values[:,0]
# Split the dataset into training and testing sets
X_train, X_test, y_train, y_test = train_test_split(X,Y,test_size=0.3, random_state=50)

# Create a decision tree classifier object
clf = DecisionTreeClassifier()

# Train the decision tree classifier on the training data
clf.fit(X_train, y_train)

# Make predictions on the testing data
y_pred = clf.predict(X_test)

# Evaluate the accuracy of the model
accuracy = accuracy_score(y_test, y_pred)
print('Accuracy:', accuracy*100)
```

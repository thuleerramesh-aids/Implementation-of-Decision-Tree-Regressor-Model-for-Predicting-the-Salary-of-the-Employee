# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
**Step 1:** Import required libraries and load the salary dataset.

**Step 2:** Separate input and output data, then preprocess categorical values.

**Step 3:** Train the Decision Tree Regressor model using the dataset.

**Step 4:** Predict salary values, evaluate the model, and visualize the decision tree.

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Thuleer R
RegisterNumber: 212225230285

import pandas as pd
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.tree import DecisionTreeRegressor, plot_tree
from sklearn.metrics import accuracy_score, classification_report
data = pd.read_csv("Salary.csv")
X = data.drop("Salary", axis=1)
y = data["Salary"]
X = pd.get_dummies(X, drop_first=True)
X_train, X_test, y_train, y_test = train_test_split(    X, y, test_size=0.2, random_state=42)
model = DecisionTreeRegressor(random_state=42)
model.fit(X, y)
y_pred = model.predict(X)
print("\nAccuracy:", accuracy_score(y, y_pred)*100)
print("\nClassification Report:")
print(classification_report(y, y_pred))
plt.figure(figsize=(25,12))
plot_tree(
    model,
    feature_names=X.columns,
    filled=True
)
plt.title("Decision Tree Regressor")
plt.show()
*/
```

## Output:
<img width="307" height="161" alt="Screenshot 2026-05-13 110704" src="https://github.com/user-attachments/assets/9660e10c-604b-42f6-90cc-1c1315cda700" />
<img width="206" height="137" alt="Screenshot 2026-05-13 110708" src="https://github.com/user-attachments/assets/eacc7bee-97d5-4830-ac13-02a23b01b1e2" />

<img width="392" height="190" alt="Screenshot 2026-05-13 110719" src="https://github.com/user-attachments/assets/8806110f-8f22-4ac1-92c6-c70b1a39764a" />



## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.

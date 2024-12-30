# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1: Load and Explore Data
Load the dataset (car.csv) into a Pandas DataFrame and preview its structure using info(), head(), and tail().

### Step2: Prepare Features and Target
Define Weight and Volume as features (x) and CO2 as the target (y).



### Step3: Train the Model
Use LinearRegression from sklearn to train a model with x and y using fit().



### Step4: Extract Model Parameters
Retrieve and print the model's coefficients (coef_) and intercept (intercept_).



### Step5: Predict CO2
Predict the CO2 emission for a specific Weight and Volume using predict() and display the result.








## Program:
    import pandas as pd
    from sklearn import linear_model
    df=pd.read_csv("car.csv")
    df.info()
    df.head()
    df.tail()
    x=df[['Weight', 'Volume']]
    y=df['CO2']
    regr=linear_model.LinearRegression()
    regr.fit(x,y)
    print('Coeffients:',regr.coef_)
    print('Intercept:',regr.intercept_)
    predictedCO2=regr.predict([[3300,1300]])
    print('Predicted CO2 for the corresponding weight and volume', predictedCO2)


## Output:
![alt text](<Screenshot 2024-12-30 214435.png>)


## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
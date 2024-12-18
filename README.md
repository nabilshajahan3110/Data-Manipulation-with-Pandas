# Data-Manipulation-with-Pandas
As part of a 75-day data analysis challenge, this work on Jupyter covers data manipulation with Pandas

import numpy as np

# Create a numpy array containing the numbers from 1 to 10, and then reshape it to a 2x5 matrix.

a1 = np.arange (1,11).reshape(2,5)
print(a1)
print(a1.shape)
print(a1.ndim)

# Create a numpy array containing the numbers from 1 to 20, and then extract the elements between the 5th and 15th index.

a2 = np.arange (1,21)
print(a2)
print(a2[5:15])

# Create a Pandas series with the following data: {'apples': 3, 'bananas': 2, 'oranges': 1}. 
# Then, add a new item to the series with the key 'pears' and the value 4.

import pandas as pd
fruit = pd.Series ({'apples': 3, 'bananas': 2, 'oranges': 1})
print(fruit)
fruit["pears"] = 4
print(fruit)

# Create a dataframe with the following columns: name, age, and gender. The dataframe should have 10 rows of data.

df = pd.DataFrame({
    'name': ['Alice', 'Bob', 'Charlie', 'David', 'Eve', 
             'Frank', 'Grace', 'Hannah', 'Ian', 'Jane'],
    'age': [25, 30, 22, 35, 28, 40, 33, 27, 29, 31],
    'gender': ['Female', 'Male', 'Male', 'Male', 'Female', 
               'Male', 'Female', 'Female', 'Male', 'Female']
})
df

# Add a new column to the data frame created in question 1, called occupation. 
# The values for this column should be Programmer, Manager, and Analyst, corresponding to the rows in the dataframe.

df['occupation'] = ['Programmer', 'Manager', 'Analyst', 'Manager', 'Programmer', 'Analyst', 'Manager', 'Analyst', 'Programmer', 'Analyst']
df

# Select the rows of the dataframe where the age is greater than or equal to 30.

age_condition = df[df['age'] >= 30]
print(age_condition)

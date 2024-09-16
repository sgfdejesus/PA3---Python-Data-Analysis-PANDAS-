# PA3 - Python Data Analysis (PANDAS)
"This repository contains Python code to solve two programming problems titled: **Problem 1** and **Problem 2**. Each problem involves the use of PANDAS for data analysis."

Below is a preview of the code, but there is also a Jupyter notebook uploaded in the files section.

---

## Problem 1:
### Overview
This problem involves analyzing a dataset contained in a .csv file. The process includes:
- Loading the .csv file into a pandas DataFrame named `cars`
- Displaying both the first five and last five rows of the DataFrame

### Code Implementation
``` python
import pandas as pd

#Load the 'cars.csv' file into a DataFrame named 'cars'
cars = pd.read_csv('cars.csv')

#Display the concatenated first 5 rows (head) and last 5 rows (tail) of the DataFrame
#'cars.head()' returns the first five rows and cars.tail() returns the last 5 rows
pd.concat([cars.head(), cars.tail()])
```

### Input and Output Example
- **Input:** A .csv file named `cars.csv`.
- **Output:** The first five and last five rows of the `cars` DataFrame.

<img width="606" alt="Screenshot 2024-09-17 at 12 05 00 AM" src="https://github.com/user-attachments/assets/d9e6914b-3690-4b27-b52e-5e5f6d81c1f8">


---

## Problem 2:
### Overview
This task involves data extraction from a pandas DataFrame using subsetting, slicing, and indexing techniques. The operations include:
- Displaying the first five rows with odd-numbered columns.
- Extracting the row with the car model ‘Mazda RX4’.
- Determining the number of cylinders in the car model ‘Camaro Z28’.
- Displaying the cylinders and gear type for the car models ‘Mazda RX4 Wag’, ‘Ford Pantera L’, and ‘Honda Civic’.

### Code Implementation
``` python
import pandas as pd

#Load the 'cars.csv' file into a DataFrame named 'cars'
cars = pd.read_csv('cars.csv')

#a. Display the first five rows with odd-numbered columns (1, 3, 5, 7...)
#Select the first 5 rows and every second column starting from index 1
print("First five rows with odd-numbered columns:")
print(cars.iloc[:5, 1::2])

#b. Display the row that contains the ‘Model’ of ‘Mazda RX4’
#Filter the DataFrame to include only the row where the 'Model' column matches 'Mazda RX4'
print("\nRow with Model 'Mazda RX4':")
print(cars[cars['Model'] == 'Mazda RX4'])

#c. How many cylinders (‘cyl’) does the car model ‘Camaro Z28’ have?
#Use .loc to filter the row where 'Model' is 'Camaro Z28' and select the 'cyl' column
#Since the result is a Series, use .iloc[0] to get the scalar value for the cylinders
print(f"\nCylinders in 'Camaro Z28':")
print(f"{cars.loc[cars['Model'] == 'Camaro Z28', 'cyl'].iloc[0]} cylinders")

#d. Determine how many cylinders (‘cyl’) and what gear type (‘gear’) the car models ‘Mazda RX4 Wag’, ‘Ford Pantera L’, and ‘Honda Civic’ have
#Use .isin() to filter rows where the 'Model' matches any of the specified models
#Select the 'Model', 'cyl', and 'gear' columns to display
print("\nCylinders and gear type for selected models:")
models = ['Mazda RX4 Wag', 'Ford Pantera L', 'Honda Civic']
print(cars[cars['Model'].isin(models)][['Model', 'cyl', 'gear']])
```

### Input and Output Example
- **Input:** A .csv file named `cars.csv`.
- **Output:**
  - The first five rows with odd-numbered columns of the `cars` DataFrame.
  - The row with the 'Model' of 'Mazda RX4'.
  - The number of cylinders in the car model 'Camaro Z28'.
  - The number of cylinders and gear type for the car models 'Mazda RX4 Wag', 'Ford Pantera L', and 'Honda Civic'.

<img width="596" alt="Screenshot 2024-09-17 at 12 05 22 AM" src="https://github.com/user-attachments/assets/8e88f651-d208-499b-9d26-aafca4b83901">








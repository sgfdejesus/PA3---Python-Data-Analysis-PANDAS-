# PA3 Python Data Analysis (PANDAS)
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

---

## Problem 2:
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







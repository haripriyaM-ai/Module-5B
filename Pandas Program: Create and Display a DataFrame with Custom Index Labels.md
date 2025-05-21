# EXP 24: Pandas Program: Create and Display a DataFrame with Custom Index Labels

##  Aim

To create and display a **DataFrame** using the **Pandas** library in Python from a given dictionary, and apply specific index labels to the rows.


##  Algorithm

1. **Import Libraries**: Import the required libraries – `pandas` and `numpy`.
2. **Create Dictionary**: Define a dictionary `exam_data` with keys: `'name'`, `'score'`, `'attempts'`, and `'qualify'`.
3. **Index Labels**: Create a list of custom index labels called `labels`.
4. **Create DataFrame**: Use `pd.DataFrame()` to create the DataFrame by passing the dictionary and index labels.
5. **Display Output**: Display the DataFrame using `print()` or by simply calling the DataFrame variable.


##  Program
```
import pandas as pd
import numpy as np

exam_data = {
    'name': ['Annie', 'Beth', 'Charles', 'David', 'Ella'],
    'score': [12.5, 9, 16.5, np.nan, 9],
    'attempts': [1, 3, 2, 3, 2],
    'qualify': ['yes', 'no', 'yes', 'no', 'no']
}

labels = ['a', 'b', 'c', 'd', 'e']

df = pd.DataFrame(exam_data, index=labels)

print(df)
```

## Output
![image](https://github.com/user-attachments/assets/7486bc88-cb8d-4580-8809-497344b9efe0)

## Result
Thus, the program is verified successfully.

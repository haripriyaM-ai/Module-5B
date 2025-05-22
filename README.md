## MODULE - 5B
# EXP 21: NumPy Program: Column-wise Sorting of a 2D Array

##  Aim
To write a **NumPy** program that sorts the elements in each column of a given 2D array in ascending order.

##  Algorithm

1. **Import NumPy**: Start by importing the NumPy library.
2. **Get Input**: Accept a 2D NumPy array from the user.
3. **Sort Column-wise**: Use the `np.sort()` function with `axis=0` to sort each column in ascending order.
4. **Store Result**: Store the sorted result in a new array.
5. **Display Output**: Print the original array and the column-wise sorted array.

## 🧾 Program
```
import numpy as np

rows = int(input())
cols = int(input())

elements = []
for i in range(rows):
    row = list(map(int, input().split()))
    elements.append(row)

arr = np.array(elements)
print("\nOriginal Array:")
print(arr)

sorted_arr = np.sort(arr, axis=0)
print("Column-wise Sorted Array:")
print(sorted_arr)
```
## Output
![image](https://github.com/user-attachments/assets/3ed53a27-8bac-4d9b-abb4-3f9e6a79387d)

## Result
Thus, the program is verified successfully.

---

# EXP 22: NumPy Program: Find Indices Where Elements in Array x are Greater Than or Equal to Corresponding Elements in Array y

##  Aim
To write a Python program using **NumPy** that finds the indices where elements in array `x` are greater than or equal to their corresponding elements in array `y`.

##  Algorithm
1. **Import NumPy**: Import the NumPy library.
2. **Define Arrays**: Define two NumPy arrays, `x` and `y`, with the same shape (i.e., same number of elements).
3. **Use Boolean Indexing**: 
   - `x > y` gives a boolean array where elements of `x` are greater than `y`.
   - `x == y` gives a boolean array where elements of `x` are equal to `y`.
4. **Find Indices**: Use `np.where()` to get the indices where the conditions `x >= y` are satisfied.
5. **Print Indices**: Print the indices where the condition holds true.

##  Program

```
import numpy as np

x = np.array([5, 2, 7, 1, 9])
y = np.array([3, 2, 6, 4, 9])

greater_equal_indices = np.where(x >= y)

print("Indices where x >= y:", greater_equal_indices[0])
```

## Output
![image](https://github.com/user-attachments/assets/c96d0442-0fa7-465f-a540-919ba6a85b5c)

## Result
Thus, the program is verified successfully.

---

#   EXP 23: NumPy Program: Replace the Second Column in a 2D Array

##  Aim
To write a **NumPy** program that deletes the second column from a given 2D array and inserts a new column at the same position.

##  Algorithm
1. **Import NumPy**: Start by importing the NumPy library.
2. **Get Input**: Get a 2D NumPy array and a new column (as another array) from the user.
3. **Delete Column**: Use `np.delete()` to remove the second column (index 1) from the original array.
4. **Insert Column**: Use `np.insert()` to insert the new column at the second column's original position.
5. **Display Result**: Print the updated array with the replaced column.

##  Program

```
import numpy as np

original_array = np.array([[1, 2, 3],
                           [4, 5, 6],
                           [7, 8, 9]])

new_column = np.array([10, 11, 12])  # Must match number of rows

modified_array = np.delete(original_array, 1, axis=1)

updated_array = np.insert(modified_array, 1, new_column, axis=1)

# Step 5: Display updated array
print("Updated array:\n", updated_array)
```
## Output
![image](https://github.com/user-attachments/assets/7fbb1ee9-ce11-4f12-a697-92fbf09872be)

## Result
Thus, the program is verified successfully.

---

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

---

# EXP 25: Pandas Program: Join Two DataFrames Along Rows

##  AIM

To write a Python program using Pandas to **join two DataFrames along rows** (row-wise concatenation) and assign all data to a new DataFrame.


##  ALGORITHM

1. **Import Libraries**: Import the `pandas` library.
2. **Create First DataFrame**: Use a dictionary to create `student_data1`.
3. **Create Second DataFrame**: Use another dictionary to create `student_data2`.
4. **Concatenate DataFrames**: Use `pd.concat()` with `axis=0` to concatenate both DataFrames row-wise.
5. **Display Result**: Print the new combined DataFrame.


##  Program

```
import pandas as pd

student_data1 = {
    'student_id': ['S1', 'S2', 'S3', 'S4'],
    'name': ['Alice', 'Bob', 'Charlie', 'David'],
    'marks': [85, 90, 78, 92]
}
df1 = pd.DataFrame(student_data1)

student_data2 = {
    'student_id': ['S5', 'S6', 'S7', 'S8'],
    'name': ['Eve', 'Frank', 'Grace', 'Hannah'],
    'marks': [88, 76, 95, 89]
}
df2 = pd.DataFrame(student_data2)
combined_df = pd.concat([df1, df2], axis=0)
print(combined_df)
```
## Output
![image](https://github.com/user-attachments/assets/97265fe9-336c-45f8-ac7a-811e374d0590)

## Result
Thus, the program is verified successfully.

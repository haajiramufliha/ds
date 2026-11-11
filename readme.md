# Foundation of Data Science Lab – Complete Practical Answers

## 1(a) NumPy – Null Vector and Update Sixth Value

### Question
Write a NumPy program to create a null vector of size 10 and update sixth value to 11.

### Aim
To create a null vector of size 10 and update its sixth value to 11.

### Algorithm
1. Import NumPy.
2. Create a vector containing 10 zeros using `np.zeros()`.
3. Access the sixth element using index `5`.
4. Assign the value `11`.
5. Display the vector.

### Program
```python
import numpy as np

a = np.zeros(10)
a[5] = 11

print(a)
```

### Output
```text
[ 0.  0.  0.  0.  0. 11.  0.  0.  0.  0.]
```

### Result
Thus, a null vector of size 10 was created and its sixth value was updated to 11.

---

## 1(b) NumPy – Convert Array to Float Type

### Question
Write a NumPy program to convert an array to a float type.

### Aim
To convert an integer NumPy array into a floating-point array.

### Algorithm
1. Import NumPy.
2. Create an integer array.
3. Use `astype(float)` to convert the array.
4. Display the converted array.

### Program
```python
import numpy as np

a = np.array([1, 2, 3, 4, 5])
b = a.astype(float)

print(b)
```

### Output
```text
[1. 2. 3. 4. 5.]
```

### Result
Thus, the integer array was successfully converted into a float array.

---

## 1(c) NumPy – 3×3 Matrix

### Question
Write a NumPy program to create a 3×3 matrix with values ranging from 2 to 10.

### Aim
To create a 3×3 matrix containing values from 2 to 10.

### Algorithm
1. Import NumPy.
2. Generate values from 2 to 10 using `np.arange()`.
3. Reshape the values into a 3×3 matrix.
4. Display the matrix.

### Program
```python
import numpy as np

a = np.arange(2, 11).reshape(3, 3)

print(a)
```

### Output
```text
[[ 2  3  4]
 [ 5  6  7]
 [ 8  9 10]]
```

### Result
Thus, a 3×3 matrix containing values from 2 to 10 was created successfully.

---

## 1(d) NumPy – List to One-Dimensional Array

### Question
Write a NumPy program to convert a list of numeric values into a one-dimensional NumPy array.

### Aim
To convert a Python list into a one-dimensional NumPy array.

### Algorithm
1. Import NumPy.
2. Create a numeric list.
3. Convert the list using `np.array()`.
4. Display the array.

### Program
```python
import numpy as np

lst = [10, 20, 30, 40, 50]
a = np.array(lst)

print(a)
```

### Output
```text
[10 20 30 40 50]
```

### Result
Thus, the list was successfully converted into a one-dimensional NumPy array.

---

# 2(a) NumPy – Convert Array to Float Type

### Question
Write a NumPy program to convert an array to a float type.

### Aim
To convert an integer array into a floating-point array.

### Algorithm
1. Import NumPy.
2. Create an integer array.
3. Use `astype(float)`.
4. Display the converted array.

### Program
```python
import numpy as np

a = np.array([10, 20, 30])
b = a.astype(float)

print(b)
```

### Output
```text
[10. 20. 30.]
```

### Result
Thus, the array was successfully converted to float type.

---

# 2(b) NumPy – Empty and Full Array

### Question
Write a NumPy program to create an empty and a full array.

### Aim
To create an empty array and an array filled with a specified value.

### Algorithm
1. Import NumPy.
2. Create an empty array using `np.empty()`.
3. Create a full array using `np.full()`.
4. Display both arrays.

### Program
```python
import numpy as np

empty_array = np.empty((2, 3))
full_array = np.full((2, 3), 5)

print("Empty Array:")
print(empty_array)

print("Full Array:")
print(full_array)
```

### Output
```text
Empty Array:
[[0. 0. 0.]
 [0. 0. 0.]]

Full Array:
[[5 5 5]
 [5 5 5]]
```

> **Note:** `np.empty()` does not initialize values to zero. The displayed values can vary depending on memory contents.

### Result
Thus, an empty array and a full array were successfully created.

---

# 2(c) NumPy – List and Tuple to Arrays

### Question
Write a NumPy program to convert a list and tuple into arrays.

### Aim
To convert a Python list and tuple into NumPy arrays.

### Algorithm
1. Import NumPy.
2. Create a list and tuple.
3. Convert them using `np.array()`.
4. Display the arrays.

### Program
```python
import numpy as np

lst = [1, 2, 3, 4]
tup = (5, 6, 7, 8)

a = np.array(lst)
b = np.array(tup)

print("Array from List:", a)
print("Array from Tuple:", b)
```

### Output
```text
Array from List: [1 2 3 4]
Array from Tuple: [5 6 7 8]
```

### Result
Thus, the list and tuple were successfully converted into NumPy arrays.

---

# 2(d) NumPy – Real and Imaginary Parts

### Question
Write a NumPy program to find the real and imaginary parts of an array of complex numbers.

### Aim
To find the real and imaginary parts of an array containing complex numbers.

### Algorithm
1. Import NumPy.
2. Create an array of complex numbers.
3. Use `np.real()` to obtain the real parts.
4. Use `np.imag()` to obtain the imaginary parts.
5. Display the results.

### Program
```python
import numpy as np

a = np.array([2+3j, 4+5j, 6+7j])

print("Real Part:", np.real(a))
print("Imaginary Part:", np.imag(a))
```

### Output
```text
Real Part: [2. 4. 6.]
Imaginary Part: [3. 5. 7.]
```

### Result
Thus, the real and imaginary parts of the complex array were obtained successfully.

---

# 3. Pandas – Element-wise Power

### Question
Write a Pandas program to get the powers of an array values element-wise.

**Note:** First array elements are raised to powers from the second array.

**Sample data:**
```python
{'X':[78,85,96,80,86],
 'Y':[84,94,89,83,86],
 'Z':[86,97,96,72,83]}
```

### Aim
To calculate element-wise powers of two arrays using Pandas.

### Algorithm
1. Import Pandas.
2. Create the given DataFrame.
3. Select the `X` and `Y` columns.
4. Raise each element of `X` to the corresponding element of `Y`.
5. Display the result.

### Program
```python
import pandas as pd

data = {
    'X': [78, 85, 96, 80, 86],
    'Y': [84, 94, 89, 83, 86],
    'Z': [86, 97, 96, 72, 83]
}

df = pd.DataFrame(data)

result = df['X'] ** df['Y']

print(result)
```

### Output
```text
0    78^84
1    85^94
2    96^89
3    80^83
4    86^86
dtype: object
```

The actual Python output will contain the corresponding very large integer values.

### Result
Thus, the elements of the first array were raised to the corresponding powers of the second array successfully.

---

# 4. Pandas – Select Specified Rows and Columns

### Question
Write a Pandas program to select the specified columns and rows from a given DataFrame.

Select `name` and `score` columns in rows 1, 3, 5, 6 from the following DataFrame.

### Aim
To select specified rows and columns from a Pandas DataFrame.

### Algorithm
1. Import Pandas and NumPy.
2. Create the given dictionary.
3. Create the DataFrame using the given labels.
4. Select rows 1, 3, 5 and 6 using `iloc`.
5. Select the `name` and `score` columns.
6. Display the result.

### Program
```python
import pandas as pd
import numpy as np

exam_data = {
    'name': ['Anastasia', 'Dima', 'Katherine', 'James', 'Emily',
             'Michael', 'Matthew', 'Laura', 'Kevin', 'Jonas'],
    'score': [12.5, 9, 16.5, np.nan, 9, 20, 14.5, np.nan, 8, 19],
    'attempts': [1, 3, 2, 3, 2, 3, 1, 1, 2, 1],
    'qualify': ['yes', 'no', 'yes', 'no', 'no',
                'yes', 'yes', 'no', 'no', 'yes']
}

labels = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j']

df = pd.DataFrame(exam_data, index=labels)

print(df.iloc[[1, 3, 5, 6]][['name', 'score']])
```

### Output
```text
       name  score
b      Dima    9.0
d     James    NaN
f   Michael   20.0
g   Matthew   14.5
```

### Result
Thus, the specified rows and columns were successfully selected from the DataFrame.

---

# 5. Pandas – Count Rows and Columns

### Question
Write a Pandas program to count the number of rows and columns of a DataFrame.

### Aim
To find the number of rows and columns in a Pandas DataFrame.

### Algorithm
1. Import Pandas and NumPy.
2. Create the given DataFrame.
3. Use `shape` to obtain the dimensions.
4. Display the number of rows and columns.

### Program
```python
import pandas as pd
import numpy as np

exam_data = {
    'name': ['Anastasia', 'Dima', 'Katherine', 'James', 'Emily',
             'Michael', 'Matthew', 'Laura', 'Kevin', 'Jonas'],
    'score': [12.5, 9, 16.5, np.nan, 9, 20, 14.5, np.nan, 8, 19],
    'attempts': [1, 3, 2, 3, 2, 3, 1, 1, 2, 1],
    'qualify': ['yes', 'no', 'yes', 'no', 'no',
                'yes', 'yes', 'no', 'no', 'yes']
}

labels = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j']

df = pd.DataFrame(exam_data, index=labels)

rows, columns = df.shape

print("Number of rows:", rows)
print("Number of columns:", columns)
```

### Output
```text
Number of rows: 10
Number of columns: 4
```

### Result
Thus, the DataFrame contains 10 rows and 4 columns.

---

# 6. Pima Indians Diabetes Dataset – Univariate Analysis

### Question
Use the Pima Indians Diabetes dataset for performing univariate analysis:

- Frequency
- Mean
- Median
- Mode
- Variance
- Standard Deviation
- Skewness
- Kurtosis

### Aim
To perform univariate statistical analysis on the Pima Indians Diabetes dataset.

### Algorithm
1. Import Pandas.
2. Load the `diabetes.csv` dataset.
3. Select a numerical variable such as `Glucose`.
4. Calculate its frequency.
5. Calculate mean, median and mode.
6. Calculate variance and standard deviation.
7. Calculate skewness and kurtosis.
8. Display all results.

### Program
```python
import pandas as pd

url = "https://raw.githubusercontent.com/npradaschnor/Pima-Indians-Diabetes-Dataset/master/diabetes.csv"

df = pd.read_csv(url)
x = df["Glucose"]

print("Frequency:")
print(x.value_counts().head())

print("Mean:", x.mean())
print("Median:", x.median())
print("Mode:", x.mode()[0])
print("Variance:", x.var())
print("Standard Deviation:", x.std())
print("Skewness:", x.skew())
print("Kurtosis:", x.kurt())
```

### Output
```text
Frequency:
99     ...
100    ...
102    ...
...

Mean: 120.89
Median: 117.0
Mode: 99
Variance: ...
Standard Deviation: ...
Skewness: ...
Kurtosis: ...
```

### Result
Thus, frequency, mean, median, mode, variance, standard deviation, skewness and kurtosis were successfully calculated.

---

# 7. Pima Indians Diabetes Dataset – Linear and Logistic Regression

### Question
Use the Pima Indians Diabetes dataset for performing bivariate analysis:

- Linear regression modeling
- Logistic regression modeling

### Aim
To perform linear and logistic regression analysis using the Pima Indians Diabetes dataset.

### Algorithm
1. Import Pandas and regression libraries.
2. Load the diabetes dataset.
3. Select `Glucose` as the independent variable.
4. Select `Outcome` as the dependent variable.
5. Fit a linear regression model.
6. Fit a logistic regression model.
7. Display coefficients and prediction.

### Program
```python
import pandas as pd
from sklearn.linear_model import LinearRegression, LogisticRegression

df = pd.read_csv("diabetes.csv")

X = df[['Glucose']]
y = df['Outcome']

# Linear Regression
linear_model = LinearRegression()
linear_model.fit(X, y)

print("Linear Regression Coefficient:",
      linear_model.coef_[0])

# Logistic Regression
logistic_model = LogisticRegression()
logistic_model.fit(X, y)

print("Logistic Regression Coefficient:",
      logistic_model.coef_[0][0])

print("Prediction for Glucose = 120:",
      logistic_model.predict([[120]])[0])
```

### Output
```text
Linear Regression Coefficient: ...
Logistic Regression Coefficient: ...
Prediction for Glucose = 120: 0
```

### Result
Thus, linear and logistic regression models were successfully applied to the diabetes dataset.

---

# 8. Pima Indians Diabetes Dataset – Multiple Regression

### Question
Use the Pima Indians Diabetes dataset for performing bivariate analysis:

- Multiple Regression analysis

### Aim
To perform multiple regression analysis using several independent variables from the diabetes dataset.

### Algorithm
1. Import Pandas and `LinearRegression`.
2. Load the diabetes dataset.
3. Select multiple independent variables.
4. Select `Outcome` as the dependent variable.
5. Create the regression model.
6. Train the model.
7. Display coefficients, intercept and predictions.

### Program
```python
import pandas as pd
from sklearn.linear_model import LinearRegression

df = pd.read_csv("diabetes.csv")

X = df[['Pregnancies', 'Glucose', 'BloodPressure',
        'BMI', 'Age']]

y = df['Outcome']

model = LinearRegression()
model.fit(X, y)

print("Coefficients:")
print(model.coef_)

print("Intercept:", model.intercept_)

print("Prediction:")
print(model.predict(X.head()))
```

### Output
```text
Coefficients:
[... ... ... ... ...]

Intercept: ...

Prediction:
[... ... ... ... ...]
```

### Result
Thus, multiple regression analysis was successfully performed using multiple variables.

---

# 9. UCI Dataset – Normal Values, Density/Contour and 3D Plotting

### Question
Apply and explore various plotting functions on UCI data set for performing:

a) Normal values  
b) Density and contour plots  
c) Three-dimensional plotting

### Aim
To visualize the UCI dataset using normal, density, contour and 3D plots.

### Algorithm
1. Import Pandas, NumPy and Matplotlib.
2. Load the UCI dataset.
3. Plot normal values using a line plot.
4. Create a density plot.
5. Create a contour plot.
6. Create a 3D scatter plot.
7. Display the plots.

### Program
```python
import pandas as pd
import matplotlib.pyplot as plt
import numpy as np

df = pd.read_csv("uci.csv")

# Normal values
plt.plot(df.iloc[:, 0])
plt.title("Normal Values")
plt.show()

# Density plot
df.iloc[:, 0].plot(kind='density')
plt.title("Density Plot")
plt.show()

# Contour plot
x = df.iloc[:, 0].values[:50]
y = df.iloc[:, 1].values[:50]

X, Y = np.meshgrid(x, y)
Z = X + Y

plt.contour(X, Y, Z)
plt.title("Contour Plot")
plt.show()

# 3D plot
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')

ax.scatter(df.iloc[:, 0],
           df.iloc[:, 1],
           df.iloc[:, 2])

ax.set_title("3D Plot")
plt.show()
```

### Output
```text
Normal Values Plot

Density Plot

Contour Plot

3D Scatter Plot
```

### Result
Thus, normal values, density, contour and three-dimensional plots were successfully created.

---

# 10. UCI Dataset – Correlation, Scatter, Histogram and 3D Plotting

### Question
Apply and explore various plotting functions on UCI data set for performing:

a) Correlation and scatter plots  
b) Histograms  
c) Three-dimensional plotting

### Aim
To visualize relationships and distributions in the UCI dataset.

### Algorithm
1. Import Pandas and Matplotlib.
2. Load the UCI dataset.
3. Calculate the correlation matrix.
4. Create a scatter plot.
5. Create a histogram.
6. Create a 3D scatter plot.
7. Display the results.

### Program
```python
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv("uci.csv")

# Correlation
print(df.corr(numeric_only=True))

# Scatter plot
plt.scatter(df.iloc[:, 0], df.iloc[:, 1])
plt.xlabel("Column 1")
plt.ylabel("Column 2")
plt.title("Scatter Plot")
plt.show()

# Histogram
df.iloc[:, 0].hist()
plt.title("Histogram")
plt.show()

# 3D Plot
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')

ax.scatter(df.iloc[:, 0],
           df.iloc[:, 1],
           df.iloc[:, 2])

ax.set_title("3D Plot")
plt.show()
```

### Output
```text
Correlation Matrix

Scatter Plot

Histogram

3D Scatter Plot
```

### Result
Thus, correlation, scatter, histogram and 3D plots were successfully generated.

---

# 11. Pima Indians Diabetes Dataset – Normal Values, Density/Contour and 3D Plotting

### Question
Apply and explore various plotting functions on Pima Indians Diabetes data set for performing:

a) Normal values  
b) Density and contour plots  
c) Three-dimensional plotting

### Aim
To visualize the Pima Indians Diabetes dataset using different plotting techniques.

### Algorithm
1. Import Pandas, NumPy and Matplotlib.
2. Load the diabetes dataset.
3. Plot normal values of the `Glucose` variable.
4. Create a density plot.
5. Create a contour plot using `Glucose` and `BMI`.
6. Create a 3D scatter plot using `Glucose`, `BMI` and `Age`.
7. Display the plots.

### Program
```python
import pandas as pd
import matplotlib.pyplot as plt
import numpy as np

df = pd.read_csv("diabetes.csv")

# Normal values
plt.plot(df["Glucose"])
plt.title("Normal Glucose Values")
plt.show()

# Density plot
df["Glucose"].plot(kind="density")
plt.title("Glucose Density")
plt.show()

# Contour plot
x = df["Glucose"].values[:50]
y = df["BMI"].values[:50]

X, Y = np.meshgrid(x, y)
Z = X + Y

plt.contour(X, Y, Z)
plt.title("Contour Plot")
plt.show()

# 3D plot
fig = plt.figure()
ax = fig.add_subplot(111, projection="3d")

ax.scatter(df["Glucose"],
           df["BMI"],
           df["Age"])

ax.set_xlabel("Glucose")
ax.set_ylabel("BMI")
ax.set_zlabel("Age")

plt.show()
```

### Output
```text
Normal Glucose Values Plot

Glucose Density Plot

Contour Plot

3D Scatter Plot
```

### Result
Thus, normal values, density, contour and 3D plots were successfully created for the diabetes dataset.

---

# 12. Pima Indians Diabetes Dataset – Correlation, Scatter, Histogram and 3D

### Question
Apply and explore various plotting functions on Pima Indians Diabetes data set for performing:

a) Correlation and scatter plots  
b) Histograms  
c) Three-dimensional plotting

### Aim
To study the relationship and distribution of variables in the Pima Indians Diabetes dataset.

### Algorithm
1. Import Pandas and Matplotlib.
2. Load the diabetes dataset.
3. Calculate the correlation matrix.
4. Create a scatter plot between `Glucose` and `BMI`.
5. Create a histogram of `Glucose`.
6. Create a 3D plot using `Glucose`, `BMI` and `Age`.
7. Display the results.

### Program
```python
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv("diabetes.csv")

# Correlation
print(df.corr(numeric_only=True))

# Scatter plot
plt.scatter(df["Glucose"], df["BMI"])
plt.xlabel("Glucose")
plt.ylabel("BMI")
plt.title("Glucose vs BMI")
plt.show()

# Histogram
df["Glucose"].hist()
plt.title("Glucose Histogram")
plt.xlabel("Glucose")
plt.ylabel("Frequency")
plt.show()

# 3D Plot
fig = plt.figure()
ax = fig.add_subplot(111, projection="3d")

ax.scatter(df["Glucose"],
           df["BMI"],
           df["Age"])

ax.set_xlabel("Glucose")
ax.set_ylabel("BMI")
ax.set_zlabel("Age")

plt.show()
```

### Output
```text
Correlation Matrix

Glucose vs BMI Scatter Plot

Glucose Histogram

3D Scatter Plot
```

### Result
Thus, correlation, scatter, histogram and 3D plots were successfully generated.

---

# 13. Pandas – Count Number of Columns

### Question
Write a Pandas program to count the number of columns of a DataFrame.

### Aim
To find the number of columns in a Pandas DataFrame.

### Algorithm
1. Import Pandas.
2. Create a DataFrame.
3. Use `shape[1]` to obtain the number of columns.
4. Display the result.

### Program
```python
import pandas as pd

data = {
    'Name': ['A', 'B', 'C'],
    'Age': [20, 21, 22],
    'Mark': [80, 90, 85]
}

df = pd.DataFrame(data)

print("Number of columns:", df.shape[1])
```

### Output
```text
Number of columns: 3
```

### Result
Thus, the number of columns in the DataFrame was successfully calculated.

---

# 14. NumPy – Number of Occurrences of a Sequence

### Question
Create a 2-dimensional array of size 2 × 3, composed of 4-byte integer elements. Write a NumPy program to find the number of occurrences of a sequence in the said array.

### Aim
To create a 2×3 array with 4-byte integer elements and find the number of occurrences of a given sequence.

### Algorithm
1. Import NumPy.
2. Create a 2×3 array using `dtype=np.int32`.
3. Define the sequence to be searched.
4. Traverse each row.
5. Compare consecutive elements with the given sequence.
6. Count the matches.
7. Display the count.

### Program
```python
import numpy as np

a = np.array([[1, 2, 3],
              [1, 2, 3]], dtype=np.int32)

sequence = [1, 2]

count = 0

for row in a:
    for i in range(len(row) - len(sequence) + 1):
        if list(row[i:i + len(sequence)]) == sequence:
            count += 1

print("Array:")
print(a)

print("Number of occurrences:", count)
```

### Output
```text
Array:
[[1 2 3]
 [1 2 3]]

Number of occurrences: 2
```

### Result
Thus, the given sequence was successfully searched and its number of occurrences was found.

---

# 15(a). NumPy – Merge Three Arrays

### Question
Write a NumPy program to merge three given NumPy arrays of the same shape.

### Aim
To merge three NumPy arrays having the same shape.

### Algorithm
1. Import NumPy.
2. Create three arrays of the same shape.
3. Use `np.concatenate()` to merge them.
4. Display the merged array.

### Program
```python
import numpy as np

a = np.array([1, 2, 3])
b = np.array([4, 5, 6])
c = np.array([7, 8, 9])

result = np.concatenate((a, b, c))

print("Merged Array:")
print(result)
```

### Output
```text
Merged Array:
[1 2 3 4 5 6 7 8 9]
```

### Result
Thus, the three NumPy arrays were successfully merged.

---

# 15(b). NumPy – Combine Last Element with First Element

### Question
Write a NumPy program to combine last element with first element of two given ndarray with different shapes.

### Aim
To combine the last element of the first array with the first element of the second array.

### Algorithm
1. Import NumPy.
2. Create two arrays with different shapes.
3. Access the last element of the first array using `a[-1]`.
4. Access the first element of the second array using `b[0]`.
5. Create a new array containing both elements.
6. Display the result.

### Program
```python
import numpy as np

a = np.array([1, 2, 3])
b = np.array([4, 5, 6, 7])

result = np.array([a[-1], b[0]])

print("Combined Array:")
print(result)
```

### Output
```text
Combined Array:
[3 4]
```

### Result
Thus, the last element of the first array and the first element of the second array were successfully combined.

---

# Quick Revision – Important Syntax

## NumPy

### Import NumPy
```python
import numpy as np
```

### Create Array
```python
a = np.array([1, 2, 3])
```

### Create Zeros
```python
np.zeros(10)
```

### Create Range
```python
np.arange(2, 11)
```

### Reshape
```python
np.arange(2, 11).reshape(3, 3)
```

### Convert to Float
```python
a.astype(float)
```

### Real Part
```python
np.real(a)
```

### Imaginary Part
```python
np.imag(a)
```

### Merge Arrays
```python
np.concatenate((a, b, c))
```

## Pandas

### Import Pandas
```python
import pandas as pd
```

### Create DataFrame
```python
df = pd.DataFrame(data)
```

### Number of Rows
```python
df.shape[0]
```

### Number of Columns
```python
df.shape[1]
```

### Mean
```python
df["Glucose"].mean()
```

### Median
```python
df["Glucose"].median()
```

### Mode
```python
df["Glucose"].mode()[0]
```

### Variance
```python
df["Glucose"].var()
```

### Standard Deviation
```python
df["Glucose"].std()
```

### Skewness
```python
df["Glucose"].skew()
```

### Kurtosis
```python
df["Glucose"].kurt()
```

### Correlation
```python
df.corr(numeric_only=True)
```

## Matplotlib

### Import
```python
import matplotlib.pyplot as plt
```

### Line Plot
```python
plt.plot(x)
plt.show()
```

### Scatter Plot
```python
plt.scatter(x, y)
plt.show()
```

### Histogram
```python
plt.hist(x)
plt.show()
```

### Density Plot
```python
df["Glucose"].plot(kind="density")
plt.show()
```

### 3D Plot
```python
fig = plt.figure()
ax = fig.add_subplot(111, projection="3d")
ax.scatter(x, y, z)
plt.show()
```

## Regression

### Linear Regression
```python
from sklearn.linear_model import LinearRegression

model = LinearRegression()
model.fit(X, y)
```

### Logistic Regression
```python
from sklearn.linear_model import LogisticRegression

model = LogisticRegression()
model.fit(X, y)
```

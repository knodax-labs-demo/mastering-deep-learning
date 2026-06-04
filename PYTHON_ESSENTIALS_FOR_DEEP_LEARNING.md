# Python Essentials for Deep Learning

Before building neural networks and deep learning models, it is important to understand the Python libraries that form the foundation of most machine learning and AI workflows. This appendix provides a concise introduction to Python programming, NumPy, Matplotlib, and Pandas, which are extensively used throughout the examples in this repository.

---

# Python Basics

Python is one of the most popular programming languages for artificial intelligence, machine learning, and data science. Its simple syntax and extensive ecosystem make it an ideal choice for deep learning development.

## Variables and Data Types

Variables store values that can be used throughout a program.

```python
name = "Deep Learning"
epochs = 10
learning_rate = 0.001
```

Common data types include:

| Data Type | Example |
| --------- | ------- |
| Integer   | 10      |
| Float     | 3.14    |
| String    | "Hello" |
| Boolean   | True    |

## Lists

Lists store multiple values in a single variable.

```python
layers = [64, 128, 256]

print(layers[0])
```

Output:

```text
64
```

## Conditional Statements

Conditional statements allow programs to make decisions.

```python
accuracy = 92

if accuracy > 90:
    print("Excellent Model")
else:
    print("Needs Improvement")
```

## Loops

Loops repeat a block of code.

```python
for epoch in range(5):
    print("Epoch:", epoch)
```

Output:

```text
Epoch: 0
Epoch: 1
Epoch: 2
Epoch: 3
Epoch: 4
```

## Functions

Functions help organize reusable code.

```python
def square(x):
    return x * x

print(square(5))
```

Output:

```text
25
```

---

# NumPy Fundamentals

NumPy is the core numerical computing library in Python. It provides efficient multidimensional arrays and mathematical operations that form the basis of many machine learning frameworks.

## Creating Arrays

```python
import numpy as np

arr = np.array([1, 2, 3, 4, 5])

print(arr)
```

Output:

```text
[1 2 3 4 5]
```

## Multidimensional Arrays

```python
matrix = np.array([
    [1, 2],
    [3, 4]
])

print(matrix)
```

Output:

```text
[[1 2]
 [3 4]]
```

## Array Operations

```python
a = np.array([1, 2, 3])

print(a + 5)
print(a * 2)
```

Output:

```text
[6 7 8]
[2 4 6]
```

## Statistical Functions

```python
data = np.array([10, 20, 30, 40, 50])

print("Mean:", np.mean(data))
print("Max:", np.max(data))
print("Min:", np.min(data))
```

Output:

```text
Mean: 30.0
Max: 50
Min: 10
```

NumPy arrays are conceptually similar to tensors and provide a useful foundation before working with PyTorch tensors.

---

# Matplotlib Visualization

Matplotlib is one of the most widely used visualization libraries in Python. It enables developers to create charts that help understand data distributions, trends, and model performance.

## Creating a Line Plot

```python
import matplotlib.pyplot as plt

epochs = [1, 2, 3, 4, 5]
loss = [0.9, 0.7, 0.5, 0.3, 0.2]

plt.plot(epochs, loss)
plt.xlabel("Epoch")
plt.ylabel("Loss")
plt.title("Training Loss")
plt.show()
```

## Creating a Bar Chart

```python
models = ["CNN", "RNN", "Transformer"]
accuracy = [88, 85, 94]

plt.bar(models, accuracy)
plt.ylabel("Accuracy")
plt.show()
```

## Creating a Histogram

```python
import numpy as np

data = np.random.randn(1000)

plt.hist(data, bins=30)
plt.title("Data Distribution")
plt.show()
```

Visualizations are frequently used during exploratory data analysis and model evaluation.

---

# A.4 Pandas for Data Processing

Pandas is a powerful library for loading, cleaning, transforming, and analyzing structured data.

## Creating a DataFrame

```python
import pandas as pd

data = {
    "Name": ["Alice", "Bob", "Charlie"],
    "Score": [90, 85, 95]
}

df = pd.DataFrame(data)

print(df)
```

Output:

```text
      Name  Score
0    Alice     90
1      Bob     85
2  Charlie     95
```

## Reading a CSV File

```python
df = pd.read_csv("data.csv")

print(df.head())
```

## Selecting Columns

```python
print(df["Score"])
```

## Filtering Rows

```python
high_scores = df[df["Score"] > 90]

print(high_scores)
```

## Descriptive Statistics

```python
print(df.describe())
```

Pandas is commonly used to prepare data before training machine learning and deep learning models.

---

# Summary

Python, NumPy, Matplotlib, and Pandas form the foundation of most modern data science and deep learning workflows. Python provides the programming environment, NumPy enables efficient numerical computation, Matplotlib supports visualization, and Pandas simplifies data processing. Mastering these tools will make it significantly easier to understand and implement the deep learning examples presented throughout this repository.

## Additional Resources

- [Installing Jupyter Notebook](INSTALLING_JUPYTER_NOTEBOOK.md)

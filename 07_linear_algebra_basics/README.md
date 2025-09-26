# 🛠 Linear Algebra in Python

Linear algebra is a **fundamental branch of mathematics** used in programming, data science, and machine learning.
It allows us to **represent and manipulate vectors, matrices, and perform operations like dot product, matrix multiplication, and solving systems of equations**.

---

## 1️⃣ Vectors

A **vector** is an ordered collection of numbers.
In Python, vectors are often represented using **lists** or **NumPy arrays**.

### Example

```python
import numpy as np

v = np.array([1, 2, 3])
print(v)
```

**Output:**

```
[1 2 3]
```

---

## 2️⃣ Vector Operations

### Addition & Subtraction

```python
v1 = np.array([1, 2, 3])
v2 = np.array([4, 5, 6])

print(v1 + v2)  # addition
print(v2 - v1)  # subtraction
```

**Output:**

```
[5 7 9]
[3 3 3]
```

### Scalar Multiplication

```python
v = np.array([1, 2, 3])
print(3 * v)
```

**Output:**

```
[3 6 9]
```

---

## 3️⃣ Dot Product

The **dot product** combines two vectors into a single number.

```python
v1 = np.array([1, 2, 3])
v2 = np.array([4, 5, 6])

dot = np.dot(v1, v2)
print(dot)
```

**Output:**

```
32
```

_(1×4 + 2×5 + 3×6 = 32)_

---

## 4️⃣ Matrices

A **matrix** is a 2D array of numbers.

### Creating a Matrix

```python
A = np.array([[1, 2], [3, 4]])
print(A)
```

**Output:**

```
[[1 2]
 [3 4]]
```

---

## 5️⃣ Matrix Operations

### Addition & Subtraction

```python
B = np.array([[5, 6], [7, 8]])
print(A + B)
print(B - A)
```

**Output:**

```
[[ 6  8]
 [10 12]]
[[4 4]
 [4 4]]
```

### Matrix Multiplication

```python
C = np.dot(A, B)
print(C)
```

**Output:**

```
[[19 22]
 [43 50]]
```

_(Dot product of rows and columns)_

---

## 6️⃣ Transpose of a Matrix

1.The transpose of a matrix flips it over its diagonal.
2.Rows become columns, and columns become rows.

.T is a simple way to transpose a matrix in NumPy.

```python
print(A.T)
```

**Output:**

```
[[1 3]
 [2 4]]
```

---

## 7️⃣ Determinant and Inverse

```python
det = np.linalg.det(A)
inv = np.linalg.inv(A)

print("Determinant:", det)
print("Inverse:\n", inv)
```

**Output:**

```
Determinant: -2.0
Inverse:
 [[-2.   1. ]
  [ 1.5 -0.5]]
```

---

## 8️⃣ Identity and Zero Matrices

```python
I = np.eye(3)    # 3x3 identity matrix
Z = np.zeros((2, 3))  # 2x3 zero matrix

print(I)
print(Z)
```

**Output:**

```
[[1. 0. 0.]
 [0. 1. 0.]
 [0. 0. 1.]]
[[0. 0. 0.]
 [0. 0. 0.]]
```

---

## 9️⃣ Solving Linear Systems

Solve `Ax = b` for `x`.

```python
A = np.array([[3, 1], [1, 2]])
b = np.array([9, 8])

x = np.linalg.solve(A, b)
print(x)
```

**Output:**

```
[2. 3.]
```

_(Solves 3x + y = 9 and x + 2y = 8)_

---

## 🔟 Summary

- **Vectors** → ordered numbers, can add, subtract, scale, dot product.
- **Matrices** → 2D arrays, support addition, subtraction, multiplication.
- **Transpose, determinant, inverse** → key matrix operations.
- **Identity & zero matrices** → special matrices for calculations.
- **Solving linear systems** → `np.linalg.solve()` for equations.

---

This notebook contains **hands-on examples** of linear algebra using **NumPy**.
Run each cell to practice and fully understand **Python linear algebra**. 🚀

# 🔄 Loops in Python

This notebook explains the **concept of loops in Python**.  
Loops allow us to **repeat code** until a certain condition is met, making programs more efficient.

---

## 1️⃣ What is a Loop?

A **loop** is used to **execute a block of code multiple times**.  
Python provides two main types of loops:

1. **`for` loop** → Iterates over a sequence (list, string, tuple, range, etc.).
2. **`while` loop** → Runs as long as a condition is `True`.

---

## 2️⃣ `for` Loop

Used to **iterate over a sequence** (like list, tuple, string, or range).

```python
fruits = ["apple", "banana", "mango"]
for fruit in fruits:
    print(fruit)
```

**Output:**

```
apple
banana
mango
```

### Using `range()` in a for loop

```python
for i in range(5):   # 0 to 4
    print(i)
```

**Output:**

```
0
1
2
3
4
```

---

## 3️⃣ `while` Loop

Runs as long as the condition is `True`.

```python
count = 1
while count <= 5:
    print(count)
    count += 1
```

**Output:**

```
1
2
3
4
5
```

⚠️ Be careful with while loops → if condition never becomes `False`, it will cause an **infinite loop**.

---

## 4️⃣ Loop Control Statements

Python provides keywords to **control loop execution**:

### `break` → Exit the loop immediately

```python
for i in range(10):
    if i == 5:
        break
    print(i)
```

**Output:**

```
0
1
2
3
4
```

---

### `continue` → Skip the current iteration

```python
for i in range(5):
    if i == 2:
        continue
    print(i)
```

**Output:**

```
0
1
3
4
```

---

### `pass` → Do nothing (placeholder)

```python
for i in range(3):
    pass   # future code will go here
```

---

## 5️⃣ Nested Loops

Loops inside another loop.

```python
for i in range(3):
    for j in range(2):
        print(f"i={i}, j={j}")
```

**Output:**

```
i=0, j=0
i=0, j=1
i=1, j=0
i=1, j=1
i=2, j=0
i=2, j=1
```

---

## 6️⃣ Loop with `else`

An **optional `else` block** runs if the loop finishes **without `break`**.

```python
for i in range(5):
    print(i)
else:
    print("Loop finished without break")
```

**Output:**

```
0
1
2
3
4
Loop finished without break
```

If a `break` occurs, the `else` block won’t execute.

---

## 7️⃣ Useful Tricks

### Looping with `enumerate()`

The purpose of enumerate() in Python is to let you loop over a sequence (like a list or string) while also keeping track of the index.

```python
names = ["Arafat", "Rima", "Nusrat"]
for index, name in enumerate(names):
    print(index, name)
```

**Output:**

```
0 Arafat
1 Rima
2 Nusrat
```

---

### Looping with `zip()`

Sometimes we need to **loop over two (or more) lists at the same time**.  
Instead of using indexes, Python’s `zip()` pairs the elements together in a cleaner way.

```python
students = ["Arafat", "Rima", "Nusrat"]
marks = [85, 92, 78]

for student, mark in zip(students, marks):
    print(f"{student} scored {mark}")
```

**Output:**

```
Arafat scored 85
Rima scored 92
Nusrat scored 78
```

---

## 8️⃣ Summary

- **`for` loop** → best for iterating over sequences.
- **`while` loop** → best when condition-based repetition is needed.
- **Control statements**:

  - `break` → exit loop
  - `continue` → skip iteration
  - `pass` → placeholder

- **Nested loops** for working with multiple dimensions.
- **`else` with loops** runs if no `break` happens.
- Use helpers like `enumerate()` and `zip()` for cleaner code.

---

This notebook contains **hands-on examples** of all loop types.
Run each cell to understand how loops work in Python. 🚀

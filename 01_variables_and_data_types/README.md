# Variables & Data Types in Python

This notebook explains the **fundamentals of variables and data types** in Python.  
It is beginner-friendly and includes simple examples for easy understanding.

---

## 1️⃣ What is a Variable?

A **variable** is a named location in memory used to store data.  
You can think of it as a **label for a value**.

```python
x = 10       # x stores the number 10
name = "Arafat"  # name stores the string "Arafat"
```

- `x` → variable name
- `10` → value stored

You can **reassign variables** anytime:

```python
x = 10
x = 20  # x now stores 20
```

---

## 2️⃣ Python Data Types

Python has several built-in **data types**:

| Data Type | Example     | Description                          |
| --------- | ----------- | ------------------------------------ |
| int       | 10          | Integer numbers                      |
| float     | 3.14        | Decimal numbers                      |
| str       | "Hello"     | Text / string                        |
| bool      | True, False | Boolean values (True/False)          |
| list      | \[1,2,3]    | Ordered collection, **mutable**      |
| tuple     | (1,2,3)     | Immutable ordered collection         |
| dict      | {"a":1}     | Key-value pair collection            |
| set       | {1,2,3}     | Unordered collection of unique items |

---

## 3️⃣ Examples of Data Types

### Numbers

```python
x = 10        # int
y = 3.5       # float
print(x, y)
```

**Output:**

```
10 3.5
```

### Strings

```python
name = "Arafat"
greeting = f"Hello, {name}!"
print(greeting)
```

**Output:**

```
Hello, Arafat!
```

### Boolean

```python
is_hungry = True
is_sleepy = False
print(is_hungry, is_sleepy)
```

**Output:**

```
True False
```

### List (Mutable, Ordered)

```python
fruits = ["apple", "banana", "mango"]
fruits.append("orange")  # Add item
fruits[0] = "avocado"    # Modify item
print(fruits)
```

**Output:**

```
['avocado', 'banana', 'mango', 'orange']
```

### Tuple (Immutable, Ordered)

```python
colors = ("red", "green", "blue")
print(colors[1])  # Access second element
# colors[1] = "yellow" -> ❌ Not allowed, immutable
```

**Output:**

```
green
```

### Dictionary (Key-Value Pairs)

```python
person = {"name": "Arafat", "age": 25}
person["age"] = 26       # Update value
person["city"] = "Dhaka" # Add new key-value
print(person)
```

**Output:**

```
{'name': 'Arafat', 'age': 26, 'city': 'Dhaka'}
```

### Set (Unique, Unordered)

```python
numbers = {1, 2, 3, 2, 1}
numbers.add(4)
print(numbers)
```

**Output:**

```
{1, 2, 3, 4}
```

- Sets **remove duplicates automatically**
- Order is **not guaranteed**

---

## 4️⃣ Type Checking

Use `type()` to check the data type of a variable:

```python
x = 10
print(type(x))   # <class 'int'>
y = 3.5
print(type(y))   # <class 'float'>
```

---

## 5️⃣ Type Conversion

You can convert between types:

```python
x = 10       # int
y = float(x) # convert to float
z = str(x)   # convert to string
print(x, y, z)
```

**Output:**

```
10 10.0 10
```

---

## 6️⃣ Naming Rules for Variables

1. Must start with a **letter** or **underscore** (\_)
2. Can contain letters, numbers, underscores
3. **Case-sensitive** (`x` and `X` are different)
4. Cannot use Python **reserved keywords** (`for`, `if`, `while`)

```python
_age = 25
name1 = "Rima"
# 1name = "Invalid"  -> ❌ Not allowed
```

---

## 7️⃣ Summary

- Variables store **data in memory**.
- Python automatically **detects the type** (dynamic typing).
- Use **`type()`** to check the data type.
- Python has several **basic data types**: int, float, str, bool, list, tuple, dict, set.
- Variables can be **reassigned** or **converted** to other types.
- **Lists** are mutable, **tuples** are immutable, **dictionaries** store key-value pairs, and **sets** store unique unordered items.

---

This notebook contains **hands-on examples** to practice all the above concepts.
Run each cell to understand how variables and data types work in Python.

```

```

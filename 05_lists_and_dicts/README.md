# 🛠 Lists & Dictionaries in Python

Lists and dictionaries are **essential data structures** in Python.
They allow you to **store, organize, and manipulate data efficiently**, making programs more flexible and powerful.

---

## 1️⃣ Lists

A **list** is an **ordered, mutable collection** of items.
You can store numbers, strings, booleans, or even other lists inside a list.

### Creating a List

```python
fruits = ["apple", "banana", "mango"]
print(fruits)
```

**Output:**

```
['apple', 'banana', 'mango']
```

---

### Accessing Elements

Use **indexes** to access items (0-based index).

```python
print(fruits[0])  # first element
print(fruits[-1]) # last element
```

**Output:**

```
apple
mango
```

---

### Modifying Lists

Lists are mutable, so you can **add, remove, or change elements**.

```python
fruits.append("orange")  # add
fruits[1] = "grape"      # modify
fruits.remove("apple")   # remove
print(fruits)
```

**Output:**

```
['grape', 'mango', 'orange']
```

---

### Slicing a List

```python
numbers = [1, 2, 3, 4, 5, 6]
print(numbers[2:5])  # from index 2 to 4
print(numbers[:3])   # first 3 elements
print(numbers[3:])   # elements from index 3 to end
```

**Output:**

```
[3, 4, 5]
[1, 2, 3]
[4, 5, 6]
```

---

### Looping Through Lists

```python
for fruit in fruits:
    print(fruit)
```

**Output:**

```
grape
mango
orange
```

---

### List Comprehensions

Create lists **efficiently** using comprehension.

```python
squares = [x**2 for x in range(5)]
print(squares)
```

**Output:**

```
[0, 1, 4, 9, 16]
```

---

## 2️⃣ Dictionaries

A **dictionary** is an **unordered collection of key-value pairs**.
Keys are unique, and values can be any data type.

### Creating a Dictionary

```python
person = {"name": "Rahim", "age": 25, "city": "Dhaka"}
print(person)
```

**Output:**

```
{'name': 'Rahim', 'age': 25, 'city': 'Dhaka'}
```

---

### Accessing Values

```python
print(person["name"])
print(person.get("age"))
```

**Output:**

```
Rahim
25
```

---

### Modifying a Dictionary

```python
person["age"] = 26      # update
person["profession"] = "Developer"  # add new key-value
print(person)
```

**Output:**

```
{'name': 'Rahim', 'age': 26, 'city': 'Dhaka', 'profession': 'Developer'}
```

---

### Removing Items

```python
person.pop("city")  # remove by key
del person["age"]   # delete key
print(person)
```

**Output:**

```
{'name': 'Rahim', 'profession': 'Developer'}
```

---

### Looping Through a Dictionary

```python
for key, value in person.items():
    print(f"{key}: {value}")
```

**Output:**

```
name: Rahim
profession: Developer
```

---

### Dictionary Comprehensions

```python
A list comprehension has the general form:
```

[expression for item in iterable]

```
expression → what you want to compute/store for each item.

item → variable that takes each value from the iterable.

iterable → any Python iterable, like range(), list, tuple, etc.

squares = {x: x**2 for x in range(5)}
print(squares)
```

**Output:**

```
{0: 0, 1: 1, 2: 4, 3: 9, 4: 16}
```

---

## 3️⃣ Summary

- **Lists** → ordered, mutable collections; use indexes to access items.
- **Dictionaries** → unordered, key-value pairs; keys are unique.
- Lists are useful for **sequences**; dictionaries are useful for **mapping**.
- Both support **looping, adding, modifying, and deleting** elements.
- Comprehensions allow **quick creation** of lists and dictionaries.

---

This notebook contains **hands-on examples** of lists and dictionaries.
Run each cell to practice and fully understand Python data structures. 🚀

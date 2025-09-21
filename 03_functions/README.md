# 🛠 Functions in Python

Functions are one of the most important concepts in Python.  
They allow us to **group code into reusable blocks**, making programs cleaner and easier to understand.

---

## 1️⃣ What is a Function?

A **function** is a block of code that runs only when called.  
It can take inputs (**parameters**) and return an output (**return value**).

### Example

```python
def greet():
    print("Hello, welcome to Python!")

greet()  # calling the function
```

**Output:**

```
Hello, welcome to Python!
```

---

## 2️⃣ Function with Parameters

Functions can take inputs (arguments) to work with.

```python
def greet(name):
    print(f"Hello, {name}!")

greet("Arafat")
greet("Jawad")
```

**Output:**

```
Hello, Arafat!
Hello, Jawad!
```

---

## 3️⃣ Function with Return Value

Functions can return values using the `return` keyword.

```python
def add(a, b):
    return a + b

result = add(5, 3)
print(result)
```

**Output:**

```
8
```

---

## 4️⃣ Default Arguments

You can give **default values** to parameters.

```python
def greet(name="Guest"):
    print(f"Hello, {name}!")

greet()        # uses default
greet("Nusrat")
```

**Output:**

```
Hello, Guest!
Hello, Nusrat!
```

---

## 5️⃣ Keyword Arguments

You can pass arguments by name for clarity.

```python
def introduce(name, age):
    print(f"My name is {name} and I am {age} years old.")

introduce(age=25, name="Rahim")
```

**Output:**

```
My name is Rahim and I am 25 years old.
```

---

## 6️⃣ Variable-Length Arguments

### `*args` → Multiple positional arguments

\*args allows a function to accept any number of positional arguments.

```python
def add_all(*numbers):
    return sum(numbers)

print(add_all(1, 2, 3, 4))
```

**Output:**

```
10
```

---

### `**kwargs` → Multiple keyword arguments

\*\*kwargs allows a function to accept any number of keyword arguments (i.e., named arguments).
Inside the function, kwargs behaves like a dictionary.

```python
def print_info(**details):
    for key, value in details.items():
        print(f"{key}: {value}")

print_info(name="Arafat", age=25, city="Dhaka")
```

**Output:**

```
name: Arafat
age: 25
city: Dhaka
```

---

## 7️⃣ Variable Scope

- **Local variables** exist only inside functions.
- **Global variables** are accessible everywhere.

```python
x = 10  # global

def my_func():
    y = 5  # local
    print("Inside function:", x, y)

my_func()
print("Outside function:", x)
```

**Output:**

```
Inside function: 10 5
Outside function: 10
```

---

## 8️⃣ Lambda Functions (Anonymous Functions)

Short, single-line functions created with `lambda`.

A lambda function is a small, unnamed function defined in a single line using the lambda keyword.
Syntax:
lambda arguments: expression

arguments → input parameters
expression → a single expression whose result is returned automatically

```python
square = lambda x: x * x
print(square(5))
```

**Output:**

```
25
```

---

## 9️⃣ Recursion (Function Calling Itself)

A function can call itself to solve problems (like factorial, Fibonacci).

```python
def factorial(n):
    if n == 1:
        return 1
    return n * factorial(n-1)

print(factorial(5))
```

**Output:**

```
120
```

---

## 🔟 Summary

- Functions help **reuse code**.
- Functions can take **parameters** and return **values**.
- Use **default arguments** and **keyword arguments** for flexibility.
- **`*args`** and **`**kwargs`\*\* allow variable numbers of inputs.
- Variables have **local** and **global scope**.
- **Lambda functions** are short one-liners.
- Functions can be **recursive**.

---

This notebook contains **hands-on examples** of all function types.
Run each cell to practice and fully understand Python functions. 🚀

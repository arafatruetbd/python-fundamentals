# 🛠 File Handling in Python

File handling is a fundamental concept in Python.
It allows us to **read from, write to, and manipulate files**, making programs capable of persisting data.

---

## 1️⃣ Opening a File

You can open a file using the `open()` function.
The syntax is:

```python
open(filename, mode)
```

- `filename` → name of the file
- `mode` → how you want to open it (`'r'`, `'w'`, `'a'`, `'rb'`, `'wb'`)

### Example

```python
file = open("example.txt", "w")  # open file for writing
file.write("Hello, Python!")
file.close()
```

**Output:**
Creates a file `example.txt` with content `Hello, Python!`.

---

## 2️⃣ Reading a File

You can read files using `.read()`, `.readline()`, or `.readlines()`.

```python
file = open("example.txt", "r")
content = file.read()
print(content)
file.close()
```

**Output:**

```
Hello, Python!
```

---

### Using `.readline()`

Reads **one line at a time**:

file.readline() reads up to the newline character (\n) or the end of the file, and returns it as a string.

```python
file = open("example.txt", "r")
line = file.readline()
print(line)
file.close()
```

**Output:**

```
Hello, Python!
```

---

### Using `.readlines()`

Reads **all lines into a list**:

The .readlines() method reads all lines of a file at once and returns them as a list of strings, where each string is one line from the file.

```python
file = open("example.txt", "r")
lines = file.readlines()
print(lines)
file.close()
```

**Output:**

```
['Hello, Python!']
```

---

## 3️⃣ Writing to a File

- **`'w'` → write mode (overwrites file)**
- **`'a'` → append mode (adds to end of file)**

```python
file = open("example.txt", "a")
file.write("\nWelcome to Python file handling!")
file.close()
```

**Output:**
Appends the text to `example.txt`.

---

## 4️⃣ Using `with` Statement (Recommended)

Automatically closes the file after the block.

```python
with open("example.txt", "r") as file:
    content = file.read()
    print(content)
# No need to call file.close(), it is done automatically
```

**Output:**

```
Hello, Python!
Welcome to Python file handling!
```

---

## 5️⃣ Reading and Writing in Binary Mode

Binary mode is used when working with non-text files like images, audio, videos, or any raw data.

wb → write in binary mode

rb → read in binary mode

```python
# Writing binary data
with open("data.bin", "wb") as file:
    file.write(b'\x00\x01\x02\x03')  # b'' indicates bytes

# Reading binary data
with open("data.bin", "rb") as file:
    data = file.read()
    print(data)
```

**Output:**

```
b'\x00\x01\x02\x03'
```

---

## 6️⃣ File Methods

- `file.read(size)` → read `size` bytes
- `file.readline()` → read next line
- `file.readlines()` → read all lines
- `file.write(string)` → write string to file
- `file.writelines(list_of_strings)` → write multiple lines
- `file.close()` → close file

---

## 7️⃣ Checking File Existence

```python
import os

if os.path.exists("example.txt"):
    print("File exists!")
else:
    print("File does not exist!")
```

**Output:**

```
File exists!
```

---

## 8️⃣ Deleting a File

```python
import os

os.remove("example.txt")
print("File deleted!")
```

**Output:**

```
File deleted!
```

---

## 9️⃣ Summary

- **Open files** → `open(filename, mode)`
- **Read files** → `.read()`, `.readline()`, `.readlines()`
- **Write files** → `'w'` (overwrite), `'a'` (append)
- **Binary files** → `'rb'`, `'wb'`
- **Automatic closing** → use `with` statement
- **Check and delete** → `os.path.exists()` and `os.remove()`
- File handling is **essential for persistent data storage**.

---

This notebook contains **hands-on examples** of all file operations.
Run each cell to practice and fully understand **Python file handling**. 🚀

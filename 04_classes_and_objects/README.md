# 🛠 Classes & Objects in Python

Classes and objects are the **cornerstones of object-oriented programming (OOP)** in Python.  
They allow us to **model real-world entities**, organize code logically, and make it reusable and maintainable.

---

## 1️⃣ What is a Class?

A **class** is like a blueprint for creating objects.  
It defines the **attributes** (data) and **methods** (functions) that the objects will have.

```python
class Person:
    pass  # empty class

# Create an object of the class
p1 = Person()
print(p1)
```

**Output:**

```
<__main__.Person object at 0x...>
```

---

## 2️⃣ Object (Instance of a Class)

An **object** is an **instance** of a class.
You can create multiple objects from the same class.

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

# Create objects
p1 = Person("Karim", 25)
p2 = Person("Rahim", 30)

print(p1.name, p1.age)
print(p2.name, p2.age)
```

**Output:**

```
Karim 25
Rahim 30
```

---

## 3️⃣ The `__init__` Method (Constructor)

The `__init__` method initializes the object's attributes when it is created.

```python
class Car:
    def __init__(self, brand, model):
        self.brand = brand
        self.model = model

my_car = Car("Toyota", "Corolla")
print(my_car.brand, my_car.model)
```

**Output:**

```
Toyota Corolla
```

---

## 4️⃣ Instance Methods

Methods are **functions inside a class** that operate on object data.

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def greet(self):
        print(f"Hello, my name is {self.name} and I am {self.age} years old.")

p1 = Person("Rahim", 25)
p1.greet()
```

**Output:**

```
Hello, my name is Rahim and I am 25 years old.
```

---

## 5️⃣ Class Variables vs Instance Variables

- **Instance variables** → unique to each object (`self.name`, `self.age`)
- **Class variables** → shared across all instances

```python
class Dog:
    species = "Canine"  # class variable

    def __init__(self, name):
        self.name = name  # instance variable

d1 = Dog("Rex")
d2 = Dog("Buddy")

print(d1.name, d1.species)
print(d2.name, d2.species)
```

**Output:**

```
Rex Canine
Buddy Canine
```

---

## 6️⃣ Inheritance

A class can **inherit** attributes and methods from another class.

```python
class Animal:
    def __init__(self, species):
        self.species = species

    def sound(self):
        print("Some sound")

class Dog(Animal):
    def __init__(self, name):
        super().__init__("Dog")  # call parent constructor
        self.name = name

    def sound(self):
        print("Woof!")

d = Dog("Rex")
print(d.name, d.species)
d.sound()
```

**Output:**

```
Rex Dog
Woof!
```

---

## 7️⃣ Encapsulation (Private Attributes)

Use **underscore** `_` or double underscore `__` to make attributes private.

```python
class Person:
    def __init__(self, name, age):
        self.__name = name  # private attribute
        self.age = age

    def get_name(self):
        return self.__name

p = Person("Rahim", 25)
print(p.get_name())
# print(p.__name) -> ❌ Error
```

**Output:**

```
Rahim
```

---

## 8️⃣ Polymorphism

**Polymorphism** allows different objects to respond differently to the same method call.

```python
class Cat:
    def sound(self):
        print("Meow")

class Dog:
    def sound(self):
        print("Woof")

animals = [Cat(), Dog()]
for animal in animals:
    animal.sound()
```

**Output:**

```
Meow
Woof
```

---

## 9️⃣ Special Methods (`__str__`, `__repr__`)

Special methods allow customization of object behavior.

**str** → human-readable, used by print() or str().

**repr** → official/unambiguous string, used in interpreter or debugging.

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def __str__(self):
        return f"{self.name}, {self.age} years old"

p = Person("Rahim", 25)
print(p)
```

**Output:**

```
Rahim, 25 years old
```

---

## 🔟 Summary

- **Class** → blueprint for creating objects
- **Object** → instance of a class
- **`__init__`** → constructor to initialize attributes
- **Instance & Class variables** → object-specific vs shared
- **Inheritance** → reuse parent class functionality
- **Encapsulation** → hide private data
- **Polymorphism** → same method behaves differently for different objects
- **Special methods** → customize object behavior

---

This notebook contains **hands-on examples** of classes and objects.
Run each cell to practice and fully understand Python OOP. 🚀

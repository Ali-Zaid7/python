# python

# ✅ Python Bytecode Summary (Test Prep Version)

---

## 📌 1. What is Python Bytecode?

- **Intermediate representation** of Python code (not human-readable).
- Created **after compilation**, but **before execution**.
- Stored in `.pyc` files in `__pycache__` folder.
- **Platform-independent** but needs the correct **Python interpreter version**.

---

## 🔄 2. Compilation Process (Steps)

1. **Lexical Analysis**: Breaks code into tokens (e.g., `def`, `name`, `42`).
2. **Syntax Analysis**: Checks if structure is valid Python (e.g., correct use of `:` or `()`).
3. **Semantic Analysis**: Verifies meaning — like checking types or variable usage.
4. **Bytecode Generation**: Converts code to **bytecode** for execution.

---

## 🧠 3. Why Bytecode is Important

- ✅ **Platform-independent**: Same `.pyc` runs on Windows, macOS, Linux.
- ✅ **Dynamic Typing**: Types checked **during** runtime, not before.
- ✅ **Flexible**: Bytecode can be modified; helps in debugging, extensions.

---

## 🧪 4. Example Code

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def greet(self):
        print(f"Hello, my name is {self.name} and I am {self.age} years old.")

person = Person("Arif Rozani", 20)
person.greet()


# 🐍 Python Indentation & Type Hinting

---

## 🧱 Indentation in Python

### 🔹 Introduction:

In Python, **indentation is used to denote a block of code** within a control structure, function, or class. It is a crucial aspect of Python syntax, and incorrect indentation can lead to syntax errors.

---

### ❓ What is Indentation?

Indentation means **adding spaces or tabs** at the beginning of a line to indicate it’s part of a block.

- Defines the **structure** of the code.
- Shows **relationships** between different code blocks.

---

### 🎯 Why is Indentation Important?

- Defines the structure of the code.
- Shows the relationship between code blocks.
- Makes the code more **readable**.
- **Prevents syntax errors.**

---

### 📏 Rules of Indentation:

- ✅ Use **consistent indentation**: Either spaces or tabs (not both).
- ✅ Use **4 spaces** for each level (PEP8 standard).
- ✅ Indent after a **colon (:)**.
- ✅ Indent inside functions and class definitions.

---

### ✅ Correct vs ❌ Incorrect Indentation Examples:

```python
# ✅ Correct indentation
if True:
    print("Hello, World!")
    print("This is a block of code")

# ❌ Incorrect indentation
if True:
print("Hello, World!")
  print("This is a block of code")

# ✅ Correct function
def greet(name: str):
    print("Hello, " + name + "!")

# ❌ Incorrect function
def greet(name: str):
print("Hello, " + name + "!")
```

# Best Practices:
Use IDE auto-indentation.
Prefer spaces over tabs (PEP 8 guideline).
Dynamic Typing & Type Hinting
Dynamic Typing:

Types resolved at runtime (e.g., x = 5 → int, x = "hi" → str).

# Example:

```
age = input("Age: ")  # Returns str, even if number entered
print(type(age))      # Output: <class 'str'>
Type Hinting (Python 3.5+)
```
# Syntax:
```
def greet(name: str) -> str:  # Parameter & return type hints
    return f"Hello, {name}"
```

# Complex Types:

```
from typing import List, Dict
scores: List[int] = [90, 85]
student: Dict[str, int] = {"age": 20}
```
# Why Use Type Hints?
Better readability.
IDE autocompletion.
Catch errors early with tools like mypy.

# Key Test Takeaways
# Indentation:
Required for blocks.
4 spaces standard.

# Type Hints:
Optional annotations (variable: type = value) for better code clarity and IDE support, but Python remains 
dynamically typed (types checked at runtime). Example: def greet(name: str) -> str: ...

Key Point: Helps catch errors early but doesn't enforce types during execution.

Optional but recommended.
Syntax: variable: type = value.
Use -> for return types.

# Object-Based Language vs. Object-Oriented Language

## 📌 Object-Based Language

### 🔹 Definition
An **object-based language** supports the use of objects but **does not implement all features** of Object-Oriented Programming (OOP). Features like **inheritance** and **polymorphism** may not be available.

### 🔹 Characteristics
- ✅ Supports **objects** and **encapsulation**
- ❌ Does **not necessarily support inheritance** or **polymorphism**
- 📎 **Examples:** `JavaScript (pre-ES6)`, `VBScript`, `Pascal (some versions)`

### 🔹 Use Cases
- Suitable for **scripting** and **simpler applications** where full OOP features are not needed.

---

## 📌 Object-Oriented Language

### 🔹 Definition
An **object-oriented language** fully supports the core principles of OOP: **encapsulation**, **inheritance**, and **polymorphism**. This enables the creation of **modular, reusable, and maintainable** code.

### 🔹 Characteristics
- ✅ Supports **encapsulation**
- ✅ Supports **inheritance**
- ✅ Supports **polymorphism**
- 📎 **Examples:** `Python`, `Java`, `C++`, `Ruby`

### 🔹 Use Cases
- Used in **large-scale software development**.
- Promotes **code reuse**, **maintainability**, and **clean architecture**.

---

## 📊 Comparison Table

| Feature         | Object-Based Language                | Object-Oriented Language      |
|----------------|---------------------------------------|-------------------------------|
| Encapsulation  | ✅ Supported                          | ✅ Supported                  |
| Inheritance    | ❌ Not necessarily supported          | ✅ Fully supported            |
| Polymorphism   | ❌ Not necessarily supported          | ✅ Fully supported            |
| Examples       | JavaScript (pre-ES6), VBScript        | Python, Java, C++, Ruby       |

---

> ✨ **Tip:** Use Object-Oriented languages when building scalable and complex applications. Choose Object-Based
>  languages for simpler scripts and tasks where full OOP isn't required.
>
> # 🐍 The Python's Object-Centric Nature

## 📌 Python as an Object-Centric Language

Python treats **everything as an object**, from integers and strings to functions and classes. This object-centric nature allows Python to support **both procedural and object-oriented programming paradigms** with ease.

---

## 🔹 Everything is an Object

In Python, even primitive data types like `int`, `str`, and `list` are objects. This means they come with built-in **methods** and **properties**.

```python
# Example: Integer as an object
x: int = 100
print(x.bit_length())  # Method call on an integer object
```

## 🔹 First-Class Functions
Python supports first-class functions, meaning functions can be:

Assigned to variables
Passed as arguments
Returned from other functions

```
def greet(name) -> str:
    return f"Hello, {name}!"

def call_function(func, name) -> str:
    return func(name)

print(call_function(greet, "Alice"))  # Passing a function as an argument
# Output : Hello ALice!
```

# 🔹 Support for OOP Principles
Python fully supports Object-Oriented Programming (OOP), including:

✅ Encapsulation
✅ Inheritance
✅ Polymorphism

# 🦆 Duck Typing in Python

**Duck typing** is a fundamental concept in Python that allows developers to write **flexible and dynamic code**. It aligns with Python’s philosophy of:  
> _“We are all consenting adults here.”_

Rather than enforcing strict types, Python emphasizes **what an object can do**, not what it is.

---

## 🔍 What is Duck Typing?

Duck typing focuses on **behavior over type**.  
If an object has the necessary methods or attributes, it can be used—regardless of its class.

> "If it walks like a duck and talks like a duck, it's a duck."

---

## ⚙️ How Duck Typing Works in Python

Python **does not check an object's type** before calling a method.  
Instead, it tries to execute the method and raises an error **only if** the method doesn't exist.

---

## 🧪 Example: Parrots, Humans, and Robots

Let’s define a function that expects the object to have a `speak()` method, regardless of its class.

```python
class Human:
    def speak(self):
        print("Human: I'm good, thanks!")

class Parrot:
    def speak(self):
        print("Parrot: Polly wants a cracker!")

def have_conversation(person):
    print("\nhave_conversation: Hello, how are you?", type(person))
    person.speak()

human = Human()
parrot = Parrot()

have_conversation(human)
have_conversation(parrot)
```

# 🤖 Adding New Types
You can easily extend this logic to other objects:
```
class Robot:
    def speak(self):
        print("Robot: Beep boop, I am functioning within normal parameters!")

robot = Robot()
have_conversation(robot)

```

# ✅ Why It’s Useful
✔️ No need for strict type hierarchies
✔️ Easy to extend behavior
✔️ Promotes clean and flexible code

🧠 Duck Typing = Polymorphism without inheritance
It allows Python functions to interact with any object as long as it behaves as expected.


# Ab asan treen Summary

## 🦆 Duck Typing in Python — A Concise Summary

Duck typing is a powerful concept in Python that allows for flexible and dynamic code by focusing on *behavior* rather than *type*.

---

### 📋 Quick Reference Table

| Feature        | Description                                                                 |
|----------------|-----------------------------------------------------------------------------|
| 🔍 **Definition**     | Type check nahi hota, behavior (methods/attributes) check hota hai               |
| 🧠 **Philosophy**     | "Agar bolta hai jaise duck, chalta hai jaise duck, to ye duck hi hoga"           |
| 🎯 **Focus**          | Kya object `kar sakta hai` (e.g., `speak()` method), na ke uska class ya type     |
| 🧪 **Example**        | `Human`, `Parrot`, `Robot` — sab me `speak()` hai, to function un sab pe chalega |
| 💡 **Use Case**       | Jab multiple classes same behavior follow karein                                 |
| ✅ **Advantage**      | Code becomes flexible, extendable, and less tightly coupled                      |

---

### 🧠 Mnemonic — "DUCK SPEAK karta hai"

> **D** = Don’t check type  
> **U** = Use same method  
> **C** = Code is flexible  
> **K** = Keep adding new types  

---

### 🎯 One-Line Reminder

> **“Agar object me required method hai, to wo valid hai — chahe wo kis bhi type ka ho.”**

---

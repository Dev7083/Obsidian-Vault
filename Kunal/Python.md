### 🟢 1. Setup & Basics

- Install Python
- Use terminal / VS Code
- Run:

`print("Hello World")`

#### Basics:

- A **high-level, interpreted language**
- Designed to be **simple and readable**
- Used in web, automation, AI, data science
- Easy to learn
- Interpreted
- Dynamically typed
- Object-oriented
- Rich in libraries
- Code structure depends on indentation
####  Input & Output

```python
name = input("Enter name: ")  
print(name)
```
#### Indentation

Python uses spaces instead of `{}`

```python
if True:  
    print("Correct")
```

---

## 🧩 2. Variables & Data Types (Core Foundation)

```python
name = "Dev"  
age = 21  
price = 99.99  
is_active = True
```
Learn:

- `int`, `float`, `str`, `bool`
- Type checking:

type(name)

---

## 🔤 3. Strings (Very Important)


```python
text = "python"  
print(text.upper())  
print(text[0])
```

Learn:

- Slicing → `text[0:3]`
- Methods → `lower()`, `strip()`, `replace()`

---

## 🔢 4. Operators

- Arithmetic → `+ - * / %`
- Comparison → `> < ==`
- Logical → `and or not`

---

## 🔀 5. Conditional Statements

```python
if age > 18:  
    print("Adult")  
elif age == 18:  
    print("Exactly 18")  
else:  
    print("Minor")
```


---

## 🔁 6. Loops
```python
for i in range(5):  
    print(i)  
  
while True:  
    break

```

Learn:

- `break`, `continue`
- Loop over list/string

---

## 📦 7. Data Structures (Very Important)

### List

```python
nums = [1,2,3]  
nums.append(4)
```

### Tuple (immutable)

`t = (1,2,3)`

### Set (unique values)

`s = {1,2,3}`

### Dictionary

```python
user = {"name": "Dev", "age": 21}  
print(user["name"])
```

---

## 🧱 8. Functions

```python
def add(a, b):  
    return a + b
```

Learn:

- Parameters
- Return values
- Default arguments

---

## 📂 9. File Handling

with open("file.txt", "r") as f:  
    data = f.read()

Modes:

- `"r"` read
- `"w"` write
- `"a"` append

---

## ⚠️ 10. Error Handling

```Python
try:  
    x = 10 / 0  
except:  
    print("Error occurred")
```

---

## 🧠 11. OOP (Object-Oriented Programming)

```python
class Person:  
    def __init__(self, name):  
        self.name = name  
  
p = Person("Dev")
```
Learn:

- Class & object
- Constructor
- Methods

---

## 📦 12. Modules & Packages

```python
import math  
print(math.sqrt(16))
```

Also:

- `pip install` libraries

---

## 🔄 13. List Comprehension (Important)

`nums = [x for x in range(5)]`
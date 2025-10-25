# Data Types in Python

In programming, a **data type** is a classification that specifies what kind of value a variable can hold. Data types are essential because they determine how data is stored in memory and what operations can be performed on that data. Python supports several built-in data types. Here are the common ones:

---

## 1. Numeric Data Types
| Type | Description | Example |
|------|-------------|---------|
| `int` | Integer numbers (whole numbers) | `x = 5` |
| `float` | Floating-point numbers (with decimals) | `y = 3.14` |
| `complex` | Complex numbers (real + imaginary) | `z = 2 + 3j` |

---

## 2. Sequence Types
| Type | Description | Example |
|------|-------------|---------|
| `str` | String (sequence of characters) | `text = "Hello, World"` |
| `list` | List (ordered, mutable sequence) | `my_list = [1, 2, 3]` |
| `tuple` | Tuple (ordered, immutable sequence) | `my_tuple = (1, 2, 3)` |

---

## 3. Mapping Type
| Type | Description | Example |
|------|-------------|---------|
| `dict` | Dictionary (key-value pairs) | `my_dict = {'name': 'John', 'age': 30}` |

---

## 4. Set Types
| Type | Description | Example |
|------|-------------|---------|
| `set` | Set (unordered, unique elements) | `my_set = {1, 2, 3}` |
| `frozenset` | Immutable set | `my_frozenset = frozenset([1, 2, 3])` |

---

## 5. Boolean Type
| Type | Description | Example |
|------|-------------|---------|
| `bool` | Boolean values (`True` or `False`) | `is_valid = True` |

---

## 6. Binary Types
| Type | Description | Example |
|------|-------------|---------|
| `bytes` | Immutable sequence of bytes | `data = b'Hello'` |
| `bytearray` | Mutable sequence of bytes | `data = bytearray(b'Hello')` |

---

## 7. None Type
| Type | Description | Example |
|------|-------------|---------|
| `NoneType` | Represents the absence of a value | `x = None` |

---

## 8. Custom Data Types
- You can define your own **data types** using **classes and objects**:

```python
# Custom data type: Person
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

# Create an object
p = Person("Alice", 25)

# Print details
print(p.name)  # Alice
print(p.age)   # 25
```
### ✅ Explanation in one line:

- class Person: → defines a new type.
- p = Person("Alice", 25) → creates an object of that type.
- p.name / p.age → access the stored values.

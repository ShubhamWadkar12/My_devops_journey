# 📝 Python Basics: Variables, Data Types & Operators

---

## 🔹 Variables
A **variable** is a name given to a memory location in a program.  
It acts as a container to store a value.

```python
a = 1            #variable
b = 'Shubham'    #string
c = 2.5          #float
d = True         #boolean
e = None        #null value
```
- Keywords: Reserved words in Python like if, for, while
- Identifiers: Names used for classes, functions, and variable

## 🔹 Data Types

Python automatically identifies the type of data. Common data types:

Integers (int)

Floating point numbers (float)

Strings (str)

## 🔹 Rules for Choosing an Identifier
Can contain alphabets, digits, and underscores (_)
Must start with an alphabet or underscore
Cannot start with a digit
No spaces are allowed

Examples:
harry, one8, seven, _seven

## 🔹 Operators in Python
Python supports several types of operators:

- Arithmetic Operators:  +, -, *, /, %, **, //
- Assignment Operators:  =, +=, -=, *=, /=
- Comparison Operators:  ==, !=, >, >=, <, <=
- Logical Operators:     and, or, not
- Booleans (bool):      True or False
- None (NoneType):      Null

# 🐍 Type Function, Typecasting & Input

---

## 🔹 `type()` Function
The `type()` function is used to find the **data type** of a variable in Python.

```python
a = 31
print(type(a))  # <class 'int'>

b = "31"
print(type(b))  # <class 'str'>
```

## 🔹 Typecasting

Python allows conversion between data types when possible.
```
# Integer to String
str(31)   # "31"

# String to Integer
int("32") # 32

# Integer to Float
float(32) # 32.0

"31" is a string literal

31 is a numeric literal
```

## 🔹 input() Function

The input() function allows the user to take input from the keyboard.
```
A = input("Enter name: ")
print("You entered:", A)

If the user enters Shubham, the output will be "Shubham"
Important: The output of input() is always a string, even if a number is entered.
```

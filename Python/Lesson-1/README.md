#  🤖 Programming Introduction

## 💻 What is Programming?
Just like we use **Hindi** or **English** to talk to each other, we use a **programming language** to communicate with a computer.  
Programming is a way to **give instructions** to the computer to perform different tasks.

---

## 🐍 What is Python?
Python is a **simple and easy-to-understand language** that feels like reading plain English.  
Its **pseudo-code style** makes it beginner-friendly and quick to learn.

---

## 🌟 Features of Python
- **Easy to understand:** Less time to write code  
- **Free & Open Source:** No cost to use  
- **High-level language:** Simple syntax for humans  
- **Portable:** Works on Linux, Windows, and Mac  
- **Fun to work with!**

---

## 🛠️ Installation
1. Go to [python.org](https://www.python.org/) and download Python for your platform.  
2. Run the setup to install Python on your system.  

### 🎉 Your First Program
Create a file called `hello.py` and add:  
```python
print("Hello World")  # print is a function that shows output
```

You will see:
```
Hello World
```
## 📦 Modules & Pip

1. A module is a file containing code written by someone else that you can use in your program.
2. Pip is Python's package manager. Install external modules using:
```
pip install flask  # Example: installs Flask module
```
## 🏷️ Types of Modules
1. Built-in Modules: Pre-installed with Python (e.g., os, random)
2. External Modules: Need to install via pip (e.g., tensorflow, flask)

## 🔢 Using Python as a Calculator

1. Open terminal and type python to enter the REPL (Read Evaluate Print Loop).
2. You can perform calculations directly here:
```
>>> 5 + 3
8
```
## 📝 Comments
- Comments are notes in your code that are not executed.
- Types of Comments
```
Single-line comment:
# This is a single-line comment
```
```
Multi-line comment:
"""
This is a 
multi-line comment
"""
```
## 🏗️ Object-Oriented Programming (OOP) in Python
Python supports Object-Oriented Programming (OOP), which helps organize code in a modular and reusable way.

Key OOP Concepts

📦 Class: Blueprint to create objects

👤 Object: Instance of a class

🔒 Encapsulation: Keep data safe inside a class

♻️ Inheritance: Reuse code from one class in another

🔄 Polymorphism: Use objects of different classes in a similar way

🕵️‍♂️ Abstraction: Hide unnecessary details

> OOP makes code easy to maintain, scale, and reuse, which is important for DevOps automation.

## ⚙️ How Python is Used in DevOps

Python is widely used in DevOps for:

🤖 Automation: Automate deployments, backups, monitoring, etc.

☁️ Infrastructure as Code (IaC): Manage cloud resources with Ansible, Terraform, AWS SDK (Boto3)

🚀 CI/CD Pipelines: Write scripts for Jenkins, GitHub Actions, GitLab CI

📊 Monitoring & Logging: Process logs and generate alerts

🐳 Containerization & Orchestration: Manage Docker containers and Kubernetes clusters

📈 Reporting & Analytics: Analyze operational data for better decision-making

> 💡 Python + OOP = clean, modular, and scalable code, improving deployment speed and reliability.

## 🏁 Practice Exercises

### 1. Print the poem *Twinkle Twinkle Little Star*
```python
print("Twinkle, Twinkle, Little Star,")
print("How I wonder what you are!")
print("Up above the world so high,")
print("Like a diamond in the sky.")
print("Twinkle, Twinkle, Little Star,")
print("How I wonder what you are!")
```
### 2. Use REPL to print the multiplication table of 5
```
# Open Python REPL by typing `python` in terminal
for i in range(1, 11):
    print(f"5 x {i} = {5*i}")
```
### 3. Install an external module and use it
```
pip install requests  # Example: install requests module
```
```
import requests
response = requests.get("https://api.github.com")
print(response.status_code)  # Prints HTTP status code
```
### 4. Print the contents of a directory using os module
```
import os
# List all files and directories in current directory
files = os.listdir(".")
print("Contents of the directory:")
for file in files:
    print(file)
```

5. Add comments to your program
```
import os  # Importing os module to work with directories
# Get all files and directories in current folder
files = os.listdir(".")  
print("Contents of the directory:")  # Print header
# Loop through each item and print its name
for file in files:
    print(file)
```


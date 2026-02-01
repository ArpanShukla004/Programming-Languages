# Python: Getting Started Guide

> "There should be one—and preferably only one—obvious way to do it."  
> — The Zen of Python

- And with that, the `python` language was programmed.

---

## **What IS Python, Really?**

A **high-level programming language** — meaning it's closer to human language than machine code.

```
Human Brain → Python → Machine Language → Computer Action
  "add two"  → 2 + 2 → 01010101... → CPU calculates
```

## **Etymology: Why the word "Python"?**

- Created by **Guido van Rossum** in 1991, named after **Monty Python's Flying Circus** (the comedy group), not the snake! 🐍

**Philosophy:** Code should be *fun to write* and *easy to read*.

## **Core Principle: Readability First**

Python sacrifices speed for **clarity**. Compare:

**C++:**
```cpp
#include <iostream>
int main() {
    std::cout << "Hello" << std::endl;
    return 0;
}
```

**Python (clean):**
```python
print("Hello")
```

**The Philosophy:** If a human can't read it easily, it's not "Pythonic".

---

## **Gearing up**

### Pre-requisites

- **Python installed** (from python.org)  
- **PATH configured** (check "Add to PATH")  
- **A text editor** ([PyCharm](https://www.jetbrains.com/pycharm/) or [VS Code](https://code.visualstudio.com))
- **Verified with** `python --version`

## 1. **Download Python**

### **Official Source (Recommended: Latest stable version)**
🔗 **https://www.python.org/downloads/**

- Choose your OS: Windows, macOS, or Linux

## **Installation by OS**

### **Windows**

1. **Run the installer** (`.exe` file)
2. **CHECK THIS BOX:** "Add Python to PATH"
   ```
   [✓] Add python.exe to PATH  ← CRITICAL!
   ```
3. Click **"Install Now"**
4. Wait ~2 minutes

**Verify:**
```bash
python --version
# Output: Python 3.12.x
```

---

### **macOS**

**Method 1: Official Installer**
1. Download `.pkg` file from python.org
2. Run installer → Follow prompts
3. Done

**Method 2: Homebrew** (if installed)
```bash
brew install python3
```

**Verify:**
```bash
python3 --version
```

---

### **Linux (Ubuntu/Debian)**

Most Linux distros **have Python pre-installed**.

**Check:**
```bash
python3 --version
```

**If missing, install:**
```bash
sudo apt update
sudo apt install python3 python3-pip
```

## **2. Package Manager: pip**

[pip](https://pypi.org/) installs Python libraries (comes with Python 3.4+).
```bash
pip --version
pip install package_name    # Install a library
pip list                    # Show installed packages
```

## **3. Optional (But Useful) Tools**

### **"Virtual Environments"**
Keeps projects separate (install later when needed).

```bash
# Create environment for python-- its like a dedicated zone for python
python -m venv venv

venv\Scripts\activate  # Activate (Windows)

source venv/bin/activate  # Activate (Mac/Linux)
```

**When to use:** Working on multiple projects.

---

### **VS Code Extensions** (If using VS Code)
1. Open VS Code
2. Go to Extensions (Ctrl+Shift+X)
3. Install **"Python"** by Microsoft

## **4. Troubleshooting**

### **"python: command not found"**
**Solution:** Python not in PATH.

**Windows:** Re-run installer, check "Add to PATH"  
**Mac/Linux:** Use `python3` instead of `python`

---

### **"pip: command not found"**
**Solution:**
```bash
python -m ensurepip --upgrade
```

> That's it. Gear up and Let's be Pythonic.
---

## **1. The Interpreter: Your Python Playground**

Python runs in two modes:

#### **Interactive Mode** (Instant Feedback)
```python
>>> 2 + 2
4
>>> name = "Alice"
>>> print(name)
Alice
```

#### **Script Mode** (Save & Run)
Write code in a `.py` file, then execute:

```python
# hello.py
print("Hello, World!")
```

Run it:
```bash
python hello.py
```

**What's happening:**

```
print         → Built-in function (already in Python)
  (...)       → Parentheses hold the input
"Hello..."    → String (text in quotes)
```

**Execution:**
```
1. Python sees print()
2. Looks inside parentheses
3. Finds the string "Hello, World!"
4. Sends it to the screen
```

*Simple, right? That's the point.*

---

## **Syntax: The Grammar Rules you will be grateful to later on**

### **Rule 1: Indentation = Structure**

Python uses **spaces** (not brackets) to show code blocks.

```python
# Correct
if True:
    print("This is inside")
    print("Still inside")
print("Now outside")

# Wrong
if True:
print("Where am I?")  # ERROR!
```

**The Standard:** 4 spaces per indent level (not tabs!).

> Here, Indentation isn't decoration—it's the bones of the code.

---

### **Rule 2: Case Sensitivity**

Python **cares about UPPERCASE vs lowercase**.

```python
name = "Alice"
Name = "Bob"    # Different variable!
NAME = "Charlie"  # Also different!

print(name)  # → Alice
print(Name)  # → Bob
```

**Remember:** `Print()` ≠ `print()` — Python won't recognize the former.

---

### **Rule 3: Comments (Notes to code readers)**

```python
# This is a comment — Python ignores it
x = 5  # Comments can go after code

"""
This is a multi-line comment
(also called a docstring)
"""
```

**Purpose:** Explain *why* you did something.

---

## **The Building Blocks: What Matters?**

### **1. Statements (Instructions)**

A statement is **one complete instruction**.

```python
x = 10           # Assignment statement
print(x)         # Function call statement
if x > 5:        # Conditional statement
    print("Big")
```

---

### **2. Expressions (Values)**

An expression **evaluates to a value**.

```python
5 + 3           # Expression → 8
"Hello" * 2     # Expression → "HelloHello"
x > 10          # Expression → True or False
```

**Key Difference:**
```python
x = 5      # Statement (does something)
5 + 3      # Expression (produces a value)
```

---

### **3. Keywords (Reserved Words) & Naming Conventions**

Python has **35 special words**. Here, one has to be specific about naming variables, functions or classes. 

```python
# These are KEYWORDS (don't use as names):
if, else, elif, for, while, def, return, 
True, False, None, and, or, not, in, is...
```


### **Variables & Functions:**
```python
# snake_case (lowercase with underscores)
user_name = "Alice"
total_price = 100

def calculate_tax():
    pass
```

### **Constants:**
```python
# UPPER_CASE
MAX_SPEED = 120
PI = 3.14159
```

### **Classes:**
```python
# PascalCase (capitalize each word)
class UserProfile:
    pass
```

---

## **So, the Priorities are:**

### **Priority 1: Indentation**
- Wrong indentation = code won't run. Period.

### **Priority 2: Syntax Accuracy**
Missing `:` after `if`, `for`, `def` = instant error.

```python
# Missing colon
if x > 5
    print("Big")

# Correct
if x > 5:
    print("Big")
```

### **Priority 3: Variable Names**
- Use descriptive names: `user_age` not `x`
- Follow conventions: `snake_case` for variables
- Avoid keywords: don't name something `list` or `str`

### **Priority 4: Comments**
- When code gets complex, **explain your thinking**.

---

## **Writing Your First Program**

```python
# 1. Comments (what this does)
# Calculate area of a rectangle

# 2. Variables (store data)
length = 10
width = 5

# 3. Expressions (calculate)
area = length * width

# 4. Output (show result)
print("Area:", area)
```
---

> *"The best way to learn Python? Write Python."* 👩🏻‍💻

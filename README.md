# AI-Based Static Code Analysis

## 📌 Project Overview

This project demonstrates **static code analysis for Python programs** using popular code-quality and security analysis tools.

The notebook analyzes a Python program containing intentional coding, security, and runtime issues. It then performs a review of the identified problems and creates a corrected version of the program.

The project uses:

* Flake8
* Pylint
* Bandit
* Python
* Google Colab / Jupyter Notebook

## 🎯 Objectives

The main objectives of this project are:

* Detect coding and style problems using Flake8.
* Analyze Python code quality using Pylint.
* Identify potential security issues using Bandit.
* Review bugs and security problems in the source code.
* Fix the identified issues.
* Run the analysis tools again on the corrected code.

## 🛠️ Technologies Used

| Technology   | Purpose                               |
| ------------ | ------------------------------------- |
| Python       | Programming language                  |
| Flake8       | Code style and linting                |
| Pylint       | Code quality analysis                 |
| Bandit       | Python security analysis              |
| Google Colab | Development and execution environment |

## 📂 Project Structure

```text
AI-Static-Code-Analysis/
│
├── static code-analysis (1).ipynb
└── README.md
```

When the notebook is executed, it also creates:

```text
sample.py
sample_fixed.py
```

## 🔍 Original Code

The notebook creates a file called `sample.py` containing:

```python
import os

password = "12345"

def divide(a,b):
    return a/b

print(divide(10,0))
```

This code intentionally contains several problems for analysis.

## ⚠️ Issues Identified

### 1. Bug

The program calls:

```python
divide(10,0)
```

This causes a **division-by-zero error**.

### 2. Security Issue

The program contains a hardcoded password:

```python
password = "12345"
```

Hardcoding credentials in source code is a security risk.

### 3. Code Quality Issues

The notebook identifies:

* Unused `os` import
* Missing comments
* Missing function docstring
* Formatting issues
* Lack of handling for division by zero

## 🔎 Static Analysis Tools

### Flake8

Flake8 is used to check Python code for style and linting problems.

```bash
flake8 sample.py
```

### Pylint

Pylint is used to analyze the quality and structure of the Python code.

```bash
pylint sample.py
```

### Bandit

Bandit is used to identify potential security vulnerabilities in Python code.

```bash
bandit -r sample.py
```

## 🤖 Code Review

The notebook performs a review covering three categories:

### Bug Analysis

* Division by zero occurs in `print(divide(10,0))`.

### Security Issues

* Hardcoded password found.

### Code Quality Issues

* Unused import `os`
* Missing comments
* Missing docstring

### Recommendations

* Remove unused imports.
* Avoid hardcoded credentials.
* Handle division-by-zero exceptions.

## ✅ Fixed Code

The notebook creates `sample_fixed.py`:

```python
def divide(a, b):
    if b == 0:
        return "Cannot divide by zero"
    return a / b

print(divide(10, 2))
```

The corrected program checks whether the divisor is zero before performing the division.

## 🔄 Validation

After creating `sample_fixed.py`, the notebook runs:

```bash
flake8 sample_fixed.py
```

```bash
pylint sample_fixed.py
```

```bash
bandit -r sample_fixed.py
```

This allows the corrected program to be checked again using the same static-analysis tools.

## 📊 Analysis Workflow

```text
Python Source Code
        ↓
      Flake8
        ↓
      Pylint
        ↓
      Bandit
        ↓
   Code Review
        ↓
Identify Problems
        ↓
   Fix the Code
        ↓
 Re-run Analysis
```

## 📚 Learning Outcomes

This project demonstrates:

* Static code analysis
* Python linting
* Code-quality checking
* Security vulnerability detection
* Bug identification
* Secure coding practices
* Code improvement and validation

## 🚀 How to Run

### Step 1: Open the Notebook

Open:

```text
static code-analysis (1).ipynb
```

in Google Colab or Jupyter Notebook.

### Step 2: Install the Tools

Run:

```python
!pip install pylint flake8 bandit
```

### Step 3: Run the Cells

Execute the notebook cells in order.

The notebook will:

1. Create `sample.py`.
2. Run Flake8.
3. Run Pylint.
4. Run Bandit.
5. Display the source code.
6. Perform the code review.
7. Create `sample_fixed.py`.
8. Run the analysis tools again on the fixed code.

## 👩‍💻 Author

**Dharshini A**

## 📌 Project Type

**Python Static Code Analysis / AI-Assisted Code Review**

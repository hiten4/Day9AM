# Day9AM

# Student Management & Python Concepts Assignment

## Overview
This project demonstrates core Python programming concepts through multiple tasks including data structures, matrix operations, algorithmic problem solving, and AI-assisted coding analysis.

---

# Part A — Student Management System

A simple **CLI-based Student Management System** was implemented using Python.

### Key Features
- Student records stored as **list of lists**
- Functions implemented:
  - `add_student(name, subject, marks)` – adds student records and prevents duplicates
  - `get_toppers(subject)` – returns top 3 students using sorting
  - `class_average(subject)` – calculates subject average using list comprehension
  - `above_average_students()` – finds students scoring above overall average
  - `remove_student(name)` – removes all records for a student using filtering
- **Menu driven interface**
- Data saved to **students.txt** using file I/O when program exits

### Python Concepts Demonstrated
- Lists and nested lists  
- `append()`  
- `sorted()` with `lambda`  
- List comprehensions  
- Slicing  
- File read/write  

---

# Part B — Matrix Operations Module

A module **matrix_ops.py** was created to perform basic matrix operations using lists.

### Implemented Functions
- `matrix_add(A, B)`  
  Performs element-wise matrix addition.

- `matrix_transpose(matrix)`  
  Computes transpose using nested list comprehension.

- `matrix_multiply(A, B)`  
  Performs matrix multiplication using dot product logic.

### Example Output

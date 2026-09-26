# Day 7 – Student Information Dictionary

## Project Overview
A Python project that stores student information in dictionaries and implements **search, add, and update** operations.

## Objective
Practice dictionaries and structured data representation.

## Tools
- Python
- Jupyter Notebook

## Features
- Store student records with unique IDs
- Display records
- Search by student ID
- Add a student
- Update marks or course
- Handle duplicate/non-existing IDs

## Project Structure
```text
Day7_Student_Information_Dictionary/
├── Student_Information_Dictionary.ipynb
├── Student_Information_Dictionary.py
├── README.md
└── Day_7_Student_Information_Dictionary_Report.pdf
```

## Dictionary Structure
```python
"S101": {
    "name": "Ananya Sharma",
    "age": 20,
    "course": "Computer Science",
    "marks": 85
}
```

## Operations
1. **Display** – Shows all records using a loop.
2. **Search** – Finds a record using its unique ID.
3. **Add** – Adds a new record if the ID is available.
4. **Update** – Changes existing marks or course.

## Complete Code
```python
# Day 7: Student Information Dictionary

students = {
    "S101": {"name": "Ananya Sharma", "age": 20, "course": "Computer Science", "marks": 85},
    "S102": {"name": "Rahul Kumar", "age": 21, "course": "Information Science", "marks": 78},
    "S103": {"name": "Priya Patil", "age": 20, "course": "Artificial Intelligence", "marks": 91}
}

def display_students():
    print("\nSTUDENT INFORMATION")
    print("=" * 50)
    for student_id, details in students.items():
        print("Student ID:", student_id)
        print("Name:", details["name"])
        print("Age:", details["age"])
        print("Course:", details["course"])
        print("Marks:", details["marks"])
        print("-" * 50)

def search_student(student_id):
    print("\nSEARCH STUDENT")
    if student_id in students:
        print(students[student_id])
    else:
        print("Student not found.")

def add_student(student_id, name, age, course, marks):
    if student_id in students:
        print("Student ID already exists.")
    else:
        students[student_id] = {
            "name": name, "age": age, "course": course, "marks": marks
        }
        print("Student added successfully.")

def update_student(student_id, marks=None, course=None):
    if student_id in students:
        if marks is not None:
            students[student_id]["marks"] = marks
        if course is not None:
            students[student_id]["course"] = course
        print("Student information updated successfully.")
    else:
        print("Student not found.")

display_students()
search_student("S102")
add_student("S104", "Sneha Rao", 21, "Data Science", 88)
update_student("S103", marks=94)
display_students()

```

## Example Results
- Search `S102` → Rahul Kumar's record is displayed.
- Add `S104` → Sneha Rao is added.
- Update `S103` → Marks are changed from 91 to 94.

## Key Concepts
- Dictionaries
- Key-value pairs
- Nested dictionaries
- `in` operator
- Functions
- Loops
- Conditional statements
- Adding and updating dictionary values

## Interview Questions

**1. What is a dictionary in Python?**  
A mutable data structure that stores data as key-value pairs.

**2. Why are keys important?**  
Keys uniquely identify values and allow the associated data to be accessed.

**3. How is a dictionary different from a list?**  
A list stores ordered elements mainly accessed by index, while a dictionary stores key-value pairs accessed by keys.

## Conclusion
The project demonstrates how Python dictionaries can be used to represent structured student data and perform basic record-management operations.

**Internship:** AI & ML Track  
**Task:** Day 7 – Student Information Dictionary  


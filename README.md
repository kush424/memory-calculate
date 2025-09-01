# Student Management System (Vector + Template)

A simple C++ console app to manage students using a template class and a vector. It supports adding, listing, searching, and removing students by ID.

## Features
- Add a student (ID + Name)
- Display all students
- Search a student by ID
- Remove a student by ID
- Uses:
  - std::vector for dynamic storage
  - A class template MemoryCalculate<T1, T2> for student data

## Tech/Requirements
- Language: C++11 or later
- Compiler: g++ or clang++
- Single source file: main.cpp (save your code into this file)


## How to Use
Menu options:
- 1: Add Student (enter integer ID, then Name as a single word)
- 2: Display All Students
- 3: Remove Student by ID
- 4: Search Student by ID
- 5: Exit

Note:
- Current input for Name uses cin >> name, so it accepts a single word only (e.g., "Kush”, not “Kush Patel”).

## Example Session
```
--- Student Management System ---
1. Add Student
2. Display All Students
3. Remove Student by ID
4. Search Student by ID
5. Exit
Enter your choice: 1
Enter ID: 101
Enter Name: Ali
 
--- Student Management System ---
1. Add Student
2. Display All Students
3. Remove Student by ID
4. Search Student by ID
5. Exit
Enter your choice: 2

List of Students:
ID: 101 | Name: Ali

--- Student Management System ---
Enter your choice: 4
Enter ID to search: 101
Student Found: ID: 101 | Name: Ali

--- Student Management System ---
Enter your choice: 3
Enter ID to remove: 101
Student with ID 101 removed.

--- Student Management System ---
Enter your choice: 2
No students available.
```

## Code Overview

- Template class: MemoryCalculate<T1, T2>
  - Attributes: id (T1), name (T2)
  - Methods:
    - Constructor to set id and name
    - display() to print details
    - getId() to access ID

- Management class: StudentManagement
  - Stores a vector<MemoryCalculate<int, string>>
  - Methods:
    - addStudent(int id, string name)
    - displayAll()
    - removeStudent(int id)
    - searchStudent(int id)

- main()
  - Provides a loop with a menu to call the above operations

## How This Meets the Assignment
- Uses a Vector and a Template as required.
- Implements:
  - Add student (push_back)
  - Display all students (iterate vector)
  - Remove student by ID (search + erase)
  - Search student by ID (search + display)

## Assumptions & Limitations
- Names are read as a single word (no spaces). To allow spaces, replace the name input with getline and clear the buffer.
- IDs are integers; duplicates are not prevented.
- Basic input validation only (non-integer input may cause issues).

## Testing Ideas
- Add two students and display all.
- Search for an existing and a non-existing ID.
- Remove a student, then try removing again.
- Display when list is empty.

-----
<img width="582" height="886" alt="image" src="https://github.com/user-attachments/assets/9cf04d6e-585e-4f74-88ab-fce67df42d73" />
<img width="347" height="306" alt="image" src="https://github.com/user-attachments/assets/147fac45-c7fc-41b4-b3d9-663caae295da" />

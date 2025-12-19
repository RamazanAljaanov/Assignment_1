Overview

The project includes three main source files:
`Student.java` — represents a student with fields and basic operations.
`Course.java` — represents a course which contains a fixed-size array of `Student` objects.
`Main.java` — driver program that pre-populates data, shows required calculations, and provides a minimal interactive menu.
 
Student.java — explanation

Purpose:
- Encapsulates student data and simple operations.

Fields (private):
`name` — student's full name (String)
`id` — student identifier (String)
`major` — academic program (String)
`gpa` — current GPA (double)
`credits` — total earned credits (int)

Constructor:
`Student(String name, String id, String major)`
Initializes `name`, `id`, and `major`. If `null` is provided, it uses an empty string.
Sets `gpa = 0.0` and `credits = 0`.

Getters:
`getName()`, `getId()`, `getMajor()`, `getGpa()`, `getCredits()`

Setters:
`setName(String)`, `setId(String)`, `setMajor(String)` 
----------------------------------------------------------

Fields (private):
`courseName` — name of the course
`instructor` — instructor name
`students` — fixed-size `Student[]` array

Constructor:
`Course(String courseName, String instructor, int size)`
If `courseName` or `instructor` is `null`, empty string is used.
Ensures `size` is at least 1 (if passed size is less than 1, size defaults to 1).

Add / insert methods:
`boolean addStudent(Student s, int index)`
Attempts to add a student at the given index.
Returns `true` if the student was placed, `false` if the index is invalid, slot is occupied, or `s` is `null`.
This method does not overwrite an occupied slot.
`boolean addStudent(Student s)`
Finds the first free slot and inserts the student.
Returns `true` if inserted; `false` if the course is full or `s` is `null`.

Processing methods:
`double courseAverageGPA()` — computes average GPA of non-null students (returns 0.0 if no students).
`Student highestCreditStudent()` — returns the student with the most credits (or `null` if none).

Other:
`toString()` — summarizes course info and lists each slot (student or `<empty>`).
`getStudents()` — returns the internal array (simple accessor in this simplified version).

Main flow:
1. Create a `Student[]` array (capacity 20).
2. Pre-populate 5 students and set their GPA and credits (this ensures the driver demonstrates required operations on startup).
3. Create a `Course` object and enroll the initial 5 students using `addStudent(Student)`.
4. Print initial course summary and the array-processing results (top GPA, honors count, total credits).

------------------------------------------------------------------------------------------------------------------------------------------
![img.png](img.png)
![img_1.png](img_1.png)


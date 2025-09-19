# Student Records Database Management System

## 📌 Introduction
This project implements a **Student Records Database Management System** using **MySQL**.  
The system manages essential information about students, departments, lecturers, courses, enrollments, and grades.  

It demonstrates relational database concepts such as:
- Primary Keys
- Foreign Keys
- Unique Constraints
- One-to-One, One-to-Many, and Many-to-Many Relationships

---

## 📂 Database Schema

### Tables
- **Departments**: Stores information about academic departments.
- **Students**: Stores student personal and academic details.
- **Lecturers**: Stores lecturer details.
- **Courses**: Stores course information.
- **Enrollments**: Junction table managing many-to-many relationships between Students and Courses.
- **Grades**: Stores performance/grade data for students in specific courses.

---

## 🔗 Relationships

1. Departments → Students (One-to-Many)
Relationship: One department can have many students
Cardinality: 1:N

2. Departments → Lecturers (One-to-Many)
Relationship: One department can have many lecturers
Cardinality: 1:N

3. Departments → Courses (One-to-Many)
Relationship: One department can offer many courses
Cardinality: 1:N

4. Lecturers → Courses (One-to-Many)
Relationship: One lecturer can teach many courses
Cardinality: 1:N

5. Students ↔ Courses (Many-to-Many via Enrollments)
Relationship: Many students can enroll in many courses
Enrollments table connects Students and Courses
Cardinality: M:N

6. Enrollments → Grades (One-to-One/One-to-Many)
Relationship: Each enrollment can have one grade (assuming one grade per enrollment)
Cardinality: 1:1 (or 1:N if multiple grades per enrollment are allowed)

#Entity Relationship Diagram

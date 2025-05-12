# Experiment 1: Entity-Relationship (ER) Diagram

## 🎯 Objective:
To understand and apply the concepts of ER modeling by creating an ER diagram for a real-world application.

## 📚 Purpose:
The purpose of this workshop is to gain hands-on experience in designing ER diagrams that visually represent the structure of a database including entities, relationships, attributes, and constraints.

---

## 🧪 Choose One Scenario:

### 🔹 Scenario 1: University Database
Design a database to manage students, instructors, programs, courses, and student enrollments. Include prerequisites for courses.

**User Requirements:**
- Academic programs grouped under departments.
- Students have admission number, name, DOB, contact info.
- Instructors with staff number, contact info, etc.
- Courses have number, name, credits.
- Track course enrollments by students and enrollment date.
- Add support for prerequisites (some courses require others).

---

### 🔹 Scenario 2: Hospital Database
Design a database for patient management, appointments, medical records, and billing.

**User Requirements:**
- Patient details including contact and insurance.
- Doctors and their departments, contact info, specialization.
- Appointments with reason, time, patient-doctor link.
- Medical records with treatments, diagnosis, test results.
- Billing and payment details for each appointment.

---

## 📝 Tasks:
1. Identify entities, relationships, and attributes.
2. Draw the ER diagram using any tool (draw.io, dbdiagram.io, hand-drawn and scanned).
3. Include:
   - Cardinality & participation constraints
   - Prerequisites for University OR Billing for Hospital
4. Explain:
   - Why you chose the entities and relationships.
   - How you modeled prerequisites or billing.

# ER Diagram Submission - Student Name

## Scenario Chosen:
University

## ER Diagram:
![er_diagram](https://github.com/user-attachments/assets/7c47b51d-a7b5-4c5b-8273-ba11ccdf46fe)


## Entities and Attributes:
- College: (College Code, City, Head)
- Department: (Scope, Block, Maximum Admission)
- Staff: (Staff ID, Address, Salary)
- Student: (Register Number, Name, Mobile Number)
- Parent: (Contact Number, Relationship, Name)
- Course: (Code, Maximum Capacity, Credits)

...

## Relationships and Constraints:
- Works in a (Staff → Department): One-to-Many relationship; each staff member belongs to a single department, but a department can have multiple staff members.
- Belongs (Department → College): Many-to-One relationship; each department belongs to a college.
- Choose (Student → Course): Many-to-Many relationship; students can enroll in multiple courses, and courses have multiple students.
- Handle (Staff → Course): Many-to-Many relationship; instructors handle multiple courses.
- Collect fee from (University → Parent): Indicates student fees collected through parent associations.
...

## Extension (Prerequisite):
- Requires (Course → Course) with One-to-Many mapping (a course can have multiple prerequisites).
- An additional table Prerequisite can store (Course ID, Prerequisite ID).

## Design Choices:
- Departments are grouped under Colleges to maintain hierarchy.
- Course prerequisites enable structured learning paths.
- Enrollments link students to courses with timestamps.
- Cardinality constraints prevent inconsistencies (e.g., a course cannot have infinite capacity).

## RESULT
The concepts of ER modeling is applied by creating an ER diagram for real-world application.

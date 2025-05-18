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
University / Hospital (choose one)

## ER Diagram:
![image](https://github.com/user-attachments/assets/449ac0bd-3d77-4303-a81e-fe79649861ca)


## Entities and Attributes:

Entities and their attributes:

1. Doctor – Name, Address, Specialization, Qualification

2. Patient – Details

3. Treat – Date, Disease, Treatment (links Doctor and Patient)

4. Log – Date (linked to Patient)

5. Report – Linked to Log

6. Test – Type, Description (linked to Report)
...

## Relationships and Constraints:

## RELATIONSHIP:

1.Doctor–Patient have a many-to-many relationship through Treat, with attributes: Date, Disease, Treatment.

2.Patient–Log has a one-to-many relationship; a patient can have multiple logs.

3.Log–Report is one-to-one; each log links to one report.

4.Report–Test is one-to-one; each report is associated with one test.


## CONSTRAINTS:

1.A doctor can treat many patients, and vice versa.

2.Each patient can have multiple logs.

3.Each report must be linked to one test.
...

## Extension (Prerequisite / Billing):

## Prerequisite:
This is a recursive relationship within the Test entity, where one test may require another test to be done first. It ensures proper sequencing of medical tests. For example, an advanced test might need a basic test as a prerequisite. This forms a one-to-many relationship, as one test can have multiple prerequisites.


## Billing:
The Billing entity is used to manage financial records related to a patient’s treatments or tests. It is associated with either Patient or Report. It includes attributes like Bill ID, Amount, Date, and Payment Status. A single patient can have multiple bills, forming a one-to-many relationship. This helps in tracking payment details and generating invoices.

## Design Choices:

1.The design follows a real-world healthcare model to manage doctor-patient interactions, treatments, tests, and billing.

2.Entities like Doctor, Patient, Test, and Billing represent key components of a hospital system.

3.Treat is used as an associative entity to handle the many-to-many relationship between doctors and patients with treatment details.

4.Log and Report capture patient history and test outcomes.

5.A recursive relationship in Test handles prerequisites.

6.Billing ensures financial tracking.

This design supports scalability, data consistency, and efficient patient management.

## RESULT

 Thus, the SQL queries to implement ER Diagram using hospital management have been executed successfully

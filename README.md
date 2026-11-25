Hospital Management System – C Programming
Project Overview

The Hospital Management System is a console-based application developed using the C programming language as part of the Programming Fundamentals (PF) project.

The application is designed to simplify basic hospital administration by managing patient records, doctor assignments, hospital bed availability, and billing operations.

It uses structures, arrays, functions, conditional statements, loops, and file handling to implement a complete menu-driven management system. It also features illness-based doctor assignment and role-based authentication, providing separate access for administrators and regular users.


Objectives
Develop a practical application using fundamental C programming concepts.
Manage patient and doctor records using structures.
Implement hospital bed allocation and availability tracking.
Automate doctor assignment based on patient illness.
Calculate patient bills based on hospital charges.
Use file handling for persistent data storage.
Implement authentication with separate admin and user access.

Technologies Used
Programming Language: C
Data Organization: Structures and Arrays
File Handling: C File I/O (stdio.h)
String Handling: string.h
Standard Libraries: stdio.h, stdlib.h, string.h
Development Environment: Dev-C++ / GCC / Visual Studio

Key Features
1. User Authentication

Implements a basic authentication system with separate administrative and user access.

Admin Credentials:

Username: admin
Password: admin123

User Credentials:

Username: user
Password: user123
Validates username and password.
Provides separate menus according to user roles.
Restricts administrative operations to authenticated administrators.
2. Patient Registration

Allows administrators to register new patients by entering:

Patient name
Age
Gender
Illness
Days of stay
Service charges
Doctor fee

The system automatically assigns an appropriate doctor and an available hospital bed.

3. Doctor Management and Automatic Assignment
Loads doctor information from doctors.txt.
Stores doctor names and specializations using structures.
Determines the appropriate medical specialization based on the patient's illness.
Automatically assigns a doctor with a matching specialization.
Provides General Practitioner as a fallback when no matching specialist is available.

Supported Medical Specializations:

Cardiology
Neurology
Orthopedics
Pediatrics
Oncology
Dermatology
Gastroenterology
Psychiatry
Urology
General Medicine
4. Hospital Bed Management
Maintains a maximum of 20 hospital beds.
Uses an integer array to track bed availability.
Automatically assigns the first available bed.
Marks beds as occupied when a patient is registered.
Frees beds when patients are discharged.
Displays the real-time availability of all hospital beds.
5. Patient Record Management
Stores patient details using a Patient structure.
Maintains a collection of patient records using an array.
Displays all registered patients.
Shows patient information, assigned doctor, bed number, and total bill.
Supports a maximum of 100 patient records.
6. Billing System

Automatically calculates patient bills based on their stay duration and additional charges.

Billing Formula:

Total Bill = (Days of Stay × 500) + Service Charges + Doctor Fee

Uses a fixed room rate of 500 per day.
Includes service charges and doctor fees.
Allows administrators to generate bills by searching for patient names.
Displays a detailed billing summary.
7. Patient Removal
Searches for patients using their names.
Removes discharged patient records.
Releases the patient's assigned bed.
Shifts remaining records to maintain a compact patient array.
Updates patient and bed information in their respective files.
8. File Handling and Data Persistence

The application uses three text files to maintain hospital records.

File	Purpose
patients.txt	Stores complete patient records
beds.txt	Stores bed availability information
doctors.txt	Stores doctor names and specializations
Loads patient information when the application starts.
Saves updated patient records after registration and removal.
Maintains bed availability between program executions.
Loads doctor information from an external file.


Programming Concepts Implemented
Concept	Application
Structures	Patient and Doctor records
Arrays	Patient, doctor, and bed storage
Functions	Modular program implementation
File Handling	Loading and saving hospital data
String Handling	Searching names and matching illnesses
Conditional Statements	Authentication and doctor assignment
Loops	Patient processing and menu navigation
Pointers	File handling and string operations
Switch Statements	Menu-driven functionality


How the Application Works
The application loads existing patient records from patients.txt.
Bed availability is restored from beds.txt.
Doctor information is loaded from doctors.txt.
The user enters a username and password.
The system authenticates the user and displays the corresponding menu.
Administrators can register patients, view records, manage beds, generate bills, and remove discharged patients.
Regular users can view bed availability.
Updated patient and bed information is saved to the respective files.

Admin Menu
Add Patient
View All Patients
View Bed Availability
Generate Bill
Remove Patient
Exit

User Menu
View Bed Availability
Exit

Required Project Files
Hospital-Management-System/
│
├── main.c
├── patients.txt
├── beds.txt
├── doctors.txt
└── README.md


Important: The doctors.txt file must contain doctor names and specializations in the following format:

Dr. Cardio, Cardiology
Dr. Neuro, Neurology
Dr. Ortho, Orthopedics
Dr. Peads, Pediatrics
Dr. Onco, Oncology
Dr. Derma, Dermatology
Dr. Gastro, Gastroenterology
Dr. Psyc, Psychiatry
Dr. Uro, Urology
Dr. General, General Medicine


How to Run

Requirements: GCC or another C compiler.

Compile using GCC:
gcc main.c -o HospitalManagement

Make sure doctors.txt is available in the application's working directory before execution. The patient and bed files are initialized automatically if they do not already exist.


Learning Outcomes
Understanding fundamental C programming concepts.
Working with structures and arrays.
Developing modular programs using functions.
Implementing file handling for persistent storage.
Applying string manipulation and searching techniques.
Understanding basic authentication and role-based access.
Developing a practical record management application.


Future Improvements
Add password encryption and stronger authentication.
Introduce a graphical user interface.
Support multiple doctors for the same specialization.
Improve patient search and record management.
Add appointment scheduling.
Implement more flexible hospital billing rates.
Improve input validation and file error handling.

Project: Hospital Management System
Language: C
Course: Programming Fundamentals (PF)

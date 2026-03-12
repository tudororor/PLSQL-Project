# 🕺 Groove Station – Advanced Database Management System

## 📌 Project Overview
**Groove Station** is a robust database solution designed to manage a large-scale network of dance studios. The system centralizes critical data regarding physical resources (studios, rooms), administrative and technical personnel (managers, instructors), clients, enrollments, and strategic partnerships (sponsorships).

This project was developed at the Faculty of Mathematics and Computer Science, University of Bucharest.

## 🏗️ System Architecture
The database architecture follows **Third Normal Form (3NF)** standards and consists of **13 interconnected tables**:
* **Core Entities:** STUDIO, SALA (Room), MANAGER, ANTRENOR (Instructor), CLIENT, STILDANS (Dance Style).
* **Relationship Entities:** PROGRAMARE (Schedule), SPONSOR, and multiple associative tables to handle Many-to-Many relationships.

## 🚀 Key Technical Features

### 🔹 Advanced Data Structures (PL/SQL Collections)
Implemented reporting procedures that utilize all three types of Oracle collections:
* **VARRAY:** For managing standard difficulty levels.
* **Nested Tables:** For collecting and processing high volumes of course data.
* **Associative Arrays:** For generating fast, indexed statistics.

### 🔹 Intelligent Logistics Reporting
A hierarchical reporting system using **Parameterized Cursors** dependent on explicit cursors to map the logistics of each studio, linking rooms to their specific scheduled sessions.

### 🔹 Business Logic & Validation (Triggers)
Data integrity is enforced through advanced database triggers:
* **Command-Level DML:** Restricts instructor deletions to preserve professional historical data.
* **Row-Level DML:** Prevents scheduling sessions in the past to maintain calendar integrity.
* **DDL Trigger:** Blocks accidental table deletions (DROP), protecting the overall database schema.

### 🔹 Granular Exception Handling
Subprograms include detailed error management, handling both predefined Oracle exceptions (NO_DATA_FOUND, TOO_MANY_ROWS) and user-defined exceptions for specific business scenarios.

## 💻 Tech Stack
* **Database Engine:** Oracle Database 21c
* **Operating System:** Windows 11
* **IDE:** DataGrip

---
*Developed by **Tudor-Mihail Dănilă**.*

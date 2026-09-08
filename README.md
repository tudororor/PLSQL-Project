# Groove Station – Relational Database Management System

## Overview
Groove Station is a relational database system designed to model and manage the operational workflows of a dance studio network[cite: 1]. The schema centralizes information about physical infrastructure (studios, halls), staff (managers, instructors), clientele, class enrollments, and corporate sponsorships[cite: 1].

Developed as coursework for the Database Management Systems (DBMS) curriculum at the Faculty of Mathematics and Computer Science, University of Bucharest[cite: 1].

## Relational Architecture
The database design adheres to Third Normal Form (3NF) and contains 13 interconnected tables[cite: 1]:
* **Core Entities:** `STUDIO`, `SALA`, `MANAGER`, `ANTRENOR`, `CLIENT`, `STILDANS`
* **Associative & Relationship Entities:** `PROGRAMARE`, `SPONSOR`, along with junction tables resolving Many-to-Many relationships[cite: 1]

## Core Features & Implementations

### PL/SQL Collections & Processing
Data aggregation workflows leverage all three primary Oracle collection types[cite: 1]:
* **VARRAY:** Configured for bounded sets of standard difficulty tiers[cite: 1].
* **Nested Tables:** Used in dynamic querying and batch processing of enrollment records[cite: 1].
* **Associative Arrays (Index-by Tables):** Employed for memory-efficient data lookup and statistical summaries[cite: 1].

### Cursors & Logistics Querying
The reporting logic utilizes parameterized cursors dependent on master explicit cursors to navigate relational hierarchies (e.g., mapping studios to individual rooms and their respective schedules)[cite: 1].

### Integrity Constraints & Triggers
Business logic enforcement and audit controls are automated via DML and DDL triggers[cite: 1]:
* **Statement-level DML Trigger:** Prevents deletion of instructor records to maintain historical operational logs.
* **Row-level DML Trigger:** Enforces temporal validity by rejecting past-dated session bookings.
* **System/DDL Trigger:** Intercepts `DROP` statements to prevent unauthorized table dropping and schema corruption[cite: 1].

### Error Handling
Procedures and functions incorporate granular exception blocks, capturing standard Oracle errors (`NO_DATA_FOUND`, `TOO_MANY_ROWS`) as well as user-defined business exceptions via `RAISE_APPLICATION_ERROR`[cite: 1].

## Environment
* **RDBMS:** Oracle Database 21c[cite: 1]
* **Language:** SQL, PL/SQL[cite: 1]
* **Development Environment:** DataGrip / SQL Developer

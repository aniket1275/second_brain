---
title: Database Schema
draft: false
tags:
  - DBMS
---
A schema is not just a “design” in a vague sense — it’s the formal blueprint of how data is organized in a database. It defines:

- what tables exist
- what columns they have
- data types
- relationships between tables
- constraints (rules)

Think of it like the architecture plan of a building — before you build anything, you decide rooms, structure, connections, etc.

### Simple Example is 

Let’s say you’re building a college database.

Schema might look like:

Table: Students
- student_id (INT, PRIMARY KEY)
- name (VARCHAR)
- age (INT)

Table: Courses
- course_id (INT, PRIMARY KEY)
- course_name (VARCHAR)
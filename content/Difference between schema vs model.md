---
title: Difference between schema vs model
draft: false
tags:
  - DBMS
  - Schema
  - Models
---
Difference between the view and model?

here is analogy for the model and schema which help understand better and also their differences.

## Model

Model is concept how to describe the data.

"Think of the model as Architecture style like traditional, modern."

Ex : 
- Relation model ( The model in which we create the table from row [data] and  column [attributes] also we represent relationship between the tables ). Used in MYSQL like DB.

- Document-Object model ( The model in which we create the document contain data and collections is multiple documents ). Used in the MongoDB.

## Schema

Schema is actual design created using model.

"Think of the schema as using model define the exact design like how many rooms, floors, collection between rooms."

Ex : 

- CREATE TABLE Students (
    student_id INT PRIMARY KEY,
    name VARCHAR(50),
    age INT
  );



---
layout: default
title: Relational Database Management Systems
nav_order: 2.3
parent: Introduction to SQL
---
# Relational Database Management Systems
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## What is a database management system?
- **Database** -- logically modelled clusters of information/data
- **Database management system (DBMS)** -- a computer program that interacts with a database
- Every DBMS has an underlying model that structures how data are stored and accessed. 
    - e.g. relational database management system (RDBMS) &larr; relational data model

## What is a relational database management system?
- Relational -- data are organised into tables. 
- Tables = relations 
- A **relation** is a set of tuples.
- A **tuple** is a row in a table. 
- Each tuple shares a set of attributes.
- An **attribute** is a column in a table. 

## Variations of SQL for RDBMSs
- SQL is used to manage and query data from relational databases. 
- Many RDBMSs use their own particular dialect of SQL. 
- The standard SQL exists. 
    - SQL standards are jointly maintained by the American National Standards Institute (ANSI), the International Organisation for Standardisation (ISO), and the International Electrotechnical Commission (IEC). 

## Constraints for RDBMSs
Database administrator impose constraints on a table to limit what values can be entered into it. A constraint typically applies to one particular column. Some constraints can apply to an entire table. Commonly used constraints include:

- `UNIQUE`: to ensure that no two entries in a column are identical
- `NOT NULL`: to ensure that a column doesn’t have any `NULL` entries
- `PRIMARY KEY`: a combination of `UNIQUE` and `NOT NULL`
- `FOREIGN KEY`: A `FOREIGN KEY` is a column in one table that refers to the `PRIMARY KEY` of another table. 
    - to link two tables together
    - Entries to the `FOREIGN KEY` column must already exist in the parent `PRIMARY KEY` column for the write process to succeed.
- `CHECK`: to limit the range of values that can be entered into a column
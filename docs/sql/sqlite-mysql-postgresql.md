---
layout: default
title: Popular Open-Source RDBMSs
nav_order: 2.4
parent: Introduction to SQL
has_children: true
has_toc: false
---
# Popular Open-Source RDBMSs
{: .no_toc }

SQLite, MySQL and PostgreSQL are the most widely implemented open-source RDBMSs nowadays. Here we will look into how each of them specialises in a different type of task. 
{: .fs-6 .fw-300 }

---

## Server-Based Databases vs. Serverless Databases

| Server-Based | Serverless |
| --- | --- |
| <span style="display: inline-block; width:340px">- database engines implemented as a server process <br> - allow programs to communicate with the host server <br> - an interprocess communication that relays requests <br> - e.g. mySQL and PostgreSQL</span> | <span style="display: inline-block; width:340px">- interact (access, read, and write) with the database disk file directly <br> - e.g. SQLite</span> |


## Data Types
A comprehensive list of data types used in varous relational databases can be found [here](https://www.w3schools.com/sql/sql_datatypes.asp). Here we provide a brief summary of the data types supported by SQLite, MySQL and PostgreSQL, respectively:

| SQLite | MySQL | PostgreSQL |
| --- | --- | --- |
| <span style="display: inline-block; width:210px">- `null` <br> - `integer`: signed integers <br> - `real` <br> - `blob`: Binary Large Objects</span> | <span style="display: inline-block; width:210px">- several numerical types <br> - several date and time types <br> - several string types</span> | <span style="display: inline-block; width:210px">- in addition to numeric, string, and date and time <br> - also supports geometric shapes, network addresses, bit strings, text searches, JSON entries</span> |


## SQLite
- a serverless database
- hence simplified setup process
    - no need to configure a server process
    - all that is needed is access to the disk










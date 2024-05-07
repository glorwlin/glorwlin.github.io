---
layout: default
title: Popular Open-Source RDBMSs
nav_order: 10.4
parent: Introduction to SQL
has_children: true
has_toc: false
---
# Popular Open-Source RDBMSs
{: .no_toc }

SQLite, MySQL and PostgreSQL are the most widely implemented open-source RDBMSs nowadays. Here we will look into how each of them specialises in a different type of task. 
{: .fs-6 .fw-300 }

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Server-Based Databases vs. Serverless Databases

| Server-Based | Serverless |
| --- | --- |
| <span style="display: inline-block; width:340px">- database engines implemented as a server process <br> - allow programs to communicate with the host server <br> - an interprocess communication that relays requests <br> - e.g. mySQL and PostgreSQL</span> | <span style="display: inline-block; width:340px">- interact (access, read, and write) with the database disk file directly <br> - e.g. SQLite</span> |

---

## Data Types
A comprehensive list of data types used in varous relational databases can be found [here](https://www.w3schools.com/sql/sql_datatypes.asp). Here we provide a brief summary of the data types supported by SQLite, MySQL and PostgreSQL, respectively:

| SQLite | MySQL | PostgreSQL |
| --- | --- | --- |
| <span style="display: inline-block; width:230px">- `null` <br> - `integer`: signed integers <br> - `real` <br> - `blob`: Binary Large Objects</span> | <span style="display: inline-block; width:230px">- several numerical types <br> - several date and time types <br> - several string types</span> | <span style="display: inline-block; width:230px">- in addition to numeric, string, and date and time <br> - also supports geometric shapes, network addresses, bit strings, text searches, JSON entries</span> |

---

## SQLite
- a serverless database

### Pros

Lightweight
: SQLite can take up very little disk space and operate without external dependencies.

Easy to use
: SQLite is not a server process. There is no need to go through steps associated with server processes, e.g. starting/stopping/restarting the process and managing configuration files.

Portable
: An entire SQLite database is stored in a single file, whereas other DBMSs typically store data as a large batch of separate files. Hence, SQLite projects can be easily shared. 

### Cons

Limited concurrency
: - Concurrency – the ability of two transactions to use the same data at the same time
: - Multiple processes can access and query an SQLite database, but only one process can make changes to the database at any given time.

No user management
: SQLite allows users to read and write directly to disk, which is poor for applications that require multiple users with special access permissions. 

Security
: Being serverless may not be able to shield the database from bugs in the client application. Server database can control data access with more precision.

---

## MySQL
- the most popular relational database since 2012
- powers many of world’s largest websites and applications like Twitter, Facebook, Netflix, and Spotify
- exhaustive documentation and large community of developers available
- peed and reliability at the expense of full adherence to standard SQL

### Pros

Popularity & ease of use
: There are experienced data administrators in the job market and abundant support online. 

Security
: MySQL supports user management, as opposed to SQLite.

Replication
: MySQL supports setting up a database backup solution and horizontally scaling a database.

### Cons

Functional limitations
: MySQL does not fully support standard SQL.

Licensing and proprietary features
: MySQL is dual-licensed with (1) free, open-source edition licenced under GPLv2 and (2) commercial editions released under proprietary licenses. Some features and plugins are only available for the proprietary editions. 

Slowed development
: Oracle’s acquisition of Sun resulted in slowed development process and led to lack of agile responses to problems. 

---

## PostgreSQL

### Pros

SQL compliance
: PostgreSQL closely adheres to SQL standards.

Open-source & community-driven
: PostgreSQL is fully open-source with abundant online resources available. 

Extensible
: It is possible to extend PostgreSQL programmatically and on the fly.

### Cons

Memory performance
: Each new process is allocated about 10MB of memory, hence, PostgreSQL is not ideal for simple read-heavy operations. 

Not as popular as MySQL
: Fewer third-party tools can help manage a PostgreSQL database. There are not as many experienced database administrators available (as is the case for MySQL). 

---

## How to choose among SQLite, MySQL, and PostgreSQL?
Here is a list of questions that you may ask yourself/your team/your clients before deciding on the RDBMS for a specific project. 

**<mark>1. Are you working with a big amount of data?</mark>**
- Yes &rarr; maybe **not SQLite** (poor when used to work with data exceeding 1TB)

**<mark>2. What is your database setup?</mark>**
- A simple setup that allows one to read/write to the disk directly &rarr; consider **SQLite**
- A distributed database setup &rarr; consider **MySQL**

**<mark>3. How important is it to maintain data integrity in this project?</mark>**
- Very important &rarr; consider **PostgreSQL**

**<mark>4. What are the types of operations needed?</mark>**
- Simple operations and quick tests &rarr; consider **SQLite**
- Concurrent read-write &rarr; consider **PostgreSQL** (better) or **MySQL**

**<mark>5. Do you need SQL compliance?</mark>**
- Yes &rarr; consider **PostgreSQL**

**<mark>6. Is network access required?</mark>**
- Yes &rarr; maybe **not SQLite**

**<mark>7. Is this DBMS integrated with other tools?</mark>**
- Yes &rarr; consider **PostgreSQL**

**<mark>8. Is this DBMS used to power websites or web applications?</mark>**
- Yes &rarr; consider **MySQL**

**<mark>9. Do you need to replicate this DBMS?</mark>**
- Yes &rarr; consider **MySQL**

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
| <span style="display: inline-block; width:230px">- `null` <br> - `integer`: signed integers <br> - `real` <br> - `blob`: Binary Large Objects</span> | <span style="display: inline-block; width:230px">- several numerical types <br> - several date and time types <br> - several string types</span> | <span style="display: inline-block; width:230px">- in addition to numeric, string, and date and time <br> - also supports geometric shapes, network addresses, bit strings, text searches, JSON entries</span> |


## SQLite
- a serverless database

### Pros

Lightweight
: - can take up very little disk space
: - no external dependencies

Easy to use
: - not a server process
:   - no need to be stopped, started, or restarted
:   - no configuration files to be managed

Portable
: - An entire SQLite database is stored in a single file, 
: - whereas other DBMSs typically store data as a large batch of separate files.
: - can be easily shared

### Cons

Limited concurrency
: - Concurrency – the ability of two transactions to use the same data at the same time
: - multiple processes can access and query an SQLite database
: - but only one process can make changes to the database at any given time

No user management
: - The access permissions used are the typical access permissions of the underlying operating system.
: - poor for applications that require multiple users with special access permissions

Security
: - Being serverless may not be able to shield the database from bugs in the client application.
: - Server database can control data access with more precision.


## MySQL
- the most popular relational database since 2012
- powers many of world’s largest websites and applications like Twitter, Facebook, Netflix, and Spotify
- exhaustive documentation and large community of developers available
- peed and reliability at the expense of full adherence to standard SQL

### Pros

Popularity & ease of use
: - experienced data administrators available
: - abundant support online

Security
: - support user management
: - as opposed to SQLite

Replication
: - support setting up a database backup solution
: - support horizontally scaling a database

### Cons

Functional limitations
: MySQL does not fully support standard SQL.

Licensing and proprietary features
: - Dual-licensed
: - (1) free, open-source edition licenced under GPLv2
: - (2) commercial editions released under proprietary licenses
: - some features and plugins are only available for the proprietary editions

Slowed development
: Oracle’s acquisition of Sun resulted in slowed development process and led to lack of agile responses to problems. 


## PostgreSQL


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
| <span style="display: inline-block; width:350px">- database engines implemented as a server process <br> - allow programs to communicate with the host server <br> - an interprocess communication that relays requests <br> - e.g. mySQL and PostgreSQL</span> | <span style="display: inline-block; width:350px">- interact (access, read, and write) with the database disk file directly <br> - e.g. SQLite</span> |


## SQLite
- a serverless database
- hence simplified setup process
    - no need to configure a server process
    - all that is needed is access to the disk










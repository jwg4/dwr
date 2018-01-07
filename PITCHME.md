# Reasons to use SQLite
An introduction to SQLite - the robust, lightweight, portable, relational database which is in (many) cars. 
---

## WHAT is SQLite ?
- a SQL database
- transactional, relational
- serverless
- contained in a single file
- supported by almost every language
- based on a small, reliable C library
- backwards compatible

---
# WHERE is it installed?
In cars. 

---
## WHY is it in cars?
- don't choose Microsoft SQL server - your car doesn't have that much RAM.
- don't even choose postgresql - don't want to configure shared_buffer on a car.
- don't choose XML - harder to read, harder to structure data.
- don't choose a custom binary format - guys in garages want to write to it.

---
## HOW do I use SQLite?
 - From any programming language
 - module in core Python
 - using a command line interface
 - by multiple processes at once
 - anyone who can read or write to your file
 - with Datasette - an awesome project to wrap SQLite database with REST APIs
 
---
## WHEN should I use SQLite?
If you put some data in:
 - XML
 - CSV
 - XLS/XLSX
 - ACCESS db
 - JSON?
and you ever:
 - Send the data to someone
 - Throw it away after you've finished with it
 - Make a backup of today's version.
 
you should use SQLite.

If you create any kind of SQL database and
 - copy all the data from another SQL database
 - write the whole database to a file
 - delete it after use.
 
you should use SQLite.

If you are creating a custom file format for your application to write to, you should use SQLite

---
## 

 
---
## Links
 - https://sqlite.org/
 - https://github.com/simonw/datasette
 - https://gitpitch.com/ GitPitch - how I made this talk

### Thanks to Robert Hardy for setting up Full Stack Quants


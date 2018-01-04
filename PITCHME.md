# Reasons to use SQLite
An introduction to SQLite - the robust, lightweight, portable, relational database which is in (many) cars. 
---

## WHAT is SQLite ?
- a SQL database
- serverless
- contained in a single file
- supported by almost every language
- based on a small, reliable C library
- backwards compatible
- in cars

---
## WHY is it in cars?
- don't choose Microsoft SQL server - your car doesn't have that much RAM
- don't even choose postgresql - don't want to configure shared_buffer
- don't choose XML - harder to read, harder to structure data
- don't choose a custom binary format - guys in garages want to write to it

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

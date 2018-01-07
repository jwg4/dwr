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
## WHERE is it installed?
 - In cars. 

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
## SQLite seems to be on your side
```
sqlite> .open C:\Users\jack\Documents\foo.db
Error: unable to open database "C:UsersjackDocumentsoo.db": unable to open database file
sqlite> .open C:/Users/jack/Documents/foo.db
sqlite> CREATE TABLE foo (
   ...>   id BIGSERIAL PRIMARY KEY,
   ...>   value_1 INTEGER,
   ...>   value_2 FLOAT,
   ...>   value_3 CHARACTER(10),
   ...>   value_4 JSONB
   ...> );
sqlite> INSERT INTO foo (value_1, value_2, value_3, value_4) VALUES (5556593, 3.141592635589, "ASDF asdf.", '{"foo": "bar", "baz": 12345}');
sqlite> SELECT * FROM foo;
|5556593|3.141592635589|ASDF asdf.|{"foo": "bar", "baz": 12345}
```
@[1-2]cmd.exe may not be on your side
@[3]Create a database that doesn't yet exist
@[4-10]Create a table. 
@[11]Put some stuff in it.
@[12-13]Get the stuff out.
@[9](SQLite doesn't have a JSONB format)
 
---
## WHEN should I use SQLite?
If you put some data in XML/CSV/Excel/ACCESS and then:
 - Send the data to someone
 - Throw it away after you've finished with it
 - Make a backup of today's version.
 
you should use SQLite.

---
## WHEN should I use SQLite? II
If you have data in 
 - YAML
 - JSON
 - XML

and you want to add references or IDs to reduce repetition between subobjects, or do joins across different files, you should just cut your losses and install SQLite.

---
## WHEN should I use SQLite? III
If you create any kind of SQL database and
 - copy all the data from another SQL database
 - write the whole database to a file
 - delete it after use.
 
you should use SQLite.

---
## WHEN should I use SQLite? IV

If you are creating a custom file format for your application to write to, you should use SQLite

--- 
## Other cool stuff
 - SQLite is very, very well tested: https://sqlite.org/testing.html
 - SQLite is good for learning about database internals: https://sqlite.org/atomiccommit.html

---
## Links
 - https://sqlite.org/
 - https://github.com/simonw/datasette
 - https://github.com/jwg4/dwr/master/PITCHME.md - this talk
 - https://gitpitch.com/ GitPitch - how I made this talk
 

#### Thanks to Robert Hardy for setting up Full Stack Quants


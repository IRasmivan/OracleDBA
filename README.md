# Oracle DBA - Cheat Sheet.

Storage Structure
1) Block:
2) Extents: This is no longer used, there are table frangmentated is no longer there in Oracle 12c!!!
2.1) Locally Manager Extents is used by oracle to auto extents.
3) Segments:
**Type of Segments**
Table Segments
Index Segments
Undo Segments
Temporary Segments - Sorting, Temporary table space. 



The below query gives you the size of the data table and temp table.
~~~~
select * from dba_data_files;
select * from v$datafile;
select * from dba_temp_files;
select * from v$tempfile;
~~~~



4) Killing a session.

~~~~
select * from v$session;
select * from v$process;
alter system kill session 'SID, serial#';
~~~~

* repository link :https://github.com/kalizasabine746-crypto/oracle_pdb_ass_II_29810_kaliza/tree/main
* pdb name created: ka_pdb_29810
* issues encounteres; YES 


# oracle_pdb_ass_II_29810_kaliza

# Overview
This project involves three core tasks:
1. Creating a permanent pluggable database (PDB) using SQL*Plus.
2. Creating a temporary PDB via SQL*Plus.
3. Managing PDBs using Oracle Enterprise Manager (OEM).

# Environment Details
| Component       | Setup                          |
|----------------|--------------------------------|
| Operating System| Windows 11                     |
| Database        | Oracle 21c                     |
| Text Editor     | Visual Studio Code (VS Code)   |
| Terminal        | Git Bash                       |
| Browser         | Firefox Developer Edition      |

# task 1: create a new pluggable database

A permanent PDB named ka_pdb_29810 was created as part of this task by running the SQL statements below:

```sql
-- Create the pluggable database
CREATE PLUGGABLE DATABASE ka_pdb_29810
ADMIN USER kaliza_plsqlauca_29810 IDENTIFIED BY admin
FILE_NAME_CONVERT = (
  'C:\USERS\ONBILLBOARDS\DOWNLOADS\ORADATA\ORCL\PDBSEED\',
  'C:\USERS\ONBILLBOARDS\DOWNLOADS\ORADATA\ORCL\KA_PDB_29810\'
);

-- Open pluggable database
ALTER PLUGGABLE DATABASE ka_pdb_29810 OPEN;

-- Save the pdb state
ALTER PLUGGABLE DATABASE ka_pdb_29810 SAVE STATE;
```
![](https://github.com/kalizasabine746-crypto/oracle_pdb_ass_II_29810_kaliza/blob/1ddcdf73075690b3326e65bff26016c78fb09cbe/screenshots/pr1.png)

The SQL statement below helped verify that the PDB was successfully created and is currently operational:

```sql
-- Verify pluggable database creation and current status
SELECT pdb_name, status
FROM dba_pdbs;
```
![](https://github.com/kalizasabine746-crypto/oracle_pdb_ass_II_29810_kaliza/blob/a3e0d9859b02441ab44d5ee940fa47592f62bdc7/screenshots/pr2.png)

# task 2: Create and Delete a PDB

We created a temporary PDB, ob_to_delete_pdb_29699, checked that it was successfully created, and then deleted it. Here are the SQL commands used:

```sql
-- Create temporary pluggable database
CREATE PLUGGABLE DATABASE ka_to_delete_pdb_29810
ADMIN USER kaliza_to_deleteplsqlauca_29810 IDENTIFIED BY admin
FILE_NAME_CONVERT = (
    'C:\USERS\ONBILLBOARDS\DOWNLOADS\ORADATA\ORCL\PDBSEED',
  'C:\USERS\ONBILLBOARDS\DOWNLOADS\ORADATA\ORCL\KA_to_delete_PDB_29810'
);

-- Verify that it exists
SELECT pdb_name
FROM dba_pdbs;

-- Delete it completely
DROP PLUGGABLE DATABASE ka_to_delete_pdb_29810 INCLUDING DATAFILES;

-- Confirm that it no longer exists
SELECT pdb_name
FROM dba_pdbs
WHERE pdb_name = 'KA_TO_DELETE_PDB_29810';
```
![](https://github.com/kalizasabine746-crypto/oracle_pdb_ass_II_29810_kaliza/blob/a3e0d9859b02441ab44d5ee940fa47592f62bdc7/screenshots/pr3.png)
![](https://github.com/kalizasabine746-crypto/oracle_pdb_ass_II_29810_kaliza/blob/a3e0d9859b02441ab44d5ee940fa47592f62bdc7/screenshots/pr3x.png)

# task 3: Oracle Enterprise Manager (OEM)

Using Oracle Enterprise Manager, the pluggable databases were monitored and managed graphically. The screenshots highlight various database operations and performance data captured by OEM.

![](https://github.com/kalizasabine746-crypto/oracle_pdb_ass_II_29810_kaliza/blob/a3e0d9859b02441ab44d5ee940fa47592f62bdc7/screenshots/pr4.png)
![](https://github.com/kalizasabine746-crypto/oracle_pdb_ass_II_29810_kaliza/blob/a3e0d9859b02441ab44d5ee940fa47592f62bdc7/screenshots/pr4s.png)
![](https://github.com/kalizasabine746-crypto/oracle_pdb_ass_II_29810_kaliza/blob/a3e0d9859b02441ab44d5ee940fa47592f62bdc7/screenshots/pr4e.png)

# references


* ([Oracle Enterprise Manager Tutorial](https://www.oracle.com/enterprise-manager/)
*[Pluggable Databases Tutorial](https://www.oracle.com/database/technologies/multitenant.html)


# Originality Statement

* All sources used in this assignment have been properly cited.

* The implementations, analysis, and examples presented are the author’s original work.

* No AI-generated content has been copied directly; any assistance was adapted and appropriately acknowledged.
























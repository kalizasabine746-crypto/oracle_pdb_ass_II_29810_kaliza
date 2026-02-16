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
---


















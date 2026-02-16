## Repository link : [https://github.com/kanyanaaidee-art/oracle-_pdb_ass_II_28813_kanyana/tree/main]
## PDB Name Created:[ka_pdb_28813]
## Issues Encountered
---
## Overview of Tasks
This assignment demonstrates practical skills in Oracle Database 21c multitenant architecture using SQL Developer. The tasks include:

1. Creating a Pluggable Database (PDB) with a user inside it.
2. Creating a temporary PDB and deleting it completely.
3. Accessing Oracle Enterprise Manager (OEM) to monitor the database environment.
4. Preparing professional documentation for submission on GitHub.

The assignment emphasizes PDB lifecycle management, user administration, and OEM monitoring.
## Oracle Environment Used
- Oracle Database Version: 21c
- Tool Used: SQL Developer
- OEM: Oracle Enterprise Manager Express
- Operating System: Windows 10/11
## Task 1: Create a New Pluggable Database
- PDB Name: ka_pdb_28813
- Username inside the PDB: kanyana_plsqlauca_28813
- Password: admin
Steps Performed:
1. Connected to Oracle as SYSDBA using SQL Developer.
2. Switched to the root container: ALTER SESSION SET CONTAINER=CDB$ROOT;
3. Created the PDB: CREATE PLUGGABLE DATABASE ka_pdb_28813 ADMIN USER pdbadmin IDENTIFIED BY admin FILE_NAME_CONVERT = ('pdbseed','ka_pdb_28813');
4. Opened the PDB: ALTER PLUGGABLE DATABASE ka_pdb_28813 OPEN;
5. Switched to the PDB: ALTER SESSION SET CONTAINER=ka_pdb_28813;
6. Created the user inside the PDB: CREATE USER kanyana_plsqlauca_28813 IDENTIFIED BY admin; 
7. Verified user creation: SELECT username FROM dba_users WHERE username = 'KANYANA_PLSQLAUCA_28813';

## Task 2: creating Temporary 
PDB Name: ka_to_delete_pdb_28813

Steps Performed:
1. Created temporary PDB: CREATE PLUGGABLE DATABASE ka_to_delete_pdb_28813 ADMIN USER pdbadmin IDENTIFIED BY admin FILE_NAME_CONVERT = ('pdbseed','ka_to_delete_pdb_28813');
2. Opened the temporary PDB: ALTER PLUGGABLE DATABASE ka_to_delete_pdb_28813 OPEN;
3. Dropped the PDB completely: DROP PLUGGABLE DATABASE ka_to_delete_pdb_28813 INCLUDING DATAFILES;
4. Confirmed deletion: SELECT PDB_NAME, STATUS FROM V$PDBS;
## Task 3: Oracle Enterprise Manager (OEM)
Steps Performed:
1. Opened OEM in browser at https://localhost:5500/em.
2. Bypassed certificate warning safely.
3. Logged in using SYS/SYSTEM with  password i set 
4. Verified: Oracle environment, completed PDB tasks, and username displayed.

These tasks improved understanding of Oracle Multitenant Architecture, PDB lifecycle management, user administration, and Oracle Enterprise Manager monitoring.

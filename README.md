# Lab 5 – Automated User, Group, and Permission Management

This project automates the creation of users, groups, team directories, and secure permission models using Bash scripting. The goal was to simulate real sysadmin workflows and enforce proper access control across multiple teams.

## Overview

This lab includes:

- Automated user creation  
- Automated group creation  
- Automated user-to-group assignment  
- Automated permission + inheritance enforcement  
- Logging for auditing  
- Verification of access control  

All automation was done using custom Bash scripts.

## 1. Verified users and groups did not exist
Confirmed the environment was clean before running any automation.

<img width="1828" height="1018" alt="1 showing users and groups dont exist" src="https://github.com/user-attachments/assets/cb712e4b-7154-408e-bb21-743379d983f2" />

## 2. Verified no scripts existed yet
Checked the `/data/scripts` directory to ensure a blank workspace.

<img width="1804" height="1010" alt="2 showing that scripts dont exist" src="https://github.com/user-attachments/assets/a346816f-3aa0-4da7-9c5a-ac270876ec22" />


## 3. Created users using a custom script
Wrote a Bash script to generate multiple users at once for consistent naming and reduced manual setup.

<img width="1798" height="1011" alt="3 adding users with new script" src="https://github.com/user-attachments/assets/cc9eb9a5-0551-4365-8e13-86e929466105" />


## 4. Verified users were created
Checked `id` to confirm each user was successfully added.

<img width="1810" height="1063" alt="4 SHOWING THE USERS WERE CREATED WITH THE SCRIPT" src="https://github.com/user-attachments/assets/2c7bc40e-32a4-44a5-932f-7cc5c5abdaef" />


## 5. Created groups using a custom script
Automated the creation of team-based groups to support permission inheritance and access control.

<img width="1823" height="1027" alt="5 creating groups using the script i made" src="https://github.com/user-attachments/assets/5c6a39ed-2f05-4492-9d9c-706646e5e588" />


## 6. Added users to groups
Used another script to assign each user to the correct team group.

<img width="1840" height="980" alt="6 adding users to groups with script i made" src="https://github.com/user-attachments/assets/7df5194d-9b94-49ec-b854-9a4e523a7950" />


## 7. Verified group membership
Confirmed that one user from each team was correctly added to their respective group.

<img width="1815" height="1034" alt="7 verifying one user form each team added to group via script" src="https://github.com/user-attachments/assets/20e7538f-0000-4a3b-9b63-f4aa51ccef58" />


## 8. Created team directories
Generated directories under `/data/` for each team to serve as shared workspaces with restricted access.

<img width="1818" height="1013" alt="8 created teams home dirs" src="https://github.com/user-attachments/assets/d3d46a95-6c1d-4601-af22-b204c2fb02a1" />


## 9. Deployed permissions + inheritance script
Created a script that:

- Applies `770` permissions  
- Applies the `g+s` inheritance bit  
- Ensures correct group ownership  
- Creates missing directories  
- Logs all actions to `perms.log`  
This enforces a secure and consistent permission model.

<img width="1563" height="1076" alt="9 created and deployed script for inheritence and permissions" src="https://github.com/user-attachments/assets/094d69f5-66f2-44a0-af26-478973f7358e" />


## 10. Verified script output and logging
Checked the log file to confirm each directory was processed correctly and that the script echoed the expected actions.

<img width="1561" height="983" alt="10 showing the scripts echoes" src="https://github.com/user-attachments/assets/c54814ee-2982-4d54-8255-5b6a830e31ae" />


## 11. Verified access control
Logged in as different team members to confirm:

- Users can access their own team directory  
- Users cannot access other teams’ directories  
- New files inherit the correct group  
- Permissions remain secure  

<img width="1545" height="1051" alt="11 showing users can only access their own dirs" src="https://github.com/user-attachments/assets/9f173762-2a8e-464c-ba1a-ea332d6c7681" />



## 12. Verifying directory creation with script
used my script that adds 770 permissions and inheritance. If the directory does not exist, it creates one with the same permissions and inheritance.

<img width="1907" height="1141" alt="12 showing script creates create a new folder if there isnt one made yet witht he same perms and inheratance" src="https://github.com/user-attachments/assets/5100641b-61ac-431e-82d8-5590b1303dcb" />


## 13. Showing my main two scripts
created these scripts using copilot as a a coach that guided me with, hints, nudges and questions. Never giving me exact commands unless excplicitly told so. 

<img width="1899" height="1136" alt="13 the main two scripts" src="https://github.com/user-attachments/assets/26181d42-40b5-4638-849e-6d66e7365642" />



## Skills Demonstrated

- Bash scripting  
- User and group administration  
- Permission modeling (`770`)  
- Directory inheritance (`g+s`)  
- Logging   
- Troubleshooting path, ownership, and permission issues  
 
 

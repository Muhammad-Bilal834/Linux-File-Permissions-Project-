# Linux File Permissions Management

## Project Overview
This project demonstrates practical Linux file permissions management for a research organization's projects directory. The goal was to update file and directory permissions to reflect proper authorization levels and enhance system security.

## Project Files
[Linux File Permissions Management projecct.pdf](https://github.com/user-attachments/files/23564830/Linux.File.Permissions.Management.projecct.pdf)
– Complete project documentation with detailed explanations and screenshots.


## Tasks Performed

### 1. Check File and Directory Details
- Used `ls -la` command to display detailed listing of directory contents
- Identified all files and directories including hidden files
- Analyzed the 10-character permissions string for each item

### 2. Understand Linux Permissions Structure
The 10-character permissions string breakdown:
- **1st character**: File type (`d` = directory, `-` = file)
- **2nd-4th characters**: User permissions (read, write, execute)
- **5th-7th characters**: Group permissions (read, write, execute)
- **8th-10th characters**: Other users permissions (read, write, execute)

### 3. Modify File Permissions
- **Removed write access for "other" users** on `project_k.txt` using:
  ```bash
  chmod o-w project_k.txt
  ```

### 4. Update Hidden File Permissions
- **Modified permissions for hidden file** `.project_x.txt`:
  - Removed write permissions for user and group
  - Added read permissions for group
  ```bash
  chmod u-w,g-w,g+r .project_x.txt
  ```

### 5. Secure Directory Access
- **Restricted access to drafts directory** to only researcher2 user:
  - Removed execute permissions for group and other users
  ```bash
  chmod g-x,o-x drafts
  ```

## Key Commands Used
- `ls -la` - Detailed directory listing with hidden files
- `chmod` - Change file/directory permissions
- Permission modifiers: `u` (user), `g` (group), `o` (other)
- Permission types: `r` (read), `w` (write), `x` (execute)
- Operators: `+` (add), `-` (remove)

## Skills Demonstrated
- Linux command line proficiency
- Understanding of Linux file permissions
- Security best practices implementation
- Working with hidden files and directories
- Permission management for different user types

## Project Outcome
Successfully updated all file and directory permissions to match organizational security requirements, ensuring proper authorization levels for the research team's projects.

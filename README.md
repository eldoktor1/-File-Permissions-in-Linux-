📝 Summary: File Permissions in Linux 🐧 🔒

This project involved reviewing and modifying file permissions within the projects directory to ensure the security and access control of specific files and directories. Here's a brief summary of the steps taken:

Reviewing File and Directory Information 👀 🔍

The `ls -la` command was used to display a detailed listing of file contents, including hidden files, within the projects directory.
The permissions string, consisting of 10 characters, was analyzed to determine the access rights for users, groups, and others.
Changing File Permissions ✏️ 📁

The `chmod` command was utilized to modify file permissions.
For example, the write access for "other" was removed from a file named `project_k.txt` using the command `chmod o-w project_k.txt`.
Changing Permissions on Hidden Files 👥 🔒

A hidden file named `.project_x.txt` was archived, and its permissions were adjusted.
Write permissions were removed for the user and group, and read permissions were added for the group using commands like `chmod u-w,g-w,g+r .project_x.txt`.
Changing Directory Permissions 📂 🔒

The permissions for the `drafts` directory were modified to restrict access.
Execute permissions were removed for groups using the `chmod` command, ensuring that only the researcher2 user had access.
These steps helped ensure that only authorized individuals had the appropriate level of access to files and directories in the projects directory, contributing to a secure system.

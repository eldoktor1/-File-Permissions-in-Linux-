# File Permissions in Linux 🐧🔒

This repository contains information and examples related to file permissions in Linux. The goal of this project is to demonstrate how to review and modify file permissions to ensure security and access control within a specific directory.

## Summary
In this project, we focused on the projects directory and performed the following steps:

1. Reviewing File and Directory Information: We used the `ls -la` command to display a detailed listing of file contents, including hidden files, within the projects directory. We analyzed the permissions string to determine the access rights for users, groups, and others.

2. Changing File Permissions: We utilized the `chmod` command to modify file permissions. For example, we removed write access for "other" on a file named `project_k.txt` using the command `chmod o-w project_k.txt`.

3. Changing Permissions on Hidden Files: We archived a hidden file named `.project_x.txt` and adjusted its permissions. We removed write permissions for the user and group, and added read permissions for the group using commands like `chmod u-w,g-w,g+r .project_x.txt`.

4. Changing Directory Permissions: We modified the permissions for the `drafts` directory to restrict access. We removed execute permissions for groups using the `chmod` command, ensuring that only the `researcher2` user had access.

These steps helped ensure that only authorized individuals had the appropriate level of access to files and directories in the projects directory, contributing to a secure system.

## Getting Started
To get started with this project, follow these steps:

1. Clone this repository to your local machine using the following command:
```
git clone https://github.com/your-username/file-permissions-linux.git
```

2. Navigate to the repository directory:
```
cd file-permissions-linux
```

3. Explore the files and directories within the projects directory to understand their current permissions.

4. Review the documentation and examples provided in this repository to learn more about file permissions in Linux.

5. Feel free to modify the files and directories' permissions as needed and observe the changes.

## Contributing
Contributions are welcome! If you have any suggestions, bug fixes, or improvements, please open an issue or submit a pull request. Make sure to follow the repository's code of conduct.

## License
This project is licensed under the MIT License.

You can use the above content as the initial README.md file for your repository. Follow the GitHub documentation to create a new repository and push the code to it. Remember to replace "your-username" in the clone command with your actual GitHub username.

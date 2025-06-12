# File Permissions in Linux

**Project Description**  
This project demonstrates how I managed file and directory permissions in a real-world Linux environment to meet organizational security standards. The research department needed to control access on specific files and folders within the `projects` directory. I reviewed and modified these permissions using standard Linux commands.

---

### 🔍 Check File and Directory Details

To begin, I used the `ls -la` command to inspect the current file and directory permissions within the `projects` directory.

![ls -la output](https://raw.githubusercontent.com/eldoktor1/-File-Permissions-in-Linux-/main/images/permissions_page_1_img_1.png)

This output showed:
- One directory: `drafts`
- One hidden file: `.project_x.txt`
- Five project files

The 10-character string in the first column (e.g., `-rw-rw-r--`) represents the type and permissions of each file or directory.

---

### 🔡 Interpreting Permission Strings

Permissions are broken down as follows:
- First character: File type (`d` for directory, `-` for regular file)
- Characters 2–4: User permissions (read/write/execute)
- Characters 5–7: Group permissions
- Characters 8–10: Others (all other users)

For example, `-rw-rw-r--` means:
- It's a regular file
- The user and group can read/write
- Others can only read

---

### 🛠️ Changing File Permissions

#### Example: Remove Write Access for Others on `project_k.txt`

I used `chmod` to remove write access for "others".

![chmod on project_k.txt](https://raw.githubusercontent.com/eldoktor1/-File-Permissions-in-Linux-/main/images/permissions_page_2_img_1.png)

The `chmod o-w project_k.txt` command removed write permissions from others. I then verified it using `ls -la`.

---

#### Example: Secure a Hidden File `.project_x.txt`

To prevent any writes to `.project_x.txt`, while allowing read access for user and group:

![chmod on hidden file](https://raw.githubusercontent.com/eldoktor1/-File-Permissions-in-Linux-/main/images/permissions_page_3_img_1.png)

Commands used:
```bash
chmod u-w .project_x.txt
chmod g-w .project_x.txt
chmod g+r .project_x.txt

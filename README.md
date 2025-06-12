# File Permissions in Linux

**Project Description**  
This project demonstrates how I managed Linux file and directory permissions
to align with my organization’s security requirements. I audited and modified
access for specific users and groups to ensure appropriate control over
sensitive data in the `projects/` directory.

---

### 📁 Step 1: Audit Existing File Permissions

Using `ls -la`, I inspected the current permissions for files and directories
in the `projects/` folder.

![ls -la output](https://raw.githubusercontent.com/eldoktor1/-File-Permissions-in-Linux-/main/file_permissions_images/permissions_page_1_img_1.png)

> Observation:
> - `.project_x.txt` has write access for the group — too permissive.
> - `drafts/` is a directory with group execute access.
> - `project_k.txt` allows write access to others.

---

### 🔧 Step 2: Remove Write Access for Others (`project_k.txt`)

To comply with policy, I removed `write` access for others on `project_k.txt`.

![chmod project_k.txt](https://raw.githubusercontent.com/eldoktor1/-File-Permissions-in-Linux-/main/file_permissions_images/permissions_page_2_img_1.png)

    chmod o-w project_k.txt
    ls -la

> Result:  
> File now shows `-rw-rw-r--`, removing write access from "others".

---

### 🔐 Step 3: Secure Hidden File `.project_x.txt`

The file `.project_x.txt` should not be writable. I removed write permissions
from both the user and group, but retained group read access.

![chmod on hidden file](https://raw.githubusercontent.com/eldoktor1/-File-Permissions-in-Linux-/main/file_permissions_images/permissions_page_3_img_1.png)

    chmod u-w .project_x.txt
    chmod g-w .project_x.txt
    chmod g+r .project_x.txt

> Result:  
> File now has `-r--r-----`, ensuring no one can write to it.

---

### 🚫 Step 4: Restrict Access to the `drafts/` Directory

Only `researcher2` should have execute access to the `drafts/` directory.
I removed group execute rights to prevent traversal.

![chmod on drafts](https://raw.githubusercontent.com/eldoktor1/-File-Permissions-in-Linux-/main/file_permissions_images/permissions_page_4_img_1.png)

    chmod g-x drafts

> Result:  
> `drafts/` now has `drwx------`, blocking group access.

---

### ✅ Summary

- Audited permissions using `ls -la`
- Used `chmod` to enforce security best practices
- Removed write access from group/others
- Secured sensitive files and directories appropriately

---

**Author:** Mina Abskhron  
**GitHub:** [@eldoktor1](https://github.com/eldoktor1)

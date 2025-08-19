# 🐚 Shell Tutorial – File Permissions with `chmod` and `chown`
---


## 🔹 1. Understanding File Permissions in Linux

Each file/directory in Linux has:

* **Owner** → The user who created the file.
* **Group** → A group of users who may share access.
* **Others** → Everyone else.

### Permission Types

* **r** → Read (4 in numeric)
* **w** → Write (2 in numeric)
* **x** → Execute (1 in numeric)

### Permission Layout

Example from `ls -l`:

```
-rwxr-xr--
```
Breakdown:

* `-` → Regular file (`d` = directory, `l` = symlink, etc.)
* `rwx` → Owner has read, write, execute
* `r-x` → Group has read, execute
* `r--` → Others have read only

---
## 🔹 2. `chmod` – Change File Permissions

### Syntax

```bash
chmod [options] mode filename
```

Modes can be set in **numeric (octal)** or **symbolic** form.

---

### (A) Numeric (Octal) Method

Each permission is represented as a number:

* Read = 4
* Write = 2
* Execute = 1

Add them up:

* `7 = rwx`
* `6 = rw-`
* `5 = r-x`
* `4 = r--`
* `0 = ---`

#### Example:

```bash
chmod 777 script.sh
```

Meaning:

* Owner: 7 → `rwx`
* Group: 7 → `r-w-x`
* Others: 7 → `r-w-x`

### **image**

![image](<chmod  2025-08-19 124346.png>)

---

### (B) Symbolic Method

Use `u` (user/owner), `g` (group), `o` (others), `a` (all).
Operators:

* `+` → Add permission
* `-` → Remove permission
* `=` → Assign exact permission


Modes can be set in **numeric (octal)** or **symbolic** form.

---

### (A) Numeric (Octal) Method

Each permission is represented as a number:

* Read = 4
* Write = 2
* Execute = 1

Add them up:

* `7 = rwx`
* `6 = rw-`
* `5 = r-x`
* `4 = r--`
* `0 = ---`

#### **Examples:**

```bash
chmod u+x script.sh     # Add execute for owner
```
![Image](<chmod2 2025-08-19 130738.png>)


```bash
chmod g-w notes.txt     # Remove write from group
```

![image](<chmod3 2025-08-19 130910.png>)

```bash
chmod o=r file.txt      # Set others to read only
``` 

![image](<chmod4 2025-08-19 130959.png>)


```bash
chmod a+r report.txt    # Everyone gets read access
```

![example](<chmod a+r.png>)

### (C) Recursive Changes

```bash
chmod -R 755 /mydir
```

* `-R` → applies changes recursively to all files/subdirectories.

![image](<chmod recursive 2025-08-19 134628.png>)

---







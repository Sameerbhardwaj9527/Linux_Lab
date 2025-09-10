 # Experiment: Basic Linux Commands

## Objective
To learn and demonstrate the usage of basic Linux commands for navigation, file management, system information, and process handling.

---

## Requirements
- A Linux operating system (Ubuntu, Fedora, Debian, etc.)
- Terminal access

---
# 1. **pwd** – Print Working Directory
Displays the current directory path.

![images](<images/Pwd command .png>)


## 2.`ls` Command

The `ls` command is used to list files and directories in the current working directory.
flag-a list down all the file and folder including the one which are hidden 

`ls -la`

OUTPUT--

Sameer Bhardwaj@LAPTOP-VE3GPB3R MINGW64 ~/Downloads/Linux_Lab (main) 

```bash
$ ls -la

total 20

drwxr-xr-x 1 Sameer Bhardwaj 197121 0 Aug 12 13:43 ./

drwxr-xr-x 1 Sameer Bhardwaj 197121 0 Aug  6 13:17 ../ 

drwxr-xr-x 1 Sameer Bhardwaj 197121 0 Aug 12 21:08 .git/

drwxr-xr-x 1 Sameer Bhardwaj 197121 0 Aug 12 13:43 Linux_Lab/ 


Sameer Bhardwaj@LAPTOP-VE3GPB3R MINGW64 ~/Downloads/Linux_Lab (main)
$
```

Image OF Above command 

![image](<images/ls command 2025-08-12 214612.png>)
 .......
 
# cd -- change directory

### moves into a directory.

```bash
`cd folder_name`
```

## Examples

```bash
`cd documents`       --        # Go to documents

`cd ..`              --         # Go up one level

`cd /`               --         # Go to root

`cd ~`               --        # Go to homr directory
```



# ✅ File and Directory Management

##  `mkdir` - Make Directory

creates a new folder

```bash
 `mkdir new_folder`
 ```


 ##  `touch` - Create File

 Creates and empty file

 ```bash
 `touch file.txt`
 ```

## `cp` Copy files or Directories

```bash
`cp source.txt destination.txt`
```

## Copy folder:

```bash
`cp -r folder1 folder2`
```

## `mv`-- Make or rename File

```bash
mv oldname.txt newname.txt

mv file.txt ~/Documents/     # Move file
```


## `rm`-- Remove files

```bash
`rm file.txt `        # Delete file

`rm -r folder_name`   # Delete folder (recursively)
```

⚠️ Be careful! There is no undo.



# ✅ 3. File Viewing & Editing

## `cat`– View File Contents
Displays content in terminal.

```bash
`cat file.txt
```

## `nano`-- Edit files in terminal
A basic terminal-based text editor.

```bash
nano file.txt
```

* Use arrows to move
* `CTRL + O` To Save
* `CTRL + X` To Exit

## `clear`-- Clears the Terminal
 
 ```bash
`clear`
```

Shortcut:`CTRL + L`

# ✅ 4. System Commands

## `echo`-- print text
Useful for debugging or scripting.

```bash
`echo "Hello, World!"`
```

## `whoami`-- Show Current User

```bash
`whoami`
```

## `man`-- Manual for Any Command

```bash
`man ls
```

 use `q` to quit the manual

 # ✅ 5. Searching and Finding

 ## `find`-- Locate files

```bash
 `find . -name "*.txt"`
```

 🔍 Finds all`.txt`files in current folder and subfolders.

 ## `grep`--  Search Inside Files
 
  ```bash
 grep "hello" file.txt
```

 🔍 Searches for the word `hello` inside `file,txt`



# ✅ 6. Helpful Shortcuts


| Shortcut   | Action                      |
| ---------- | --------------------------- |
| `Tab`      | Auto-complete files/folders |
| `↑ / ↓`    | Browse command history      |
| `CTRL + C` | Stop a running command      |
| `CTRL + L` | Clear screen                |

---


## ✅ 7. **Bonus: Chaining Commands**

* **Run multiple commands**:

```bash
mkdir test && cd test && touch hello.txt
```

* **Run only if previous command succeeds**: `&&`
* **Run regardless of success**: `;`

---

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

![image](<images/chmod  2025-08-19 124346.png>)
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
![image](<images/chmod2 2025-08-19 130738.png>)

```bash
chmod g-w notes.txt     # Remove write from group
```

![image](<images/chmod3 2025-08-19 130910.png>)

```bash
chmod o=r file.txt      # Set others to read only
``` 
![image](<images/chmod a+r.png>)


```bash
chmod a+r report.txt    # Everyone gets read access
```

![image](<images/chmod a+r.png>)

### (C) Recursive Changes

```bash
chmod -R 755 /mydir
```

* `-R` → applies changes recursively to all files/subdirectories.

![iamge](<images/chmod recursive 2025-08-19 134628.png>)
---

## 🔹 3. `chown` – Change File Ownership

### Syntax

```bash
chown [options] new_owner:new_group filename
```

### Examples:

```bash
chown sameer file.txt           # Change owner to user 'sameer'
chown sameer:dev file.txt       # Change owner to 'sameer' and group to 'dev'
chown :dev file.txt            # Change only group to 'dev'
chown -R sameer:dev /project    # Recursive ownership change
```

---

## 🔹 4. Putting It All Together

### Example Scenario

```bash
touch project.sh
ls -l project.sh
```

Output:

```
-rw-r--r-- 1 sameer dev 0 Aug 19 12:00 project.sh
```

Now:

```bash
chmod 700 project.sh       # Only owner has rwx
chmod u+x,g-w project.sh   # Add execute for user, remove write for group
chown root:admin project.sh # Change owner to root and group to admin
```

---

## 🔹 5. Quick Reference Table

| Numeric | Permission | Meaning      |
| ------- | ---------- | ------------ |
| 0       | ---        | No access    |
| 1       | --x        | Execute only |
| 2       | -w-        | Write only   |
| 3       | -wx        | Write + Exec |
| 4       | r--        | Read only    |
| 5       | r-x        | Read + Exec  |
| 6       | rw-        | Read + Write |
| 7       | rwx        | Full access  |

---

✅ **Key Tip**: Use **numeric for quick settings** (e.g., 755, 644) and **symbolic for fine adjustments** (`u+x`, `g-w`).

---

# 📌**Extra questions**

### ❓What is the difference between chmod and chown?

Ans-✅ In short (theory):

chmod → modifies the mode/permissions of a file.

chown → modifies the ownership of a file.

### ❓How do you check current directory and user?

Ans-Current directory → the folder where the process is working.

🔹 Command: `pwd`

Current user → the identity under which the process runs.

🔹 Command: `whoami`
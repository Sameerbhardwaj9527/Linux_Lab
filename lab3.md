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

![image](<Pwd command .png>)


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

![image](<ls command 2025-08-12 214612.png>)
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















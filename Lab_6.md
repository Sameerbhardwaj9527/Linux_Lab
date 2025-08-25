# **🐚 Shell Scripting Tutorial!!**
### Shell scripting allows you to automate tasks in Linux/Unix by writing commands inside a file that the shell executes line by line.

### 1. 🔹 What is a Shell Script?
A shell is a command-line interpreter (e.g., bash, zsh, sh).
A shell script is a text file with a series of commands.
File usually has .sh extension, though not mandatory.

### Example: hello.sh

```bash
#!/bin/bash
echo "Hello, World!"
```
Run it:

chmod +x hello.sh   # make it executable
./hello.sh
Output:

Hello, World!

# **IMAGE**
![image](<shell script1.png>)

----

## 2. 🔹 Variables

Variables store data (text, numbers, paths, etc.).

### Defining variables

```bash
name="Vibhu"
age=37
```

⚠️ No spaces around `=`.

### Accessing variables

```bash
echo "My name is $name and I am $age years old."
```

Output:

```
My name is Vibhu and I am 37 years old.
```
# **"image"**
![image](shellscript2.png)


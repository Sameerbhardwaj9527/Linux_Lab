# **Experiment: Counting Lines, Words, and Characters in a File using Shell Script**

## **Objective**
To write a shell script that counts the number of **lines**, **words**, and **characters** in a given text file using the `wc` command.

---

## **Requirements**
- Linux/Unix environment  
- Bash shell  
- Text editor (e.g., `nano`, `vim`)  
- A sample text file (e.g., `sample.txt`)  

---

## **Algorithm**
1. Start the script with `#!/bin/bash`.  
2. Check if exactly one argument (filename) is passed.  
   - If not, display usage and exit.  
3. Check if the file exists.  
   - If not, display an error and exit.  
4. Use `wc -l`, `wc -w`, and `wc -m` to count lines, words, and characters.  
5. Display the results.  

---

## **Program Code**
Save the following as **count_lwc.sh**:

```sh
#!/bin/bash
# count_lwc.sh
# Usage: ./count_lwc.sh filename.txt

if [ $# -ne 1 ]; then
  echo "Usage: $0 <filename>"
  exit 1
fi

if [ ! -f "$1" ]; then
  echo "File not found."
  exit 1
fi

lines=$(wc -l < "$1")
words=$(wc -w < "$1")
chars=$(wc -m < "$1")

echo "Lines: $lines"
echo "Words: $words"
echo "Characters: $chars"
```
# **Image**
![image](images/count_lines.png)

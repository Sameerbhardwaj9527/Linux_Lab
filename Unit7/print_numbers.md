# **Experiment: Printing Numbers Using Shell Script**

## **Aim**
To write a shell script that prints numbers stored in an array.

---

## **Algorithm**
1. Start the program with the bash shebang (`#!/bin/bash`).
2. Initialize an array `a` with numbers.
3. Use a `for` loop to iterate through all elements of the array.
4. Print each element one by one.

---

## **Program Code**

```sh
#!/bin/bash
# one_to_ten.sh
# Usage: ./one_to_ten.sh

a=(1 2 3 4 5 6 7)

for i in "${a[@]}"; do
  echo "$i"
done
```
## **image for the output**

![image](images/print_numbers.sh.png)
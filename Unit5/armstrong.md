# **Experiment: Armstrong Number Program in Shell Script**

## **Objective**
To write and execute a shell script that checks whether a given number is an **Armstrong number** or not.

## **Theory**
- An **Armstrong number** (also known as a narcissistic number, pluperfect number, or pluperfect digital invariant (PPDI)) is a number that is equal to the sum of its own digits each raised to the power of the number of digits.  
- For example:
  - `153 = 1³ + 5³ + 3³`
  - `9474 = 9⁴ + 4⁴ + 7⁴ + 4⁴`

### Formula:
If a number has `n` digits:
\[
\text{Armstrong Number} = d_1^n + d_2^n + d_3^n + \dots + d_n^n
\]

## Algorithm
1. Read a number from the user.  
2. Count the number of digits.  
3. Extract each digit using modulus operator.  
4. Raise each digit to the power of total digits and add them.  
5. Compare the sum with the original number.  
6. If both are equal → Armstrong number, else not.

## Shell Script Code (`armstrong.sh`)

```sh
#!/bin/bash

# Read a number
echo "Enter a number: "
read num

# Store original number
original=$num
sum=0

# Count number of digits
n=${#num}

# Process each digit
while [ $num -gt 0 ]
do
    digit=$(( num % 10 ))
    power=1
    i=0
    while [ $i -lt $n ]
    do
        power=$(( power * digit ))
        i=$(( i + 1 ))
    done
    sum=$(( sum + power ))
    num=$(( num / 10 ))
done

# Check Armstrong condition
if [ $sum -eq $original ]
then
    echo "$original is an Armstrong number."
else
    echo "$original is NOT an Armstrong number."
fi
```
# **image**

![image](armstrong.sh.png)



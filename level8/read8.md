# Bandit Level 8

## Objective

The password for the next level is stored in the file `data.txt`. The file contains many lines of text, and only one line occurs exactly once. The password is that unique line.

## How I Solved It

After logging into the Bandit Level 8 server, I used the `ls` command to list the files in the current directory.

```bash
ls
```
The command returned the file path:
```
data.txt
```

I needed to find the line that appears only once in the file. I used the ```sort``` command to sort all lines, then piped the output to ```uniq -u``` to print only the unique line (the one that occurs exactly once).
```
sort data.txt | uniq -u
```
The command returns:
```
UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
```
This displayed the password for Level 8.

## Commands Used

```bash
ls
sort data.txt | uniq -u
```

## Command Explanation

```bash
sort data.txt | uniq -u
```

1. ```sort data.txt``` – sorts all lines in ```data.txt``` alphabetically. This ensures that identical lines are grouped together.
2. ```|```  – pipes the sorted output to the next command.
3. ```uniq -u``` – filters the input and prints only lines that appear exactly once (the -u flag means "unique").
Together, these commands identify the single line that is not repeated in the file.


## Password for Level 9

```text
UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
```

## What I Learned

I learned how to use ```sort``` and ```uniq``` together to find unique lines in a file. This is a powerful combination for analysing data files with duplicate entries.

## Result

Successfully found the password for Bandit Level 9.

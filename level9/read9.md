# Bandit Level 9

## Objective

The password for the next level is stored in the file `data.txt`. However, the file is a binary file containing non‑printable characters. The password can be found by extracting human‑readable strings from the file and searching for lines that contain `===`.

## How I Solved It

After logging into the Bandit Level 9 server, I used the `ls` command to list the files in the current directory.

```bash
ls
```
The command returned the file path:
```
data.txt
```

Since the file is binary, I used the ```strings``` command to extract all printable character sequences from it, and piped the output to ```grep``` to search for lines containing ```===```.
```
strings data.txt | grep "==="
```
The command returns:
```
========== password
========== truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
```
This displayed the password for Level 8.

## Commands Used

```bash
ls
strings data.txt | grep "===" 
```

## Command Explanation

```bash
strings data.txt | grep "==="   
```

1. ```strings data.txt``` – extracts all sequences of printable characters (at least 4 characters long by default) from the binary file data.txt.
2. ```|```  – pipes the sorted output to the next command.
3. ```grep "==="``` – searches for lines containing three consecutive equals signs, which often precede passwords in these challenges.
Together, these commands identify the single line that is not repeated in the file.


## Password for Level 9

```text
UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
```

## What I Learned

How to use the strings command to extract human‑readable text from binary files.

How to pipe the output of strings into grep to search for specific patterns.

That binary files may contain useful text hidden among non‑printable characters.

## Result

Successfully found the password for Bandit Level 10.

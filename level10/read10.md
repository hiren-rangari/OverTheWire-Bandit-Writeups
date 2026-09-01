# Bandit Level 10

## Objective

The password for the next level is stored in the file `data.txt`, but the file contains base64‑encoded data. The goal is to decode it to retrieve the password.

## How I Solved It

After logging into the Bandit Level 10 server, I used the `ls` command to list the files in the current directory.

```bash
ls
```
The command returned the file path:
```
data.txt
```

I used the ```cat``` command to read the file and piped the output to ```base64 -d``` to decode it.
```
cat data.txt | base64 -d
```
The command returns:
```
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
```
This displayed the password for Level 11.

## Commands Used

```bash
ls
cat data.txt | base64 -d 
```

## Command Explanation

```bash
cat data.txt | base64 -d 
```

1. ```cat data.txt``` – reads the contents of ```data.txt```.
2. ```|```  – pipes the sorted output to the next command.
3. ``` base64 -d``` – decodes the base64‑encoded input and prints the original data.


## Password for Level 11

```text
6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
```

## What I Learned

How to use ```base64 -d``` to decode base64‑encoded text.

How to pipe the output of ```cat``` into ```base64``` for decoding.

That data can be encoded to prevent simple reading, but decoding is straightforward with the right tools.

## Result

Successfully found the password for Bandit Level 11.

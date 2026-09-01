# Bandit Level 11

## Objective

The password for the next level is stored in the file `data.txt`. However, the file contains text that has been encrypted with a simple ROT13 cipher (each letter shifted by 13 positions). The goal is to decode the text to retrieve the password.

## How I Solved It

After logging into the Bandit Level 11 server, I used the `ls` command to list the files in the current directory.

```bash
ls
```
The command returned the file path:
```
data.txt
```

I used the ```tr``` command to translate the letters by shifting them 13 positions (ROT13). The command reads the file and applies the transformation.
```
tr 'A-Za-z' 'N-ZA-Mn-za-m' < data.txt
```
The command returns:
```
The password is 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
```
This displayed the password for Level 11.

## Commands Used

```bash
ls
tr 'A-Za-z' 'N-ZA-Mn-za-m' < data.txt
```

## Command Explanation

```bash
tr 'A-Za-z' 'N-ZA-Mn-za-m' < data.txt
```

1. ```tr``` – translates or deletes characters.
2. ```'A-Za-z'``` – specifies the set of characters to translate (all uppercase and lowercase letters).
3. ```'N-ZA-Mn-za-m'``` – specifies the replacement set. This maps:

A→N, B→O, ... M→Z (first half of alphabet shifts to second half)

N→A, O→B, ... Z→M (second half shifts to first half)

Similarly for lowercase.
4. ```< data.txt``` – redirects the contents of ```data.txt``` as input to ```tr```.


## Password for Level 12

```text
7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
```

## What I Learned

How to use the ```tr``` command for character translation.

How ROT13 works and how to apply it using ```tr```.

That simple ciphers like ROT13 can be easily reversed with the same command.

## Result

Successfully found the password for Bandit Level 12.

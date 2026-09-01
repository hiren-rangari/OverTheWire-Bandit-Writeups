# Bandit Level 7

## Objective

The password for the next level is stored in the file `data.txt` next to the word `millionth`.

## How I Solved It

After logging into the Bandit Level 7 server, I used the `ls` command to list the files in the current directory.

```bash
ls
```
The command returned the file path:
```
data.txt
```

I used the grep command to search for the word ```millionth``` inside ```data.txt```.
```
grep millionth data.txt
```
The command returned the file path:
```
millionth   cvX2JJa4CFALtqS87jk27qwqGhBM9plV
```
This displayed the password for Level 7.

## Commands Used

```bash
ls
grep millionth data.txt
```

## Command Explanation

```bash
grep millionth data.txt
```

1. ```grep``` is a command-line utility for searching text patterns.
2. ```millionth ```is the search pattern.
3. ```data.txt``` is the file to search in.
```grep``` prints lines that contain the pattern. In this case, it printed the line containing the password.


## Password for Level 7

```text
cvX2JJa4CFALtqS87jk27qwqGhBM9plV
```

## What I Learned

I learned how to use ```grep``` to search for a specific word in a file. This is very useful for finding information quickly without reading through the entire file..

## Result

Successfully found the password for Bandit Level 8.

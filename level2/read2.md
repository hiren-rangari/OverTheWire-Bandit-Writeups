# Bandit Level 2

## Objective

The objective of Level 2 is to find the password for the next level. The password is stored in a file with spaces in its filename.

## How I Solved It

After logging into the Bandit Level 2 server, I used ls to list the files in the current directory.
```
ls
```
The output showed a file named 
```-- spaces in this filename --```
Since the filename contains spaces, I used ```./``` followed by the complete filename to access it.
```
cat ./-- spaces in this filename --
```
This displayed the password for the next level.

Commands Used
```
ls
```
```
cat ./-- spaces in this filename --
```

Command Explanation
```ls``` is used to list files and directories.
```cat ./-- spaces in this filename --``` is used to display the contents of the file.
``` ./``` represents the current directory and helps specify the exact filename, including the spaces.

Password for Level 3
```
7ZZ2LFrykP2zEyvBl4m3clcL7tGYJPME
```
What I Learned

I learned how to access files whose names contain spaces. Using ./ with the complete filename allows the shell to correctly identify the file.

Result

Successfully obtained the password for Bandit Level 3.

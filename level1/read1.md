# Bandit Level 1

## Objective

The objective of Level 1 is to find the password for the next level. The password is stored in a file named `-`.

## How I Solved It

After logging into the Bandit Level 1 server, I used the `ls` command to list the files in the current directory.

```bash
ls
```
The output showed a file named:
```
-
```
The problem is that - has a special meaning in many Linux commands. It can be interpreted as an option or as standard input/output instead of being treated as a normal filename.
Therefore, using:
```bash
cat -
```
may not read the file as expected.
To explicitly tell cat that - is a filename in the current directory, I used:
```bash
cat ./-
```
Here, ./ means the current directory, so ./- clearly refers to the file named -.
The command displayed the password for the next level.
Commands Used
```bash
ls
cat ./-
```
Command Explanation
```bash
ls
```
Lists the files and directories in the current directory.

```bash
cat ./-
```
1. cat displays the contents of a file.
2. ./ represents the current directory.
3. - is the filename.
4. ./- prevents the - from being interpreted as a special option.

Password for Level 2
```bash
PK8fYLZg2hnHSz83plBL1iEPKdD3QToB
```

What I Learned

I learned that filenames beginning with special characters can cause problems with Linux commands.

Using ./ before a filename is a useful way to explicitly specify that the filename should be treated as a path.

Result

Successfully obtained the password for Bandit Level 2.


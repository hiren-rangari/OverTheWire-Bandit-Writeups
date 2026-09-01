# Bandit Level 0

## Objective

The objective of Bandit Level 0 is to log in to the Bandit server using SSH and find the password for the next level.

## Login Details

- Username: `bandit0`
- Host: `bandit.labs.overthewire.org`
- Port: `2220`
- Password: `bandit0`

## How I Solved It

I logged into the Bandit server using the given username and password.

After logging in, I used the `ls` command to list the files in the current directory.

```bash
ls
```
The command showed a file named readme.

I then used the cat command to read the contents of the file:
```bash
cat readme
```
The file contained the password required to log in to the next level.

Password for Level 1:
```bash
6y2kwnwK6grgvwvpvLaa2T1cpFEKOhNR
```
Commands Used:
```bash
ls
cat readme
```
What I Learned
ls is used to list files and directories.
cat is used to display the contents of a file.
Basic Linux commands can be used to explore files and find information.
Result

Successfully obtained the password for Bandit Level 1.

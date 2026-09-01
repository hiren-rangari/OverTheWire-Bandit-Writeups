# Bandit Level 3

## Objective

The objective of Level 3 is to find the password for the next level. The password is stored in a hidden file inside the `inhere` directory.

## How I Solved It

After logging into the Bandit Level 3 server, I used the `ls` command to list the files in the current directory.

```bash
ls
```

The output showed a directory named:

```text
inhere
```

I entered the directory using:

```bash
cd inhere
```

I then used `ls` to check the contents of the directory.

```bash
ls
```

No files were displayed because the required file was hidden.

To display hidden files, I used:

```bash
ls -la
```

This showed a hidden file named:

```text
...Hiding-From-You
```

I then used the `cat` command with `./` to read the file:

```bash
cat ./...Hiding-From-You
```

This displayed the password for the next level.

## Commands Used

```bash
ls
cd inhere
ls
ls -la
cat ./...Hiding-From-You
```

## Command Explanation

```bash
ls
```

Lists the files and directories in the current directory.

```bash
cd inhere
```

Changes the current directory to `inhere`.

```bash
ls -la
```

Lists all files, including hidden files.

- `-l` displays detailed information about the files.
- `-a` displays all files, including hidden files such as `.` and `..`.

```bash
cat ./...Hiding-From-You
```

1. `cat` displays the contents of a file.
2. `./` represents the current directory.
3. `...Hiding-From-You` is the hidden filename.
4. `./` helps explicitly specify the file path.

## Password for Level 4

```text
xzTXq1rDJQVVAzdv5cHq1TQytTWufAMq
```

## What I Learned

I learned how to find hidden files in Linux using `ls -la`.

Hidden files can be identified using the `-a` option with `ls`.

I also learned how to navigate between directories using the `cd` command and access a hidden file using its complete path.

## Result

Successfully obtained the password for Bandit Level 4.

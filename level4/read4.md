# Bandit Level 4

## Objective

The objective of Level 4 is to find the password for the next level. The password is stored in the only human-readable file inside the `inhere` directory.

## How I Solved It

After logging into the Bandit Level 4 server, I used the `ls` command to list the files in the current directory.

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

I then used `ls` to view the files inside the directory.

```bash
ls
```

There were multiple files with names such as `-file00`, `-file01`, and so on.

To identify the type and content format of each file, I used the `file` command with a wildcard:

```bash
file ./*
```

The output showed that most files contained data or other non-text formats. The file `-file07` was identified as:

```text
./-file07: ASCII text
```

Since ASCII text is human-readable, I read the file using:

```bash
cat ./-file07
```

This displayed the password for the next level.

## Commands Used

```bash
ls
cd inhere
ls
file ./*
cat ./-file07
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
file ./*
```

Checks and displays the type of each file in the current directory.

- `file` identifies the type of a file.
- `./` represents the current directory.
- `*` is a wildcard that matches all files in the directory.

```bash
cat ./-file07
```

Displays the contents of the `-file07` file.

## Password for Level 5

```text
6C7h9GD8M6ai5nr7wo1RonrzFjj9yIrG
```

## What I Learned

I learned how to use the `file` command to identify the type of different files.

I also learned how wildcards such as `*` can be used to perform an operation on multiple files at once.

## Result

Successfully identified the human-readable file and obtained the password for Bandit Level 5.

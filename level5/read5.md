# Bandit Level 5

## Objective

The objective of Level 5 is to find the password for the next level. The password is stored in a file with specific properties: it is human-readable, has a size of 1033 bytes, and is not executable.

## How I Solved It

After logging into the Bandit Level 5 server, I used the `ls` command to list the files in the current directory.

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

I then used `ls` to view the directories inside `inhere`.

```bash
ls
```

There were many directories with names such as `maybehere00`, `maybehere01`, and so on.

Instead of checking every file manually, I used the `find` command to search for a file matching the required conditions.

```bash
find . -type f -size 1033c ! -executable
```

The command returned:

```text
./maybehere07/.file2
```

I then used the `cat` command to read the file:

```bash
cat ./maybehere07/.file2
```

This displayed the password for the next level.

## Commands Used

```bash
ls
cd inhere
ls
find . -type f -size 1033c ! -executable
cat ./maybehere07/.file2
```

## Command Explanation

```bash
find . -type f -size 1033c ! -executable
```

1. `find` is used to search for files and directories.
2. `.` tells `find` to search from the current directory.
3. `-type f` searches only for regular files.
4. `-size 1033c` searches for files that are exactly 1033 bytes in size.
5. `! -executable` excludes executable files.

```bash
cat ./maybehere07/.file2
```

Displays the contents of the file found by the `find` command.

## Password for Level 6

```text
pXa26xhMWaC2SvDotA4r9EgZkulOeSBW
```

## What I Learned

I learned how to use the `find` command with multiple conditions to locate a specific file.

I also learned how to search recursively through directories and filter files based on their type, size, and executable permissions.

## Result

Successfully found the required file and obtained the password for Bandit Level 6.

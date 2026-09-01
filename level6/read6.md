# Bandit Level 6

## Objective

The password for the next level is stored somewhere on the server. It is owned by user `bandit7` and group `bandit6`, and has a file size of exactly 33 bytes. The goal is to locate and read that file.

## How I Solved It

After logging into the Bandit Level 6 server, I used `ls` to check the current directory – it was empty.

I then used the `find` command to search the entire filesystem for a file matching the given conditions:

- owned by user `bandit7`
- owned by group `bandit6`
- exactly 33 bytes in size

To avoid clutter from permission‑denied errors (which are common when searching `/`), I redirected standard error to `/dev/null`.

```bash
find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
```
The command returned the file path:
```
/var/lib/dpkg/info/bandit7.password
```

I then read the file using ```cat```:
```
cat /var/lib/dpkg/info/bandit7.password
```
This displayed the password for Level 7.

## Commands Used

```bash
ls
find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
cat /var/lib/dpkg/info/bandit7.password
```

## Command Explanation

```bash
find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
```

1. `find` starts the search.
2. `/` search from the root directory (entire filesystem).
3. `-user bandit7` match files owned by user bandit7.
4. `-group bandit6` match files owned by group bandit6.
5. `-size 33c` match files exactly 33 bytes in size (c means bytes).
6. `2>/dev/null` redirect error messages to the null device, keeping the output clean.

```bash
cat /var/lib/dpkg/info/bandit7.password
```

Displays the contents of the discovered file.

## Password for Level 6

```text
Bmnnvf82KzQlfxgAI2d1zYbr1u9pr3E3
```

## What I Learned

How to search the entire filesystem with find using multiple criteria (user, group, size).

How to suppress error messages with 2>/dev/null to avoid clutter.

That files can be located anywhere, not just in the home directory.

## Result

Successfully found the required file and obtained the password for Bandit Level 7.

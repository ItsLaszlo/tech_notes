# Bash

Explanation of the tool and it's purpose. Be Brief and say it concisely in a sentence

## Key Terms

### Environment variables

_global_: Env var set upon initialization of a shell and can be used across all shells. To make it global export variable to `~/.profile` 

```terminal
❯ cat .zprofile

# Setting PATH for Python 3.9
# The original version is saved in .zprofile.pysave
PATH="/Library/Frameworks/Python.framework/Versions/3.9/bin:${PATH}"
export PATH
```

*_local_*: Env var that is set during a shell session and is erased when the shell is closed.

```bash
export MY_VARIABLE="some value"
echo $MY_VARIABLE # some value
```

\*\*\*\*\*\*\*\*\*\*

### Shell variables

Variables created and only accessible by the script

\*\*\*\*\*\*\*\*\*\*

## Common Commands

### Run the following command only if the first command succeeds

`&&`
`echo Hello && echo World`

\*\*\*\*\*\*\*\*\*\*

### Uncompress a .zip file

`unzip <path to zip file> -d <location to save decompressed file>`  
`-d` show all containers

\*\*\*\*\*\*\*\*\*\*

### Tail display last few lines of a file

`tail -f /path/to/file`  
 `-f` follow bottom of file if any changes are appended

\*\*\*\*\*\*\*\*\*\*

### See all environment variables both local and global

`env`

---

## ADVANCED COMMANDS

### COMMAND

``  
`-`

\*\*\*\*\*\*\*\*\*\*

### COMMAND

``  
`-`

\*\*\*\*\*\*\*\*\*\*

---

## Configs

### Name_of_config

What does the config do  
Config example and definition of each term

\*\*\*\*\*\*\*\*\*\*

---

## Processes

### Process

1. steps
2. step
3. step

\*\*\*\*\*\*\*\*\*\*

---

## Links

[Bash Crash Course](https://zach-gollwitzer.medium.com/the-ultimate-bash-crash-course-cb598141ad03#ada7)  

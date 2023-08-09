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

Variables created in a script and only accessible by the script

```bash
MY_SHELL_VARIABLE="some value"
```

\*\*\*\*\*\*\*\*\*\*

## Common Commands

### Run the following command only if the first command succeeds

`&&`  
`echo Hello && echo World`

\*\*\*\*\*\*\*\*\*\*

### Run the following command output into the next command

`|`  
`cat /etc/passwd | grep --color -E "^[a-z]{3}:"`

\*\*\*\*\*\*\*\*\*\*

### Text transformation tool for simple transformation like fined/replace

`sed [options] <pattern_to_replace> <new_pattern_to_add> <file_with_contents>`  
`-i '<.extension>'` back up file to be made before changes  
`-e'<pattern to follow>'` substitute command to run on file  
`s/<pattern_to_replace>/<pattern_to_insert>/g` s(substitute) /(separates the command and pattern) g(perform replacement globally)  
_example_: `sed -i '' -e 's/,/ /g' apple.csv`  

\*\*\*\*\*\*\*\*\*\*

### Formatting tool for text or formatting transformation

`awk [options] BEGIN { <action_before_processing> }; <optional_condition> { <action_after_processing_line>}`  
`-F` Field separator for the input file  
`BEGIN { print "<PRINT_THIS_STUFF\tAND_THIS_AFTER_TAB>" }` Execute contents before processing any lines  
`NR > <line_num>` If condition (current record number is greater than digit) is full filled execute the following action  
`{ print $<field_number> "\t" $<field_number> "\t" $<field_number> }` Main action block of that is executed for each record line in input file  
_example:_ `awk -F " " ' BEGIN { print "Date\t\tPrice\t\tVolume" }; NR > 1 { print $1 "\t" $2 "\t" $7 } ' apple.csv`  
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

\*\*\*\*\*\*\*\*\*\*

### Find patterns or words in one or more files. Search tool

`grep [options] "<text_to_search_for>" <file_to_search_in>`
`-i` case insensitive  
`-E` extended regular expressions  
`--color` highlight the matching text in color  


\*\*\*\*\*\*\*\*\*\*
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

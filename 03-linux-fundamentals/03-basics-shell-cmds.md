# Linux Shell Basics

### Shell 
Shell is an interface to interact with the OS using commands. Bash(Bourne again shell) is the most common default shell.

Syntax for Bash
```
command [options] [arguments]

ex: ls -l /home
```

To know more about each cmds, type:
- `man ls`: Manual Pages or list command.
- `info ls`: More detailed than man.
- `ls --help`: Quick help


### Essential Commands

#### Navigation
- **cd**: Change directory -> cd /home/user
- **ls**: List files and directories -> ls -l, ls -a
- **pwd**: Print current directory

#### File Operations
- **cp**: Copy files -> cp file1.txt backup.txt
- **mv**: Move/rename files -> mv old.txt new.txt
- **rm**: Remove files -> rm file.txt
- **mkdir / rmdir**: Create/remove directories

#### Viewing Files
- **cat**: View entire file
- **less**: Scrollable view
- **tail**: View end of file
- **head**: View start of file

#### Searching
- **grep**: Search inside files -> grep "text" file.txt
- **find**: Find files in directory tree -> find /home -name "*.txt"
- **locate**: Fast search using database -> locate file.txt

#### Permissions
- **chmod**: Change file permissions -> chmod 755 script.sh
- **chown**: Change file owner -> chown user file.txt
- **chgrp**: Change group of file
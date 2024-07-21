---
title: "Basic and must-know commands on Linux"
datePublished: Sun Jul 21 2024 10:19:01 GMT+0000 (Coordinated Universal Time)
cuid: clyveo7xv000c09kza4yzciyy
slug: basic-and-must-know-commands-on-linux
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1721555114081/332e550d-bded-4d5c-8b3f-deb57999ffad.gif
tags: linux-commands, file-permissions-linux-unix-acls-access-control-lists-security-permissions-chmod-chown-setfacl-getfacl-octal-notation-symbolic-notation-user-permissions-group-permissions-other-permissions-fine-grained-access-control-file-ownership-file-system-security-command-line-operating-systems, filemaintenance, fileoperations, permissionmanagement, ownershipcontrol, directorysearch, timestampupdate, copyandmove, textprocessing

---

In Linux, navigation and directory commands are essential for interacting with the file system. Here are some commonly used commands:

### Navigation Commands:

1. **cd (Change Directory)**:
    
    * Usage: `cd [directory]`
        
    * Example: `cd Documents`
        
    * Moves you to the specified directory. Use `cd` without arguments to return to your home directory (`cd` or `cd ~`).
        
2. **pwd (Print Working Directory)**:
    
    * Usage: `pwd`
        
    * Example: Shows the current directory path you are in.
        
3. **ls (List)**:
    
    * Usage: `ls [options] [directory]`
        
    * Example: `ls -l`
        
    * Lists files and directories in the current directory. Common options include `-l` (long format, showing details like permissions and sizes), `-a` (show hidden files), and `-h` (human-readable sizes).
        

### Directory Commands:

1. **mkdir (Make Directory)**:
    
    * Usage: `mkdir [directory name]`
        
    * Example: `mkdir Documents`
        
    * Creates a new directory with the specified name.
        
2. **rmdir (Remove Directory)**:
    
    * Usage: `rmdir [directory name]`
        
    * Example: `rmdir Documents`
        
    * Removes the specified empty directory.
        
3. **cp (Copy)**:
    
    * Usage: `cp [options] source destination`
        
    * Example: `cp file1.txt /path/to/destination`
        
    * Copies files and directories. Use `-r` option to copy directories recursively.
        
4. **mv (Move)**:
    
    * Usage: `mv [options] source destination`
        
    * Example: `mv file1.txt /path/to/destination`
        
    * Moves files and directories. Can also be used to rename files/directories within the same parent directory.
        
5. **rm (Remove)**:
    
    * Usage: `rm [options] file/directory`
        
    * Example: `rm file.txt`
        
    * Deletes files and directories. Use with caution, as deleted files are not typically recoverable from the command line.
        
6. **chmod (Change Mode)**:
    
    * Usage: `chmod [options] mode file/directory`
        
    * Example: `chmod +x` [`script.sh`](http://script.sh)
        
    * Changes the permissions (read, write, execute) of files and directories.
        
7. **chown (Change Owner)**:
    
    * Usage: `chown [options] owner:group file/directory`
        
    * Example: `chown user1:group1 file.txt`
        
    * Changes the owner and group of files and directories.
        

Some tips!  
1\. ls -la command

`ls -la` is a command in Linux used to list all files and directories in a detailed format, including hidden ones.

Here’s what each part of the command does:

* `ls`: This is the command to list directory contents.
    
* `-l`: This option (lowercase "L") specifies that the output should be in long format. Long format typically includes information such as permissions, number of links, owner, group, size, and timestamp.
    
* `-a`: This option stands for "all" and includes all files and directories, including hidden ones (those whose name starts with a dot `.`).
    

So, `ls -la` together lists all files and directories in the current directory (`.`) in a detailed (long) format, showing all files, including hidden ones. It's a common command used to get a comprehensive view of everything within a directory, including files and directories that might not be visible with a simple `ls` command.

**ls-r | cp-r |chmod -R | where -r stands for recursive**

1. `ls -r`:
    
    * This option is used to reverse the order of the sort to get a reverse listing of files. By default, `ls` lists files and directories in alphabetical order. Using `-r` reverses this order lists them in reverse alphabetical order.
        
    
    Example:
    
    ```bash
    ls -r
    ```
    
2. `cp -r`:
    
    * In the `cp` command, `-r` stands for. It is used to copy directories and their contents recursively, including all subdirectories and files within them.
        
    
    Example:
    
    ```bash
    cp -r directory1 directory2
    ```
    
3. `chmod -R`:
    
    * In the `chmod` command, `-R` (uppercase "R") stands for recursive as well. It is used to change file permissions recursively for all files and directories within a directory.
        
    
    Example:
    
    ```bash
    chmod -R 755 directory
    ```
    

If you encounter `-r` in a command, it's crucial to check the specific command context to understand its exact function, as it can vary significantly between commands.

`-v` **typically stands for "verbose "**

In Linux commands, `-v` typically stands for "verbose". Its exact function can vary depending on the command being used. Here are a few common commands where `-v` is used:

1. `cp -v`:
    
    * In the `cp` (copy) command, `-v` stands for verbose mode. When you use `cp -v`, it displays detailed information about each file being copied, including the source file and destination file paths.
        
    
    Example:
    
    ```bash
    cp -v file1.txt /path/to/destination/
    ```
    
2. `mv -v`:
    
    * Similarly, in the `mv` (move) command, `-v` also enables verbose mode. It displays information about each file or directory being moved, including the source and destination paths.
        
    
    Example:
    
    ```bash
    mv -v file1.txt /path/to/destination/
    ```
    
3. `rm -v`:
    
    * In the `rm` (remove) command, `-v` again enables verbose mode. It displays the names of files and directories as they are being removed.
        
    
    Example:
    
    ```bash
    rm -v file1.txt
    ```
    
4. `chmod -v`:
    
    * In the `chmod` (change mode) command, `-v` can be used to display a message for each file processed, indicating the changes made to file permissions.
        
    
    Example:
    
    ```bash
    chmod -v +x script.sh
    ```
    

The `-v` option is useful when you want to see more detailed information about the operation being performed by a command. It provides feedback and confirmation of each action taken by the command, making it easier to track and verify what changes or operations are being executed.

`-`f **typically stands for "force"**

In Linux commands, **the** `-f` **an option** often stands for "force". Its exact behavior can vary depending on the specific command being used. Here are a few common commands that `-f` is used:

1. `rm -f`:
    
    * In the `rm` (remove) command, `-f` stands for force. It suppresses prompts to confirm the removal of files. It's commonly used in scripts or when you want to delete files without being prompted for confirmation.
        
    
    Example:
    
    ```bash
    rm -f file1.txt
    ```
    
2. `cp -f`:
    
    * In the `cp` (copy) command, `-f` stands for force as well. It causes the `cp` command to overwrite existing destination files without prompting for confirmation.
        
    
    Example:
    
    ```bash
    cp -f file1.txt /path/to/destination/
    ```
    
3. `mv -f`:
    
    * Similarly, in the `mv` (move) command, `-f` forces the move operation without prompting for confirmation, even if it would overwrite existing files.
        
    
    Example:
    
    ```bash
    mv -f file1.txt /path/to/destination/
    ```
    
4. `chmod -f`:
    
    * In the `chmod` (change mode) command, `-f` doesn't force anything related to permissions directly. Instead, it might suppress error messages that would normally be displayed if the command encounters problems.
        
    
    Example:
    
    ```bash
    chmod -f +x script.sh
    ```
    

The `-f` option is useful when you want to carry out an operation forcefully, without being prompted for confirmation or when you want to suppress certain types of errors or warnings. However, use it with caution, especially with commands like `rm -f`, as it can delete files irreversibly without a chance to recover them.

**<mark>File maintenance commands </mark>** in Linux are essential for managing files and directories effectively. Here's an explanation of each command you mentioned:

1. **touch**:
    
    * **Usage**: `touch [options] file`
        
    * **Description**: The `touch` command is used to create empty files or update the access and modification timestamps of existing files. If the file doesn't exist, `touch` creates an empty file with the specified name. If it does exist, `touch` updates the timestamps to the current time.
        
    
    Example:
    
    ```bash
    touch file.txt
    ```
    
2. **find**:
    
    * **Usage**: `find [path...] [expression]`
        
    * **Description**: The `find` command is used to search for files in a directory hierarchy based on various criteria such as file name, permissions, type, size, and more. It is powerful and versatile, allowing complex searches and actions on the found files.
        
    
    Example:
    
    ```bash
    find . -name "*.txt"
    ```
    
3. **umask**:
    
    * **Usage**: `umask [mode]`
        
    * **Description**: The `umask` command sets the default permissions for new files and directories created by the current shell session. It works by subtracting the specified mode from the default permission settings.
        
    
    Example:
    
    ```bash
    umask 022
    ```
    
4. **chmod**:
    
    * **Usage**: `chmod [options] mode file/directory`
        
    * **Description**: The `chmod` command is used to change the permissions (read, write, execute) of files and directories. Permissions can be specified using symbolic or octal notation.
        
    
    Example:
    
    ```bash
    chmod +x script.sh
    ```
    
5. **chown**:
    
    * **Usage**: `chown [options] owner:group file/directory`
        
    * **Description**: The `chown` command changes the owner and/or group of a file or directory to the specified owner and/or group.
        
    
    Example:
    
    ```bash
    chown user1:group1 file.txt
    ```
    
6. **chgrp**:
    
    * **Usage**: `chgrp [options] group file/directory`
        
    * **Description**: The `chgrp` command changes the group ownership of a file or directory to the specified group.
        
    
    Example:
    
    ```bash
    chgrp group1 file.txt
    ```
    
7. **cp**:
    
    * **Usage**: `cp [options] source destination`
        
    * **Description**: The `cp` command copies files and directories. It can copy single or multiple files, as well as entire directories and their contents. Use the `-r` option for recursive copying of directories.
        
    
    Example:
    
    ```bash
    cp file1.txt /path/to/destination/
    ```
    
8. **mv**:
    
    * **Usage**: `mv [options] source destination`
        
    * **Description**: The `mv` command moves (or renames) files and directories from one location to another. It can also be used to rename files and directories within the same parent directory.
        
    
    Example:
    
    ```bash
    mv file1.txt /path/to/destination/
    ```
    
9. **wc**:
    
    * **Usage**: `wc [options] file`
        
    * **Description**: The `wc` (word count) command is used to count the number of lines, words, and bytes in a file. It's useful for obtaining basic statistics about the content of text files.
        
    
    Example:
    
    ```bash
    wc -l file.txt
    ```
    

These commands are fundamental for file and directory maintenance tasks in Linux, enabling users to manage permissions, ownership, content, and locations of files efficiently from the command line.
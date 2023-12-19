## Navigating The File System
### pwd
pwd command working directory to the screen.

### ls
ls command displays the names of the files and directories in the current working directory.

### cd
cd command navigates between directories. 

## Reading File Content
### cat
cat command displays the content of a file. 
```
cat updates.txt
```

### head
head command displays just the beginning of a file
```
head updates.txt
head -n 5 updates.txt
```

### tail
tail command does the opposite of head 
```
tail updates.txt
```

### less
less command returns the content of a file one page at a time. 
```
less updates.txt
```
Keyword | Comment 
--- | --- 
Space bar | Move forward one page 
b | Move back one page 
Down arrow | Move forward one line 
Up arrow | Move back one line 
q | Quit and return to the previous terminal window 

## Filtering for information
### grep
The grep command searches a specified file and returns all lines in the file containing a specified string. 
```
grep OS updates.txt
```

### Piping
Piping sends the standard output of one command as standard input to another command for further processing. 
```
ls /home/analyst/reports | grep users
```

### find 
The find command searches for directories and files that meet specified criteria. `-name` is case-sensitive, and `-iname` is not.  `-mtime` option can be used for this search.
```
find /home/analyst/projects
find /home/analyst/projects -name "*log*"
/home/analyst/projects -iname "*log*"
find /home/analyst/projects -mtime -3
```
**`Note`**: An asterisk (*) is used as a wildcard to represent zero or more unknown characters. The option -mmin can be used instead of `-mtime` if you want to base the search on minutes rather than days.

## Manage Directories and Files
### mkdir
The mkdir command creates a new directory. 
```
mkdir /home/analyst/logs/network
mkdir network
```

### rmdir
The rmdir command removes, or deletes, a directory. For example, entering `rmdir /home/analyst/logs/network` would remove this empty directory from the file system.
**`Note`**: The rmdir command cannot delete directories with files or subdirectories inside. For example, entering rmdir /home/analyst returns an error message.

### touch and rm
The touch command creates a new file. This file won’t have any content inside. If your current directory is `/home/analyst/reports`, entering `touch permissions.txt` creates a new file in the reports subdirectory called permissions.txt.

The `rm` command removes, or deletes, a file. This command should be used carefully because it’s not easy to recover files deleted with rm. To remove the permissions file you just created, enter `rm permissions.txt`. 
```
touch permissions.txt
rm permissions.txt
```

### mv and cp
You can also use mv and cp when working with files. The mv command moves a file or directory to a new location, and the cp command copies a file or directory into a new location. The first argument after mv or cp is the file or directory you want to move or copy, and the second argument is the location you want to move or copy it to.
```
mv permissions.txt /home/analyst/logs
cp permissions.txt /home/analyst/logs
```
**`Note`**: The mv command can also be used to rename files. To rename a file, pass the new name in as the second argument instead of the new location. For example, entering mv permissions.txt perm.txt renames the permissions.txt file to perm.txt.
```
mv permissions.txt perm.txt
```

### nano text editor
nano is a command-line file editor that is available by default in many Linux distributions. 
```
nano permissions.txt
```
Since there isn't an auto-saving feature in nano, it’s important to save your work before exiting. To save a file in nano, use the keyboard shortcut `Ctrl + O`. You’ll be prompted to confirm the file name before saving. To exit out of nano, use the keyboard shortcut `Ctrl + X`.

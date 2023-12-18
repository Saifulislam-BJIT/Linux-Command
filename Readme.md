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

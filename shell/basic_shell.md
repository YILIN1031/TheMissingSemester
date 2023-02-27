# Basic Shell

## Common(Basic)

### **cd** 

Change directory, `cd -` change the current directory to the last working one, `cd ~` change to the home, `cd /` change to root

### **ls** 

see directory contents, `ls -a` see **.** and **..**, namely "dotfiles", `ls -l` to see more information 

### **pwd** 

See the current location of working the directory

### **cp**

Copy files from one place to another 

### **mv**

Move files or change the name

### **mkdir**

Making directories 

### **rm**

Remove files, `rm -rf` remove strongly(force)

### **ln -s**

Set symbolic links, `ln -s origin_file access_path`

### **file**

See the file type

### **less**

Less is more, see text contents of a file(like .txt), or combine with pipe to see the standard output, for example: `ls | less`

### **type**

See the command type

### **help**

Get help for Shell Builtins

### **man**

Display a program's manual page

### **alias**

Set abbreviation or another name for a set of command

### **cat**

Concatenate， be used to change the direction of standard input and output for usual programs, using combine with `>`, `<` and `|` 

### **echo**

Display the result (standard input) of a command

### **tee**

Read from STDIN and output to FILES and STDOUT, e.g. some commands... | tee file | command


### **head/tail**

Output the first/last part of a file


### **grep**

print lines matching the specific pattern

### **$(...)**

In a command, running contents in `()` firstly 

### **``**

Suppress all expansions

### **""**

Perform all expansions


### **chmod**

Change permissions of the file, `chmod: ugoa+rwx, 777`
(e.g, `chmod 777 test_file`)

**su/sudo**

Enter super user mode

### **vim ~/.bashrc**

modifying startup files to customize the environment, and using `source ~/.bashrc` to activate changes

### **find**

Search for files in a directory hierarchy.

Some examples:

~~~
find ~ -type f -name "filename" 
find ~ -type f -name "*.JPG" -size +1M
find ~ -type f -iname "filename" 
find ~ -type f -not -name "filename" 
find . -type d
find ~ -perm -664 -mtime 5
find . -print -delete
~~~

### **touch**

This command is usually to set or update the access, change, and modify times of files. However, if a filename argument is that of a nonexistent file, an empty file is created.

## Troubleshooting

### ...

placeholders

# Moving and Rename Files and Directrories

### Standard Command
`$ mv source destination`

### Move File to Directory:
`$ mv file-name directroy-name`

### Move File to File (Overwriting):
`$ mv file-name file-name`

### Rename File:
`$ mv file-name new-and-not-existing-file-name`

### Move Directory to Directory:
$ mv directory-name directory-name

### Rename Directory:
`$ mv directory-name new-and-not-existing-directory-name`

>Note: if the file or directory not in the current path we use the relative path name for the file-name or directory-name

----------

# Reading Files Throug The Shell

### cat Command
`$ cat file_name`
=> cat shows the content of a file without the accessability of navigation or searching through the file.

### more Command
`$ more file_name`
=> more views the content of a file and give you the accessability of navigation and searching

### less Command
`$ less file_name`
=> less views the content of a file and give you the accessability of navigation and searching (with Arrows Navigation in a plus)

** You can search on less or more by '/pattern' and using n for the next result and b for previous result
** You can use Enter for to forward a line and B for backward a line

### grep Command
`$ grep pattern file_name`
=> grep search and filter for the pattern throug the file and print it

----------

# file permissions

```
  r     w       x
  4     2       1
read  write  execute
```

There is three categories of permissions:

1. for owner (file owner).
2. for group (primary group).
3. for others (any one else).

`chmod`\
change file mode

`chmod 100 directory/`\
can read and change directory name, but cannot read subdirectories inodes.

`chmod 200`\
can read and change directory name, and also can read subdirectories inodes.

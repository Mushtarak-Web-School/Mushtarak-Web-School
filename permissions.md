# permissions

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
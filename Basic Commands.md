# Hello Linux!

### This is the first time you will be writing a linux command.

press ``ctrl + alt + t`` and you will get into the terminal.

- ``who`` command tell us about who is logged into the system right now.
- ``uname - a`` prints information about the system. ``-a``  is called an option in this case.
- ``man uname`` get the manual of ``uname``, which is an argument in this case.
- ``whoami`` prints whos the current user.
- ``passwd`` allows us to change the current user's password.
- ``pwd`` present working directory.
- ``cd`` to change dirictory.
- ``ls`` listing present working directory files.
- ``ls -l`` long listing files.
- ``mkdir`` makes a new directory.
- ``rmdir`` remove a directory (only if it's empty).
- ``tree`` listing contents of all directories in a tree-like format.
- we use ``echo`` command to print text on the screen.
- ``exit`` to exit the shell.

### commands types:
- programs.
- aliases.
- shell (internal commands).

### The main parts of this course:
- files.
- processes.
- users.
- groups.

Files: is an ordered collection of data, is addressable.

contains UTF encoding (0:4 billion chars).

File name could contain any character except ``/`` sign because it represents the root file in the system.

### There are two kinds of paths:
- absolute path like: ``/home/name/``.
- relative path like: ``music/``.

### Type of files:
Try the command ``ls -l`` in the terminal, you will get a long listing of the current directory.

In the first row there is a charachters, the first character determine the type of the file:
- ``b`` for a block.
- ``d`` for a directory.
- ``-`` is a regular file.
- ``l`` is a link to file.
- ``c`` is a character sequence.

### Notes:
- ``~`` this symbol called (telda) and represnts the user home directory.
- ``./`` is a refrence to the current directory.
- ``../`` is a refrence to the parent directory.

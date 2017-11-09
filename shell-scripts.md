# Shell script

shell script simply is some commands in a file, and the shell interprate it line by line untile the end of the file.

> Ask yourself, how can we make the shell read from a file insted of STDIN?
we may use ridiraction. let's try write a script and run it.

```bash
$ cat < myfirstscript.sh
ls -l /etc
cat /etc/passwd
who
uname -a
echo "Done with this shell"
```

then run it like this

```bash
$ bash < myfirstscript.sh
```

## Variables

Variables are named memory locations.\
In shell any variable is string.

To declear a variable

```bash
$ MYNAME="Ahmed Hussien"
```

and to call it

```bash
$ echo $MYNAME
```

> How many data types do we have?

there is 3 main types

- strings
- numiric
- boolian

these types called simple data types

What if we want to concatenate 1 to the variable value when we print it,
if this is the varible and its type

```bash
$ MYNAME="Ahmed Hussien"
# we want to print it like this
# Ahmed Hussien1
```

Can we print it like this?

```bash
$ echo $MYNAME1
```

the answer is

```bash
$ echo ${MYNAME}1
Ahmed Hussien1
```

If we want to run the script like any programe without wrinting "bash".
we use hash bang #! some times called shbang or she bang.
let's edit `myfirstscript.sh` to be like this.

```bash
#!/usr/bin/bash
$ cat < myfirstscript.sh
ls -l /etc
cat /etc/passwd
who
uname -a
echo "Done with this shell"
MYNAME="Ahmed Hussien"
echo ${MYNAME}
echo ${MYNAME}1
```

then make it executable and run it.

```bash
$ chmod 755 myfirstscript.sh
$ ./myfirstscript.sh
```

## Shell modes

1- Non-interactive shell

It knows that it reads from a file.

```bash
$ bash myfirstscript.sh
```

2- Interactive shell

It is the defult mode, and when it run a script, it think that it
reads from STDIN.

```bash
$ bash < myfirstscript.sh
# and
$ ./myfirstscript.sh
```

The interactive shell has two types

- login interactive shell
- non-login interactive shell

```bash
$ ps
 PID TTY          TIME CMD
 7265 pts/0    00:00:00 -bash
 7332 pts/0    00:00:00 ps
```

```bash
$ ps
 PID TTY          TIME CMD
 7265 pts/0    00:00:00 bash
 7332 pts/0    00:00:00 ps
```

## Parameters and Arguments

```bash
$ cat >> myfirstscript.sh
echo My name is $0
echo first argument is $1
echo second argument is $2
```

then run it

```bash
$ ./myfirstscript.sh Hello world
...
...
My name is myfirstscript.sh
first argument Hello
second argument world
```

## Variables types

Any processes inherate

- ENV variables
- Non-ENV variables

## For loop

With loops we can use one statement or more, more than one time.

Lets see the syntax of for loop.

write the folowing script

```bash
#!/usr/bin/bash
for i in Hello There Who are you
do
    echo "The variable i has the value" ${i}
done
```

In the first line, for and in are keywords, i is a varible, and (Hello There Who are you) are the values which assines to i. in the next lines do and done are keywords, the for loop will repeat any commands between them.

lets run it.

```bash
The variable i has the value Hello
The variable i has the value There
The variable i has the value Who
The variable i has the value are
The variable i has the value you
```

In the first time for assained Hello to i, and in the second time it assained There to i, and so on until it reached to the last value then it finshed the loop.

Try to change the first line to be like this

```bash
for i in "Hello There" "Who are you"
```

## comments

Any line starts with # the shell will ignore it. like this

```bash
echo "Hello there"
#echo "Who are you"
```

You can use comments to document your script or to make shell ignore
something.

## If statement

> read chapter 7 in [Bash Guide for Beginners](http://www.tldp.org/LDP/Bash-Beginners-Guide/html/index.html)

## Reading from files

```bash
#!/usr/bin/bash
for i in $(cat names.list)
do
    echo "Hello $i"
done
```

```bash
#!/usr/bin/bash
exec 4<names.list
while true
do
    read -u 4 i
    echo "Hello $i"
done
```

> ex. to cheak the errors.txt file if there is duplicate error ids that have
> diffrent error description

## Refrences

If you want to get deeper, you can use these refrences

1- [The Linux Command Line](http://www.linuxcommand.org/)

2- [Bash Guide for Beginners](http://tldp.org/LDP/Bash-Beginners-Guide/html/)

3- [Advanced Bash-Scripting Guide](http://tldp.org/LDP/abs/html/)
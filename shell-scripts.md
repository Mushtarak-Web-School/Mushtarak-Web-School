# Shell script

shell script simply is some commands in a file, and the shell interprate it line by line untile the end of the file.

> Ask yourself, how can we make the shell read from a file insted of STDIN?
we may use ridiraction. let's try write a script and run it.

```bash
cat < myfirstscript.sh
ls -l /etc
cat /etc/passwd
who
uname -a
echo "Done with this shell"
```

then run it like this

```bash
bash < myfirstscript.sh
```

## Variables

Variables are named memory locations.\
In shell any variable is string.

To declear a variable

```bash
MYNAME="Ahmed Hussien"
```

and to call it

```bash
echo $MYNAME
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
MYNAME="Ahmed Hussien"
# we want to print it like this
# Ahmed Hussien1
```

Can we print it like this?

```bash
echo $MYNAME1
```

the answer is

```bash
echo ${MYNAME}1
```

If we want to run the script like any programe without wrinting "bash".
we use hash bang #! some times called shbang or she bang.
let's edit `myfirstscript.sh` to be like this.

```bash
#!/usr/bin/bash
cat < myfirstscript.sh
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
chmod 755 myfirstscript.sh
./myfirstscript.sh
```

## Shell types

## Parameters and Arguments

```bash
cat >> myfirstscript.sh
echo My name is $0
echo first argument is $1
echo second argument is $2
```

then run it

```bash
./myfirstscript.sh Hello world
```

## Variables types

## For loop

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
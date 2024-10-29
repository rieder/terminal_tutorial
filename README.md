# Introduction to the terminal

In this tutorial you will practice using the terminal.

## Step 1: download

First, open a terminal on your computer.
Create a new directory for this tutorial:
```sh
mkdir $(PWD)/terminal_tutorial
```
**Question:** what does `$(PWD)` mean here?


Move from the working directory to this new directory:
```sh
cd $(PWD)/terminal_tutorial
```

Then, download the contents of this tutorial there:
```sh
wget https://github.com/rieder/terminal_tutorial/archive/refs/heads/main.tar.gz
```

And unpack the contents:
```sh
tar xvf main.tar.gz
```
**Question:** what does `xvf` mean here? Try `tar -h` or `tar --help` to find out.

## Step 2: move files

List the contents of the directory:
```sh
ls
```

Move the contents of the `terminal_tutorial-main` directory into the current working directory.
First, type:
```sh
mv ter
```
Then press the `tab` key to complete the directory name, specify you are moving all files (`*`), and enter the current directory as (`./`) as the destination:
```sh
mv terminal_tutorial-main/* ./
```

## Step 3: 

Find the path of file named `this_file`
```sh
find ./ | grep this
```
**Note:** try running `find ./` and `grep this` on their own to find out what they do. To exit `grep`, use `^C` (control + c).

See what file type the file is:
```sh
file (FILENAME)
```

Now show its contents:
```sh
cat (FILENAME)
```

## Final step: create a log

Write the last 10 commands to a log file:
```sh
history | tail -n 10 > COMMANDLOG.txt
```
To add this last history command to the log as well:
```sh
history | tail -n 1 >> COMMANDLOG.txt
```

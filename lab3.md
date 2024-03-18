## Lab 3: Understanding terminal commands


### Q1. You have just logged in. Enter the command to display the current working directory

```
pwd
```

### Q2. Create a directory dir1 under the user's HOME directory

```
pwd
mkdir dir1
```

### Q3. Enter the command to change to the directory dir1.

```
cd dir1
```

### Q4. Create a file file3.doc under the directory dir1. Enter the text "Welcome to the Unix session".

```
touch file3.doc
echo "Welcome to the Unix session" > file3.doc
```

### Q5. Create another directory under the user's HOME directory called dir1bkp.

```
mkdir dir1bkp
```

### Q6. Create a file file2.doc in dir1bkp directory from your current directory.

```
touch dir1bkp/file2.doc
```

### Q7. Navigate to the directory /home. Use both relative path names and absolute path names.

```
cd /home/gibin/dir1
cd ~/dir1
```

### Q8. Enter the command to change to the user’s HOME directory directly.

```
cd
```

### Q9. List all the files in the current directory.

```
ls
```

### Q10. Create directories temp1 and subdirectories temp1a and temp1b under temp1 with one appropriate command.

```
mkdir temp1 temp1/temp1a temp1/temp1b
```

### Q11. List the commands you had executed so far since your last login. Save them in a file MyHist.

```
history > myhist
```

### Q12. Clear the history in your terminal.

```
history -c
```
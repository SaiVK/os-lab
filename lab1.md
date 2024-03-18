## Lab 1: Understanding grep

### Grep tool
```
grep [options] pattern [files]
```

### Create a text file(file1.txt) with the following content:
```
boot
book
booze
machine
boots
bungie
bark
aardvark
broken$tuff
robots
```

### Q1. Print out every line that contains the word 'boo'

```
grep -e "boo" file1.txt
```

### Q2. If you were working with a large file, what way you could track down a particular string more easily, if you needed to open the file in an editor to make some changes

```
grep -e "boo" file1.txt
```

### Q3. Print every line that does not contain the string "boo"

```
grep -v -e "boo" file1.txt
```

### Q4. Print every line that does not contain the string "boo" and display with the line numbers

```
grep -v -n -e "boo" file1.txt
```

### Q5. Display the number of occurences of "boo" in the file.

```
grep -c -e "boo" file1.txt
```

### Q6. Search the file for lines ending with the letter e

```
grep  "e$" file1.txt
```

### Q7. Search for boot or boots from the file

```
grep  -e "boot" file1.txt
```

### Q8. Search for boot from the file

```
grep  -w "boot" file1.txt
```

### Q9. Search the file for lines ending with the letter e

```
grep "^u" file1.txt
```


### For further commands, have a look at this website and try practising commands: [Grep tool](https://www.geeksforgeeks.org/grep-command-in-unixlinux/#5-displaying-only-the-matched-pattern-using-grep)
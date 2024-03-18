## Lab 4: Understanding cut

### Cut tool
```
cut OPTION... [FILE]...
```

### Create a text file(file4.txt) with the following content:
```
singh~manju~222~12 preethi apartments, Chennai 90~mktg~a2~7890
kanetkar~viji~223~22 N H road , Chennai~accts~s2~6782
shah~parul~224~viji apartments, delhi~pers~s5~7653
garg~kripa~225~ram garh, delhi~mktg~s1~4733
weeling~preethi~226~43 meena sadan~accts~a3~4894
iyer~kamala~227~11 crescent apt~mktg~s8~2234
randive~ketan~228~11 crescent apt~mktg~s8~2236
nadkarni~girish~229~34 manju lane~pers~s5~6754
kottori~divya~230~shell colony~accts~a2~6543
kulkarni~makrand~231~dadar house~a6~9999
```

### Q1. List only first 10 bytes/characters from the file in each line

```
cut -c -10 file4.txt
cut -b -10 file4.txt
```

### Q2. List only  2nd to 3rd bytes/characters from the file in each line

```
cut -c 2-4 file4.txt
cut -b 2-4 file4.txt
```

### Q3. List only the firstname,grade and depcode for the employees 

```
cut -d "~" -f 2,5,6 file4.txt
```

### Q4. List the depcode,lastname of all employees

```
cut -d "~" -f 5,1 file4.txt
```

### Q5. Display details of first three employees

```
head -n 3 file4.txt
```

### Q6. Display details of last three employees

```
tail -n 3 file4.txt
```

### For further commands, have a look at this website and try practising commands: [Cut tool](https://www.geeksforgeeks.org/cut-command-linux-examples/)
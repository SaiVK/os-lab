## Lab 2: Understanding awk

### Awk tool
```
awk options 'selection _criteria {action }' input-file > output-file
```

### Create a text file(file2.txt) with the following content:
```
chr2 74711 127472363 Pos1 0 +
chr3 74723 127473530 Pos2 0 +
chr1 73530 127474697 Pos3 0 +
chr2 17469 127475864 Pos4 0 +
chr3 12747 127477031 Neg1 0 -
chr5 17477 127478198 Neg2 0 -
chr7 74781 127479365 Neg3 0 -
chr7 74795 127480532 Pos5 0 +
chr1 12748 127481699 Neg4 0 -
```

### Q1. How can you get a list of all distinct chromosomes(column 1)?

```
awk '{print $1}' file2.txt  | sort | uniq
```

### Q2. Read the 7th line from the above file

```
awk 'NR==7 {print $0}' file2.txt
```

### Q3. How can you create another file that contains only reads from the - strand(6th column in the file)?

```
awk '$6=="-" {print $0}' file2.txt  > neg_strand.txt
```

### Q4. To print the length of the longest line?

```
awk '{ if (length($0) > max) max = length($0) } END { print max }' file2.txt
```

### Q5. Display the number of times "chr7" is present in the file.

```
grep -c -e "chr7" file2.txt
```

### Q6. To count the lines in a file
```
awk 'END { print NR }' file2.txt 
```



### For further commands, have a look at this website and try practising commands: [Awk tool](https://www.geeksforgeeks.org/awk-command-unixlinux-examples/)
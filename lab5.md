## Lab 5: Understanding sort

### Create a text file(file5.txt) with the following content:
```
harry potter and the order of phoenix~rowling~756
operating system concepts~silberschatz~256
unix concepts~das~234
linux concepts~das~435
operating system concepts~stalling~765
harry potter and the half blood prince~rowling~856
harry potter and the prisoner of azkaban~rowling~768
unix - an introduction~galvin~234
```


### Q1. Display the Book name and price

```
cut -d "~" -f 1,3 file5.txt
```

### Q2. Display the Book name and price, without "~" delimiter symbol, but with "::: Rs."

```
cut -d "~" -f 1,3 file5.txt --output-delimiter="::: Rs."
```

### Q3. Cut the book name store it as file and then cut the price, store it as a file, combine both the files without delimiter

```
cut -d "~" -f 1 file5.txt > book5.txt
cut -d "~" -f 3 file5.txt > price5.txt
paste book5.txt price5.txt > book_price5.txt
```

### Q4. Sort the file and store it in a file

```
sort file5.txt > sorted_file5.txt
```


### Q5. Check whether the file is sorted

```
sort -c file5.txt
```

### Q6. Sort the file on price

```
sort -t "~" -k3n file5.txt
```

### Q7. Sort the file on price in reverse order

```
sort -t "~" -k3nr file5.txt
```

### Q8. Sort the file in the order of author and within author on price

```
sort -t "~" -k1,1 -k3,3n file5.txt
```

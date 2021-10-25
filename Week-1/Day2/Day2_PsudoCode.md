### Patterns Questions
-----
```Python
'''
print this pattern
   *
  ***
 *****
*******
'''
```
-----
> Observation Seen In The Pattern

| Row ( N ) | Space     | Stars ( * )|
|-----------|-----------|------------|
| 1         | 3         |1           |
| 2         | 2         |3           |
| 3         | 1         |5           |
| 4         | 0         |7           |
| N|(N-i)|(2*N-1)|
------
### **Sudo Code**
1. Take  Input Of Number of Rows (N)
2. CurrentIndex = 1
3. While CurrentIndex <= N
   1. space = 1
   2. while (space <= N-CurrentIndex)
      - print(" ")
      - increase space by 1
   3. stars = 1
   4. while ( stars <= (2*CurrentIndex -1))
      - print("*)
      - increase stars count by 1
   5. Increse The CurrentIndex Count by 1
   6. print a new line
4. end
***
 * Main While Loop starts from 1 - N
   * First While Loop to print the spaces till 1 to N-CurrentRowIndex
   * Second While Loop to Print * till 1 to (2*currentRowIndex-1) times

--------
   

```Python
rows=int(input("Enter Number Of Rows : "))

def print_pattern(N):
    row=1
    while(row<=N):
        #print Spaces
        space = 1
        result=""
        while(space<=N-row):
            result+=" "
            space+=1
        #print stars
        stars = 1
        while(stars <= 2*row-1):
            result+="*"
            stars+=1
        print(result)
        row+=1
#Driver Code
print_pattern(rows)
```

```Python
'''
print this pattern
*
***
*****
*******
'''
```

```Python
'''
print this pattern
1
1 2
1 2 3
1 2 3 4
1 2 3 4 5
'''
```
```Python
'''
print this pattern
1
2 3
4 5 6
7 8 9 10
'''
```


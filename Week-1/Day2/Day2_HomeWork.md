### **HomeWork 2**
---
```Python
'''
print this pattern
    1
   232
  34543
 4567654
567898765
'''
```
#### **Observation**
---
| Row ( N ) | Space     | Total Numbers| Numbers |
|-----------|-----------|------------|------------|
| 1         | 4         |1           | 1
| 2         | 3         |3           | 2,3,2
| 3         | 2         |5           | 3,4,5,4,3
| 4         | 1         |7           | 4,5,6,7,6,5,4
| 5         | 0         |9           | 5,6,7,8,9,8,7,6,5
| N         | N-i |2*i-1 | N....2*N-1....N
---
> Psudo Code
---
1. Take Input of Total Number Row Numbers (N)
2. Take Current Index =1
3. Now Run A While Loop Till 1-N
   1. Print The Spaces
        1. take space=1
        2. run a loop till space reaches N-i
           1. print the space
           2. increase the space value by 1
   2. Print The Numbers
      1. now steps = i
      2. while(steps < 2*i-1)
         - print steps value
         - step +=1
      3. while(steps >= i)
        - print(steps)
        - steps -=1
    3. Now Print the new line
4. End   
---   
```python
def PrintNumberPyramid(N):
    index=1
    while(index<=N):
        result=""
        #print the spaces
        space=1
        while(space<=N-index): # Print spaces till N-i
            result+=" "
            space+=1
        #print the numbers 
        # first N....2*N-1
        # then 2*N-1.....N
        num=index
        while(num < 2*index-1): # prints till N....2*N-1
            result+=str(num)
            num+=1
        # last loop will make the Number to 2*N-1
        while(num >= index): # print till 2*N-1 to N
            result+=str(num)
            num-=1
        print(result)
        index +=1

# Driver Code
PrintNumberPyramid(int(input("Enter The Number : ")))
```
---
### Print this pattern

![image](full_diamond.png)
#### Print GCD (Greatest Commond Divisor) of two numbers
---  
> Psudo Code
---
1. Take input of tow numbers
2. take two integers i=1, Gcd_result =0
3. run a loop from i to minimum of these two numbers:
   1. if both the numbers are divisable by i then result is i
   2. now increase the i by 1
   3. Repeat till minimum of the both numbers
4. return the result
---

```python
def GDC(a,b):
    i=1
    gcd=1
    while(i<=min(a,b)):
        if (a%i== 0) and (b%i == 0):
            gcd=i
        i+=1
    return gcd 

res = GDC(int(input("Num1 :")),int(input("Num2 :")))

print(res)
```

### Print LCM (Least Common Multiplier) of two numbers

```bash
Math Formula : GDC * LCM = Number1 * Number2
```
---
```python
def GCD(a,b):
    i=1
    gcd=1
    while(i<=min(a,b)):
        if (a%i== 0) and (b%i == 0):
            gcd=i
        i+=1
    return gcd 

def LCM(a,b):
    return (a*b)/GDC(a,b)

result=LCM(10,5)
```

## Day1 : FlowCharts
---
#### Sum Of Digits Of a Number
---  
> Psudo Code
---

1. Take Input of The number
2. Initialize SumOfDigits = 0
3. Run A a loop will the Number does'nt turns to zero
   - Add the reminder of the number by dividing by 10 in to SumOfDigits
   - Modify The Number by getting rid of the last digit ( Num = Num /10 )
4. Return The Sum    

```python
def SumOfDigits(Num):
    sum = 0
    while(Num != 0):
        sum+= Num%10
        Num = Num//10
    return sum
```
----
#### Swap Two Numbers
----
> Psudo Code :
**With Out Third Variable**
1. Take Input Of Two numbers : Num1, Num2
2. Add The Numbers Like This : Num1 = Num1+Num2
3. Num2 = Num1-Num2
4. Num1 = Num1-Num2
5. return the swapped values of Num1, Num2
```python
def SwapTwoNumbers(Num1, Num2):
    Num1=Num1+Num2
    Num2=Num1-Num2
    Num1=Num1-Num2
    return Num1,Num2

a,b=SwapTwoNumbers(int(input("Enter First Number :")),int(input("Enter Second Number :")))

print("Swapped Numbers :",a,b)

```
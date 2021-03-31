# Cmubomb
## Phase 1:

Our input is compared with 
```
"Public speaking is very easy."
```

## Phase 2:
If we look into function check we can find we need to input 6 integers in such a way that first number i.e a[0] is 1 then it follows a[i]=(i+1)*a[i-1].
a[1]=2*1=2
a[2]=3*2=6
a[3]=4*6=24
a[4]=5*24=120.
a[5]=6*120=720
so for 2nd phase our input is ```1 2 6 24 120 720```.


## Phase 3:
Here we need to input format as "%d %c %d"
here combinations for 2nd and 3rd inputs are:
q 777
b 214
b 755
k 251
o 160
t 458
v 780
x 524
Trying different input values for each I found that it is a switch case statement if it first integer is 0 it is checking character and next integer as q and 777.


## Phase 4:
Here we can see that function 4 is recursive function.
```
int func4(value)
if (value is less than 1)
	eax=1
else
	p=func4(value-1)
	q=func4(value-2)
	eax=p+q
return eax
```
And final eax is getting compared with 0x37 i.e 55 so we need to check for which value we get 55 we can see that for value=9 return value is 55 so our input is 9.


## Phase 5:
Here we have 2 strings "isrveawhobpnutfg\260\001" and "giants".We will be taking index of characters of 2nd string in first like g has index 15 in 1st string all these indices are anded with 15 and that result is getting compared with "giants".Here is small python code to get input:
```
s=[15,0,5,11,13,1]
for i in s:
    for j in range(33,126):
        if ((j & 15) == i):
            print(chr(j),end=" ")
    print("")
```
Output:
/ ? O _ o 
0 @ P ` p 
% 5 E U e u 
+ ; K [ k { 
- = M ] m } 
! 1 A Q a q
Here we can take any of the character from 1st line for 1st character and so on.OPEKMA,o@5m1,opU[]Q....


## Phase 6:
- Here first we need to input 6 numbers.
- First loop checks if our input-1 is less than 5.
- Next for loop checks if number is repeating or not.So our input should be 1,2,3,4,5,6 in some order.
- The order we need to input is given by next loop using nodes.
- Finally our input is 
	```4 2 6 3 1 5```



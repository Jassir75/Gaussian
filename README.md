# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
### Step 1:
import numpy as np
### Step 2:
import sys
### Step 3:
get input from the user
### Step 4:
calculate the X0, X1 and X2 values by Gaussian elimination.
### Step 5:
print the values
### Step 6:
End the program
## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: Jassir Sulthan 
RegisterNumber: 212224240060
*/
import numpy as np
n=int(input())
ar=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        ar[i][j]=int(input())
for i in range (n):
    for j in range (i+1,n):
        ratio=ar[j][i]/ar[i][i]
        for k in range (n+1):
            ar[j][k]=ar[j][k]-ratio*ar[i][k]
x[n-1]=ar[n-1][n]/ar[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=ar[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-ar[i][j]*x[j]
    x[i]=x[i]/ar[i][i]
for i in range (n):
    print("X%d = %0.2f"%(i,x[i]),end=" ")
```

## Output:
<img width="1262" height="883" alt="image" src="https://github.com/user-attachments/assets/df6c1607-4d5f-427d-8c47-f4af5dcab9df" />



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.


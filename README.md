# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
### Step 1: 
Enter the number of equations.
### Step 2:
Input the augmented matrix (coefficients and constants).
### Step 3: 
Convert the matrix to upper triangular form using row operations.
### Step 4: 
Eliminate variables below the diagonal.
### Step 5: 
Start back substitution from the last equation.
### Step 6:
Solve for each variable moving upward
### Step 7: 
Print the values of all variables.
## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: Pragatheeshraaj D
RegisterNumber: 212224230199
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][i]==0.0:
        sys.exit("Divide by zero detected!")
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]

for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
        
    x[i]=x[i]/a[i][i]
    
for i in range(n):
    print('X%d = %0.2f'%(i,x[i]),end=' ')
*/
```

## Output:
![Screenshot 2025-04-25 181750](https://github.com/user-attachments/assets/ba6c3047-7140-4adb-a58e-3924eb286924)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.


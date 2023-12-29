# Gaussian Elimination
### Name: Anbuselvan.S
### Reference No: 23005959
## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
Import the numpy module and sys module to use the built-in functions for calculation 
Get the size of the matrix from user and create empty matrix and vector
using for loop get elements for matrix and vector
Using another for loop to take each element in the matrix
solve row echelon form
perform back substitution
print the value in two decimal points 
End the program

## Program:
```
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: Anbuselvan.S
RegisterNumber: 23005959
'''
import numpy as np
import sys 
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)

for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][j]==0.0:
        sys.exit("divided by zero detected")
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
        print("X%d = %0.2f"%(i,x[i]),end=' ')
```

## Output:
![image](https://github.com/anbuselvan1519/Gaussian/assets/139841744/fe7cca7d-f703-4b81-bfb3-64072b8b68df)

## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.


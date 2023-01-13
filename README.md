# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Get the input from the user
2. The rows and columns can be defined by n,n+1
3. Declearing the range value for the matrix
4. 

## Program:
```
'''Program to solve a matrix using Gaussian elimination with partial pivoting.
Developed by: S.Kishore
RegisterNumber: 22008388
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
    if a[i][i]==0.0:
        sys.exit('Divide by zero detected!')
    for j in range(i+1,n):
        ratio =a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    
    for j in range(i+1,n):
        x[i]=x[i] -a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f' %(i,x[i]),end = ' ')

```

## Output:
![gaussian 3](https://user-images.githubusercontent.com/118679883/212273103-bb44c341-5b71-4ff7-a5c4-879ed7146ce5.png)
![gaussian 4](https://user-images.githubusercontent.com/118679883/212273160-63db226f-f1ca-4e05-9fba-bf9a032e418e.png)




## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.


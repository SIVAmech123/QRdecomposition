# Algorithm for QR Decomposition
## Aim:
To implement QR decomposition algorithm using the Gram-Schmidt method.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Intialize the matrix Q and u
2.	The vector u and e is given by

    ![eqn1](./ex4.jpg)

    ![eqn2](./ex6.jpg)

    ![eqn3](./ex3.jpg)

3.	Obtain the Q matrix   
    ![eqn4](./ex1.jpg)
4.	Construct the upper triangular matrix R
    ![eqn5](./ex2.jpg)



## Program:
### Gram-Schmidt Method
```
''' 
Program to QR decomposition using the Gram-Schmidt method
Developed by: sivakumar R
RegisterNumber: 23013501
'''
import numpy as np

def QR_Decomposition(A):

    n, m = a.shape

    q = np.empty((n,n))

    u = np.empty((n,n))

    u[:,0] = a[:,0]

    q[:,0] = u[:,0]/np.linalg.norm(u[:,0])

    for i in range(1,n):

        u[:,i]=a[:,i]

        for j in range(i):

            u[:,i]-=(a[:,i]@ q[:,j])* q[:,j]

        q[:,i] = u[:,i] / np.linalg.norm(u[:,i])

    r = np.zeros((n,m))

    for i in range(n):

        for j in range(i,m):

            r[i,j] = a[:,j] @ q[:,i]

    print(q)

    print(r)
    
    
    
a = np.array(eval(input()))

QR_Decomposition(a)






```

## Output
<img width="570" alt="Screenshot 2024-04-06 215459" src="https://github.com/SIVAmech123/QRdecomposition/assets/151629067/8804325a-5c1f-42ee-9c45-cec18d1d3a3a">



## Result
Thus the QR decomposition algorithm using the Gram-Schmidt process is written and verified the result.

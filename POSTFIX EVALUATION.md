# Exp.No:13c
## POSTFIX EVALUATION - Implementation of Tower of Hanoi Problem Using Recursion in Python

### AIM  
To recursively solve the Tower of Hanoi puzzle by transferring n disks from a source rod to a target rod, using an auxiliary rod, while obeying the rules of disk movement.
### ALGORITHM
```
1.Input the number of disks n.
2.Define a recursive function TowerOfHanoi(n, source, destination, auxiliary):
     ->If n > 0:
        1.Move n-1 disks from source to auxiliary rod.
        2.Move the largest disk (nth disk) from source to destination rod.
         3.Move n-1 disks from auxiliary to destination rod.
3.Call the function with the initial rods named 'A', 'C', and 'B'.
4.Print each move of the disks during execution.
```
### PROGRAM

```
def TowerOfHanoi(n , source, destination, auxiliary):
    if (n>0):
         TowerOfHanoi(n-1,source,auxiliary, destination)
         print("Move disk from",source,"to",destination)
         TowerOfHanoi(n-1,auxiliary, destination,source)
n=int(input())
print("No. of disks =",n)

```

### OUTPUT
<img width="1180" height="846" alt="image" src="https://github.com/user-attachments/assets/c2c65a67-09ea-4251-accf-99549c14e2fc" />


### RESULT
->The program prints all moves required to transfer the disks from the source rod to the destination rod.

->Demonstrates recursion and the divide-and-conquer strategy effectively.

# Exp.No:13a 
## CONVERSION OF INFIX TO POSTFIX - Implementation of Stack Operations Using Python

### AIM  
To demonstrate the basic operations of a stack data structure—push, pop, and peek—using Python.
### ALGORITHM
```
1.Start by creating an empty stack using a Python list.
2.Define a class st with methods to manipulate the stack:
  ->Push method:
      Accept input elements.
      Add each element to the top of the stack using append().
  ->Pop method:
      Remove the top element using pop() if the stack is not empty.
      Display the removed element.
      If stack is empty, display a warning.
   ->Peek method:
      Display all current elements in the stack without removing them.
3.Take input from the user (string or list of elements).
4.Call push() to insert the elements into the stack.
5.Call peek() to show the current stack elements.
6.Call pop() to remove the topmost element.
7.Call peek() again to display the updated stack.
```
### PROGRAM

```
stack = []
class st:
    def push(self,S):
        for i in S:
            stack.append(i)
        return
    def pop(self):
        if stack:
            print("Element popped : ",stack.pop())
        else:
            print("The stack is empty")
        return 
    def peek(self):
        print("Elements in the stack \n",stack)
        return 
s=st()
l=input()
s.push(l)
s.peek()
s.pop()
s.peek()
```

### OUTPUT

<img width="1177" height="283" alt="image" src="https://github.com/user-attachments/assets/5b81fb7d-acb0-46af-9841-9b073e4ea004" />

### RESULT

->The program correctly demonstrates stack behavior.

->Input elements are added to the stack in order.

->The top element is removed during pop().

->peek() reflects the current state of the stack.

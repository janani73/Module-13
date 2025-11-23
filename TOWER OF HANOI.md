# Exp.No:6e 
## SEB - Stack Operations Using Python with Odd Numbers

### AIM  
To demonstrate stack operations (push, pop, peek) by storing and manipulating odd numbers from 1 to n-1 using a Python list and class.
### ALGORITHM  
```
1.Input a number n from the user.
2.Generate a list l of all odd numbers from 1 to n-1.
3.Create a class st with methods:
    ->push(l): Add all elements of list l to the stack using extend().
    ->pop(): Remove and print the top element of the stack using pop().
   -> peek(): Display all current elements in the stack.
4.Create an object of class st.
5.Push the list of odd numbers to the stack using push().
6.Display the stack using peek().
7.Pop the top element using pop().
8.Display the updated stack using peek().
```
### PROGRAM  

```
stack = []
class st:
    def push(self,l):
        stack.extend(l)
    def pop(self):
        print("Element popped : ",stack.pop())
    def peek(self):
        print("Elements in the stack\n",stack)
n=int(input())
l=[i for i in range(1,n) if i%2!=0]
s=st()
s.push(l)
s.peek()
s.pop()
s.peek()
```

### OUTPUT
<img width="1195" height="360" alt="image" src="https://github.com/user-attachments/assets/9b908f4f-18c4-488e-b72a-72d964505c10" />


### RESULT
->The program successfully stores odd numbers in a stack and demonstrates LIFO behavior.

->peek() shows the current stack elements.

->pop() removes the topmost element correctly.

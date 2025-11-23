# Exp.No:13b  
## IMPLEMENTATION OF STACK - Conversion of Infix Expression to Postfix Expression Using Python

### AIM  
To convert a mathematical expression from infix notation (operators between operands) to postfix notation (operators after operands) using the stack data structure and operator precedence rules.
### ALGORITHM
```
1.Initialize an empty stack and an empty output string.
2.Iterate through each character of the input expression:
     If the character is an operand, append it directly to the output string.
     If the character is '(', push it onto the stack.
     If the character is ')', pop from the stack and append to output until '(' is found; discard '('.
     If the character is an operator (+, *, ^):
         -> While the stack is not empty, the top is not '(', and the priority of the current operator is less than or equal to the top operator in the stack, pop from the stack to the output.
         -> Push the current operator onto the stack.
3.After processing all characters, pop any remaining operators from the stack and append them to the output.
4.Return the output as the postfix expression.
```

### PROGRAM

```
Operators = set(['+', '*', '^','(',')']) # collection of Operators
Priority = {'+':1,'*':2,'^':3} 
def infixToPostfix(expression): 
    stack = [] # initialization of empty stack
    output = '' 
    for character in expression:
        if character not in Operators:  # if an operand append in postfix expression
            output+= character
        elif character=='(':  # else Operators push onto stack
            stack.extend('(')
        elif character==')':
            while stack and stack[-1]!= '(':
                output+=stack.pop()
            stack.pop()
        else: 
            while stack and stack[-1]!='(' and Priority[character]<=Priority[stack[-1]]:
                output+=stack.pop()
            stack.append(character)
    while stack:
        output+=stack.pop()
    return output
expression=input()
print('infix notation: ',expression)
print('postfix notation: ',infixToPostfix(expression))
```
### Output
<img width="1183" height="220" alt="image" src="https://github.com/user-attachments/assets/358f004f-1059-4ffa-9259-1043e2550e60" />


### Result
->The program converts an infix expression into its corresponding postfix notation correctly.

->Operator precedence is maintained (^ > * > +) and parentheses are handled properly.

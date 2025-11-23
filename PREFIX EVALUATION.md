# Exp.No:6d
## PREFIX EVALUATION - Evaluation of Prefix Expressions Using Python

### AIM  
To evaluate a prefix (Polish notation) mathematical expression using a stack, performing the correct operations in the right order.
### ALGORITHM
```
1.Initialize an empty stack.
2.Iterate through the prefix expression from right to left:
    ->If the character is an operand, convert it to an integer and push it onto the stack.
    ->If the character is an operator (+, -, *, /, %, **):
           ->Pop the top two operands from the stack.
           ->Apply the operator to these operands (operand1 operator operand2).
           ->Push the result back onto the stack.
3.After processing all characters, the stack will contain the final result.
4.Pop and return the result as the evaluation output.
```

### PROGRAM

```
OPERATORS=set(['*','-','+','%','/','**']) 
def evaluate(expression):
	stack = []
	for c in expression[::-1]:
		if c not in OPERATORS:
			stack.append(int(c))
		else:
			o1 = stack.pop()
			o2 = stack.pop()
			if c == '+':
				stack.append(o1 + o2)
			elif c == '-':
				stack.append(o1 - o2)
			elif c == '*':
				stack.append(o1 * o2)
			elif c == '/':
				stack.append(o1 / o2)
	return stack.pop()
test_expression = input()
print("Prefix Expression :",test_expression)
print("Evaluation result :",evaluate(test_expression))

```


### OUTPUT
<img width="1170" height="278" alt="image" src="https://github.com/user-attachments/assets/430be5af-4942-417e-abe0-b50c7c107eb0" />

### RESULT
->The program evaluates any valid prefix expression correctly.

->It uses a stack-based approach to handle operator precedence implicitly.

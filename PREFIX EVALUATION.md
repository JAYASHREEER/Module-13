![image](https://github.com/user-attachments/assets/e1a74fc7-af70-4623-8702-671ca7b4cc07)Exp.No:34  
PREFIX EVALUATION

AIM  
To write a Python program to evaluate a user-given Prefix expression using a stack. The expression must contain operators such as Multiplication, Addition, and Subtraction.

ALGORITHM

1.Start.
2.Read the prefix expression as a string input.
3.Reverse the expression (since prefix is evaluated right to left).
4.Initialize an empty stack.
5.Traverse each character (token) in the reversed expression:
If the token is a digit:
Convert it to integer and push it onto the stack.
If the token is an operator (+, -, or *):
Pop the top two values from the stack (op1 and op2).
Apply the operation:
If +: result = op1 + op2
If -: result = op1 - op2
If *: result = op1 * op2
Push the result back onto the stack.
6.After all tokens are processed, the top of the stack will contain the final result.
7.Print the prefix expression and the evaluation result.
8.End.

PROGRAM
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

			
	return stack.pop()




test_expression = input()
print("Prefix Expression :",test_expression)
print("Evaluation result :",evaluate(test_expression))

OUTPUT
![image](https://github.com/user-attachments/assets/f7a55d47-e39e-49c4-9296-c019977785ff)

RESULT
Thus,the Python program to evaluate a user-given Prefix expression using a stack. The expression must contain operators such as Multiplication, Addition, and Subtraction was successfully implemented and verified.

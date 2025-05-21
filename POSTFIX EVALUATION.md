Exp.No:33  
POSTFIX EVALUATION

AIM  
To write a Python program to evaluate a user-given Postfix expression that contains Multiplication and Addition operators using the stack concept.

ALGORITHM
1.Start.
2.Read the postfix expression as a string.
3.Initialize an empty stack.
Traverse each character (token) in the postfix expression:
If the token is a digit, convert it to integer and push it onto the stack.
If the token is an operator (+ or *):
4.Pop the top two elements from the stack (say op2 and op1).
Apply the operator: result = op1 + op2 or op1 * op2.
Push the result back onto the stack.
5.After the loop ends, the top element in the stack is the final result.
6.Display the result.
7.End.
 
PROGRAM
OPERATORS=set(['*','+']) 


def evaluate_postfix(expression):
    stack=[] 
    for i in expression:
        if i not in OPERATORS:
            stack.append(i)  
        
        else:
            a=stack.pop()  
            b=stack.pop()
        
            if i=='+':
                res=int(b)+int(a)  
            elif i=='*':
                res=int(b)*int(a)
            
            stack.append(res) 
    return stack[0]

expression = input()
print('postfix expression: ',expression)
print('Evaluation result: ',evaluate_postfix(expression))

OUTPUT
![image](https://github.com/user-attachments/assets/5cb3e928-85b2-4f47-8c84-8ffaf045f221)

RESULT
Thus, the Python program to evaluate a user-given Postfix expression that contains Multiplication and Addition operators using the stack concept was successfully implemented and verified.


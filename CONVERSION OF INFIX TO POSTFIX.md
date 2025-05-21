Exp.No:32  
CONVERSION OF INFIX TO POSTFIX

AIM  
To write a Python program that converts a given infix expression to a postfix expression using a dictionary to define operator precedence and a set to store the valid operators, considering only division, subtraction, and bitwise AND.

ALGORITHM
1.Start.
2.Define a dictionary to hold the precedence of operators (/, -, &).
3.Define a set to hold the valid operators.
4.Initialize an empty stack to hold operators during conversion.
5.Initialize an empty list for the postfix expression.
6.Read the input infix expression.
7.For each token in the infix expression:
If the token is an operand, append it to the postfix list.
If the token is an operator:
While the stack is not empty and the top of the stack is an operator with greater or equal precedence, pop from the stack to the postfix list.
Push the current operator onto the stack.
8.After processing all tokens, pop remaining operators from the stack to the postfix list.
9.Join the postfix list and display the result.
10.End.

PROGRAM
Operators = set(['&', '-', '/','(',')']) # collection of Operators

Priority = {'&':1,'-':2,'/':3} 
 
def infixToPostfix(expression): 

    stack = [] # initialization of empty stack

    output = '' 

    

    for character in expression:

        if character not in Operators:  # if an operand append in postfix expression

            output+= character

        elif character=='(':  # else Operators push onto stack

            stack.append('(')

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


expression = input()

print('infix notation: ',expression)

print('postfix notation: ',infixToPostfix(expression))

OUTPUT
![image](https://github.com/user-attachments/assets/73a7eacc-73b5-4122-a74d-7a86c41e38c1)

RESULT
Thus ,the program that converts a given infix expression to a postfix expression using a dictionary to define operator precedence and a set to store the valid operators, considering only division, subtraction, and bitwise AND.




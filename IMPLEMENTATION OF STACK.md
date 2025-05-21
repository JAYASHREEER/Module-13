Exp.No:31  
IMPLEMENTATION OF STACK

AIM  
To write a Python program that evaluates a user-given prefix expression using a stack, handling two-digit numbers and binary operators (+, -, *, /, %) using a function prefix_Eval(x).

ALGORITHM
1.Start.
2.Read the prefix expression as input (space-separated).
3.Split the expression into tokens (operators and operands).
4.Reverse the list of tokens (since prefix evaluation starts from the right).
5.Initialize an empty stack.
6.For each token in the reversed list:
If the token is a number:
Convert it to integer and push onto the stack.
If the token is an operator:
Pop the top two elements from the stack.
Apply the operator on them (first popped as operand1, second popped as operand2).
Push the result back onto the stack.
7.After processing all tokens, the result will be at the top of the stack.
8.Return the final result.
9.End.

PROGOPERATORS=set(['*','-','+','/'])
stack = []


    
def prefix_Eval(x):
    for c in x[::-1]:
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
    return stack[0]

m=input()
print("The prefix expression is",m)
n=m.split()
print("The result is",prefix_Eval(n))

OUTPUT 
![image](https://github.com/user-attachments/assets/bcbd5608-1e7b-4bf9-8d12-339d05b0714b)

RESULT 
Thus,Python program that evaluates a user-given prefix expression using a stack, handling two-digit numbers and binary operators (+, -, *, /, %) using a function prefix_Eval(x) was successfully implemented and verified.



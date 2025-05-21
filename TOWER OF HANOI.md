Exp.No:35  
TOWER OF HANOI

AIM  
To write a Python program to implement **Tower of Hanoi** and display all the moves of the disks using a recursive function.  
Consider the names of the tower pegs as A, B, C. Get the number of disks value from the user.

ALGORITHM  
1.Start.
2.Define a recursive function tower_of_hanoi(n, source, target, auxiliary):
3.If n == 1 (base case):
Print move: "Move disk from source to target".
Else:
4.Recursively call tower_of_hanoi(n-1, source, auxiliary, target) to move n-1 disks from source to auxiliary.
5.Print move: "Move disk from source to target" for the largest disk.
6.Recursively call tower_of_hanoi(n-1, auxiliary, target, source) to move n-1 disks from auxiliary to target.
7.Prompt the user to enter the number of disks.`
Call the function with source='A', target='C', and auxiliary='B'.
8.End.

PROGRAM  
def TowerOfHanoi(n , source, destination, auxiliary):
	
	if(n>0):
	    TowerOfHanoi(n-1, source, auxiliary, destination)
	    print ("Move disk from",source,"to",destination)
	    TowerOfHanoi(n-1, auxiliary, destination, source)

n=int(input())		
print("No. of disks =",n)
#TowerOfHanoi(n,'A','C','B')

OUTPUT
![image](https://github.com/user-attachments/assets/fd22f576-9bb4-46bf-b891-ff0069c47c55)

RESULT 
Thus, the Python program to implement **Tower of Hanoi** and display all the moves of the disks using a recursive function.  
Consider the names of the tower pegs as A, B, C. Get the number of disks value from the user was successfully implemented and verified.



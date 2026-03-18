# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
Lovely is training to become a logic wizard. She enters a gate that tests her understanding of logical conditions.

She is given two magical conditions:

hasKey – whether she has the golden key (boolean)

knowsPassword – whether she knows the secret password (boolean)

The gate then evaluates her truthfulness using logical operators:

Operator	Meaning
&&	Logical AND – both must be true
||	Logical OR– any one can be true
!	Logical NOT – reverse the result
 

Write a program that:

Accepts two boolean inputs: hasKey and knowsPassword

Displays the results of:

hasKey && knowsPassword
hasKey || knowsPassword
!hasKey
!knowsPassword
Input Format:
First line: true or false (hasKey)

Second line: true or false (knowsPassword)

Output Format:

Access with AND: <true/false>

Access with OR: <true/false>

Does NOT have key: <true/false>

Does NOT know password: <true/false>

## AIM:

To write a Java program that takes two boolean inputs (hasKey and knowsPassword) and demonstrates the use of logical operators (AND, OR, NOT) by displaying the evaluated results.

## ALGORITHM :
1.Start the program.

2.Import the Scanner class for user input.

3.Create a Scanner object to read input.

4.Read the first boolean value (hasKey) from the user.

5.Read the second boolean value (knowsPassword) from the user.

6.Evaluate logical AND:

7.Compute hasKey && knowsPassword.

8.Evaluate logical OR:

Compute hasKey || knowsPassword.

9.Evaluate logical NOT for hasKey:

Compute !hasKey.

10.Evaluate logical NOT for knowsPassword:

Compute !knowsPassword.

11.Display all results in the required format.

12.End the program.



## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: VISMAYA.V
RegisterNumber: 212224060310 
*/
```

## Sourcecode.java:
```
import java.util.Scanner;
public class Main
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        {
            boolean hasKey=sc.nextBoolean();
            boolean knowsPassword=sc.nextBoolean();
            System.out.println("Access with AND: "+(hasKey&&knowsPassword));
            System.out.println("Access with OR: "+(hasKey||knowsPassword));
            System.out.println("Does NOT have key: "+(!hasKey));
            System.out.println("Does NOT know password: "+(!knowsPassword));
            
        }
    }
}

```
## OUTPUT:

<img width="1232" height="442" alt="image" src="https://github.com/user-attachments/assets/7e9a2978-f086-48c9-b8e4-bdf4ec2077d9" />

## RESULT:
Therefore the program has been executed successfully.

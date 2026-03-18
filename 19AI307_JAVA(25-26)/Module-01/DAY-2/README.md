# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
A library charges a fine for every book returned late. For first 5 days the fine is 50 paise, for 6-10 days fine is one rupee and above 10 days fine is 5 rupees. If you return the book after 30 days your membership will be cancelled - Print ("Your Membership would be Cancelled.")

Write a program to accept the number of days the member is late to return the book and display the fine or the appropriate message.

## AIM:

To write a Java program that calculates the library fine based on the number of days a book is returned late and displays the fine amount or a cancellation message if the delay exceeds 30 days.
## ALGORITHM :
1.Start the program.

2.Import the Scanner class.

3.Create a Scanner object to take user input.

4.Read the number of late days (n) from the user.

5.Initialize a variable amt to store the fine amount.

6.Check the number of late days using conditional statements:

7.If n <= 5, then fine = 0.5 × n.

8.Else if n >= 6 and n <= 10, then fine = 1 × n.

9.Else if n > 10, then fine = 5 × n.

10.Display the fine amount using formatted output.

11.Check if n > 30:

If true, display the message: "Your Membership would be Cancelled."

12.End the program.




## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: VISMAYA.V
RegisterNumber: 212224060310
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Main
{
    public static void main(String[]args)
    {
        Scanner sc=new Scanner(System.in);
        double n=sc.nextInt();
        double amt=0;
        if(n<=5)
        amt=0.5*n;
        else if(n>=6&&n<=10)
        amt=1*n;
        else if(n>10)
        amt=5*n;
        System.out.printf("Fine Amount Pay to Rs :%.2f\n",amt);
        if(n>30)
        {
            System.out.printf("Your Membership would be Cancelled.");
        }
    }
}

```

## OUTPUT:

<img width="1214" height="321" alt="image" src="https://github.com/user-attachments/assets/8b89a135-5d8d-407a-ac2c-361bfcd4fb08" />


## RESULT:
Therefore,the program has been executed successfully.

# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
A Right Pascal Triangle is a pattern of stars (*) in which the number of stars increases in each row until the middle row, then decreases symmetrically, forming a right-aligned triangle on top of an inverted right-aligned triangle.

Write a Java program that:

Prompts the user to enter the number of rows for the upper half of the triangle.

Uses nested loops to first print the increasing part of the triangle, then the decreasing part.

Ensures the stars are aligned properly to form the Right Pascal Triangle shape.

## AIM:
To write a Java program that prints a Right Pascal Triangle pattern using stars (*) by taking the number of rows for the upper half as input from the user, and displaying both the increasing and decreasing parts using nested loops.

## ALGORITHM :
1.Start the program.

2.Import the required package:

3.Import java.util.Scanner to take user input.

4.Declare variables:

5.Create a Scanner object.

6.Declare an integer variable rows to store the number of rows.

7.Input:

Prompt the user to enter the number of rows for the upper half.

8.Read the input value into rows.

9.Print the upper (increasing) part:

10.Use a loop from i = 1 to rows.

11.For each row, use an inner loop from j = 1 to i.

12.Print * in each iteration.

13.Move to the next line after each row.

14.Print the lower (decreasing) part:

15.Use a loop from i = rows - 1 down to 1.

16.For each row, use an inner loop from j = 1 to i.

17.Print * in each iteration.

18.Move to the next line after each row.

19.End the program.





## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: VISMAYA.V
RegisterNumber: 212224060310 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
public class Main
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        int rows=sc.nextInt();
        for(int i=1;i<=rows;i++)
        {
            for(int j=1;j<=i;j++)
            {
                System.out.printf("*");
            }
            System.out.println();
        }
        for(int i=rows-1;i>=1;i--)
        {
            for(int j=1;j<=i;j++)
            {
                System.out.printf("*");
            }
            System.out.println();
        }
    }
}
```
## OUTPUT:

<img width="1276" height="783" alt="image" src="https://github.com/user-attachments/assets/fa3d928e-d110-445f-8e42-77e6d6a1ba01" />



## RESULT:
Therefore the program has been executed successfully.

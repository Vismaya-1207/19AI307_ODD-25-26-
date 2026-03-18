# Ex.No:2(B) METHODS

## QUESTION:

Write a method int cube(int x) that calls a method int square(int x) internally to calculate the cube as x * square(x).
## AIM:
To write a Java program that defines a method square(int x) and uses it inside another method cube(int x) to calculate the cube of a number.
## ALGORITHM :
1.Start the program.

2.Import java.util.Scanner.

3.Define a method square(int n) that returns n * n.

4.Define a method cube(int n) that:
  Calls the method square(n).
  Returns n * square(n).

5.In the main method, create a Scanner object to take input.

6.Read an integer value n from the user.

7.Call the method cube(n) and store the result in a variable res.

8.Print the result res.

9.Stop the program.




## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by:VISMAYA.V 
RegisterNumber:212224060310  
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
public class Main
{
    static int square(int n)
    {
        return n*n;
    }
    static int cube(int n)
    {
        return n*square(n);
    }
    
    public static void main(String[]args)
    {
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        int res=cube(n);
        System.out.printf("%d",res);
    }
}
```
## OUTPUT:
<img width="1236" height="278" alt="image" src="https://github.com/user-attachments/assets/95ea824a-bc51-4c09-b48d-33f53f7ace54" />



## RESULT:
Therefore,the program was executed successfully.

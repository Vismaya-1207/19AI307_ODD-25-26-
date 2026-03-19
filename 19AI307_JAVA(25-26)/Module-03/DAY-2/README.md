# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program to create a class MaxFinder with three overloaded max() methods:

max(int a, int b) – returns the maximum of two integers.

max(double a, double b) – returns the maximum of two double values.

max(int a, int b, int c) – returns the maximum of three integers.

In the main() method, demonstrate the use of each overloaded method with various inputs.

## AIM:
To write a Java program using method overloading to find the maximum of two integers, two double values, and three integers.

## ALGORITHM :
1.Start the program.

2.Create a class MaxFinder with three overloaded max() methods.

3.Define methods to find maximum of:

two integers

two double values

three integers

4.In main(), read input values from the user.

5.Create an object of MaxFinder.

6.Call each max() method with appropriate inputs.

7.Display the results.

8.Stop the program.




## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by:VISMAYA.V 
RegisterNumber: 212224060310 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
class MaxFinder
{
    int max(int a,int b)
    {
        return (Math.max(a,b));
    }
    double max(double a ,double b)
    {
        return (Math.max(a,b));
    }
    int max(int a,int b,int c)
    {
        return Math.max(Math.max(a,b),c);
    }
}
public class Main
{
    public static void main(String[]args)
    {
        Scanner sc=new Scanner(System.in);
        int a=sc.nextInt();
        int b=sc.nextInt();
        double c=sc.nextDouble();
        double d=sc.nextDouble();
        int e=sc.nextInt();
        int f=sc.nextInt();
        int g=sc.nextInt();
        MaxFinder ob=new MaxFinder();
         System.out.printf("Max(%d, %d): %d\n",a,b,ob.max(a,b));
         System.out.printf("Max(%.1f, %.1f): %.1f\n",c,d,ob.max(c,d));
         System.out.printf("Max(%d, %d, %d): %d\n",e,f,g,ob.max(e,f,g));
    }
}

```

## OUTPUT:
<img width="1292" height="483" alt="image" src="https://github.com/user-attachments/assets/bfb87fe8-7f59-44fd-9034-71d2a1f221fd" />



## RESULT:
Therefore,the program was executed successfully.

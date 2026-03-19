# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to check if a number is an Armstrong number using Math.pow() and the Integer wrapper class. Take input from the user.

## AIM:
To write a Java program to check whether a given number is an Armstrong number using Math.pow() and the Integer wrapper class.

## ALGORITHM :
1.Start the program.

2.Read an integer from the user.

3.Convert the number to a string using Integer.toString() to find the number of digits.

4.Store the original number in a variable.

5.Initialize sum = 0.

6.Extract each digit of the number using a loop:

7.Find digit using num % 10.

8.Add Math.pow(digit, number of digits) to sum.

9.Remove last digit using num / 10.

10.Compare sum with the original number.

11.If equal, print "Armstrong number".

12.Else, print "Not an Armstrong number".

13.Stop the program.





## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by:VISMAYA.V 
RegisterNumber:212224060310  
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
public class Main
{
    public static void main(String[]args)
    {
        Scanner sc=new Scanner(System.in);
        int num=sc.nextInt();
        String str=Integer.toString(num);
        int digits=str.length();
        int temp=num;
        int sum=0;
        while(num>0)
        {
            int digit=num%10;
            sum+=Math.pow(digit,digits);
            num/=10;
        }
        if(temp==sum)
        {
            System.out.printf("%d is an Armstrong number.",temp);
        }
        else
        {
            System.out.printf("%d is not an Armstrong number.",temp);
        }
    }
}
```


## OUTPUT:
<img width="1218" height="382" alt="image" src="https://github.com/user-attachments/assets/ff80c8e9-f86d-4961-8fa5-aaaa4669b27f" />



## RESULT:
Therefore,the program was executed successfully.

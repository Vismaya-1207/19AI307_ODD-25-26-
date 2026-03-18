# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java program to print all elements in an array that are greater than a given value

## AIM:
To write a Java program that reads elements into an array and prints all elements that are greater than a given value.

## ALGORITHM :
1.Start the program.

2.Import java.util.Scanner.

3.Create a Scanner object to take input.

4.Read an integer n (size of the array).

5.Declare an integer array arr of size n.

6.Use a loop from i = 0 to n - 1 to input array elements:
 Read each element and store it in arr[i].

7.Read the value val to compare.

8.Initialize a boolean variable flag as false.

9.Use a loop from i = 0 to n - 1:
  If arr[i] > val, then:
    a. Print arr[i].
    b. Set flag = true.

10.After the loop, check if flag == false:
11. If true, print "No elements greater than val".

12.Stop the program.





## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: VISMAYA.V
RegisterNumber:212224060310  
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
        int n=sc.nextInt();
        int[]arr=new int[n];
        for(int i=0;i<n;i++)
        {
            arr[i]=sc.nextInt();
        }
        int val=sc.nextInt();
        boolean flag=false;
        for(int i=0;i<n;i++)
        {
            if(arr[i]>val)
            {
                System.out.printf("%d\n",arr[i]);
                flag=true;
            }
        }
        if(flag==false)
        {
            System.out.printf("No elements greater than %d",val);
        }
    }
}



```
## OUTPUT:
<img width="1213" height="714" alt="image" src="https://github.com/user-attachments/assets/985731c5-f432-4602-9e5b-96e88fd6e3b6" />



## RESULT:
Therefore, the program was executed successfully.

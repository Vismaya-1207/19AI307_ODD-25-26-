# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
You wrote a program that stores some input strings into a String array and prints each string in uppercase.
However, you're getting a NullPointerException.
What should you check in your array before calling .toUpperCase() on a element?

## AIM:
To write a Java program that checks for null values in a string array before converting each string to uppercase, to avoid NullPointerException.

## ALGORITHM :
1.Start the program.

2.Read input strings using BufferedReader.

3.For each input string:

4.Check if the string is null.

5.If it is null, print "Null element".

6.Else, convert the string to uppercase using .toUpperCase() and print it.

7.Repeat until no more input is given.

8.Stop the program.





## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by:VISMAYA.V 
RegisterNumber:212224060310  
*/
```

## SOURCE CODE:
```
import java.io.BufferedReader;
import java.io.InputStreamReader;
public class UppercaseArray
{
    public static void main(String[]args) throws Exception
    {
        BufferedReader br=new BufferedReader(new InputStreamReader(System.in));
        String input;
        while((input=br.readLine())!=null)
        {
            if(input.equals("null"))
            {
                System.out.println("Null element");
            }
            else
            {
                System.out.println(input.toUpperCase());
            }
        }
    }
}

```


## OUTPUT:
<img width="1282" height="375" alt="image" src="https://github.com/user-attachments/assets/90b80297-cfc9-428f-a377-a328f828ba89" />


## RESULT:
Therefore,the program was executed successfully.

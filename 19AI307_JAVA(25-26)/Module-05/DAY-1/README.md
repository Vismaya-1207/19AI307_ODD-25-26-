# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a program to demonstrate chaining of streams (BufferedReader on top of InputStreamReader on top of System.in)

## AIM:
To demonstrate the chaining of input streams using BufferedReader, InputStreamReader, and System.in for efficient keyboard input in Java.

## ALGORITHM :
1.Start the program.

2.Create an InputStreamReader object to convert byte input (System.in) into character stream.

3.Wrap the InputStreamReader with a BufferedReader for efficient reading.

4.Prompt the user to enter a string.

5.Read the input using BufferedReader.readLine().

6.Display the entered input.

7.End the program.



## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: VISMAYA V
RegisterNumber: 212224060310 
*/
```

## SOURCE CODE:
```
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

public class ChainingStreamsExample {
    public static void main(String[] args) {
        // Chaining: System.in -> InputStreamReader -> BufferedReader
        //Write your code here
        BufferedReader br=new BufferedReader(new InputStreamReader(System.in));
        try
        {
            String name=br.readLine();
            int age=Integer.parseInt(br.readLine());
            System.out.println("--- User Details ---");
            System.out.println("Name: "+name);
            System.out.println("Age: "+age);
        }
        catch(Exception e)
        {
            System.out.println(" ");
        }


    }
}


```
## OUTPUT:
<img width="1290" height="575" alt="image" src="https://github.com/user-attachments/assets/548fd65c-2b83-44cc-a00a-5a797683b767" />



## RESULT:
Therefore,the program was executed successfully.

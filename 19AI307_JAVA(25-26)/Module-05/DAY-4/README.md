# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a Java program to implement a extending thread class

## AIM:
To create and run a thread in Java by extending the Thread class.

## ALGORITHM :

1.Start the program.

2.Create a class that extends the Thread class.

3.Override the run() method with the task to be executed.

4.In the main method, create an object of the thread class.

5.Call the start() method to begin execution.

6.Display the output from the thread.

7.End the program.



## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: VISMAYA V
RegisterNumber: 212224060310 
*/
```

## SOURCE CODE:
```
import java.util.*;
class MyThread extends Thread
{
    public void run()
    {
        for(int i=1;i<=5;i++)
        {
            System.out.println("Thread: "+i);
        }
    }
}
public class Main
{
    public static void main(String[]args)
    {
        MyThread t=new MyThread();
        t.start();
        System.out.println("Main thread finished");
    }
}




```
## OUTPUT:
<img width="1289" height="381" alt="image" src="https://github.com/user-attachments/assets/978e59fb-cf03-4062-a6aa-f6b018ffd6db" />



## RESULT:
Therefore,the program was executed successfully.

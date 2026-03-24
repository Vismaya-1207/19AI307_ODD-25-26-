# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:

Write a Java program to create a new file named example.txt.
## AIM:
To create a new file named example.txt using Java file handling.

## ALGORITHM :
1.Start the program.

2.Import required I/O package.

3.Create a File object with the name example.txt.

4.Use createNewFile() method to create the file.

5.Check if the file is created successfully.

6.Display appropriate message.

7.End the program.





## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: VISMAYA V
RegisterNumber:212224060310  
*/
```

## SOURCE CODE:
```
import java.io.FileWriter;
import java.util.*;
public class MAin
{
    public static void main(String[]args)
    {
        String filename="example.txt";
        try
        {
            FileWriter f=new FileWriter(filename);
            f.close();
            System.out.println("File created: "+filename);
        }
        catch(Exception e)
        {
            System.out.println(" ");
        }
    }
}




```
## OUTPUT:
<img width="1290" height="260" alt="image" src="https://github.com/user-attachments/assets/a732d698-19e9-4c91-ad15-07be5fffd218" />



## RESULT:
Therefore,the program was executed successfully.

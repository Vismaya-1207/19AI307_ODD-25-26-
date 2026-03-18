# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a java program to find the longest word in a sentence.

## AIM:
To write a Java program that reads a sentence and finds the longest word present in it.

## ALGORITHM :
1.Start the program.

2.Import java.util.Scanner.

3.Create a Scanner object to take input.

4.Read a sentence from the user using nextLine().

5.Split the sentence into words using split(" ") and store them in an array.

6.Initialize a variable longest with the first word.

7.Traverse through each word in the array.

8.For each word, compare its length with the length of longest.

9.If the current word is longer, update longest.

10.After completing the loop, print the longest word.

11.Stop the program.




## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
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
        String sentence=sc.nextLine();
        String[] words=sentence.split(" ");
        String longest=words[0];
        for(String word:words)
        {
            if(word.length()>longest.length())
            {
                longest=word;
            }
        }
        System.out.printf("The longest word is: %s",longest);
    }
}


```
## OUTPUT:
<img width="1203" height="336" alt="image" src="https://github.com/user-attachments/assets/58af920b-9b8e-4f35-87e2-35ed56d889af" />



## RESULT:
Therefore,the program was executed successfully.

# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program to create an enum Season with values WINTER, SPRING, SUMMER, and FALL. Use a switch statement to display a custom message based on the current season.

# AIM:
To create a Java program using an enum named Season and display a custom message for each season using a switch statement.


## ALGORITHM :
1.Start the program.

2.Define an enum called Season with values: WINTER, SPRING, SUMMER, FALL.

3.Create the main class and method.

4.Take user input for the season.

5.Convert the input to uppercase.

6.Convert the input string into an enum value using Season.valueOf().

7.Use a switch statement to check the season.

8.Display the corresponding message for each case.

9.End the program.




## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by:VISMAYA.V 
RegisterNumber:212224060310  
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
enum Season
{
    WINTER,SPRING,SUMMER,FALL;
}
public class Main
{
    public static void main(String[]args)
    {
        Scanner sc=new Scanner(System.in);
        String input=sc.nextLine().toUpperCase();
        Season season=Season.valueOf(input);
        switch(season)
        {
            case WINTER:
                System.out.print("It's cold outside. Stay warm!");
                break;
            case SPRING:
                System.out.print("Flowers are blooming. Enjoy the fresh air!");
                break;
                case SUMMER:
                System.out.print("It's sunny and hot. Time for the beach!");
                break;
                case FALL:
                System.out.print("Leaves are falling. Autumn is beautiful!");
                break;
        }
    }
}



```

## OUTPUT:

<img width="1292" height="358" alt="image" src="https://github.com/user-attachments/assets/4778dc75-54fe-4706-8f05-e434398aa844" />



## RESULT:
Therefore,the program was executed successfully.

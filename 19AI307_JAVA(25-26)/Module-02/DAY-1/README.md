# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class Vehicle with attributes as number, type and owner.

## AIM:
To create a Java class Vehicle with attributes number, type, and owner, and to read and display details of two vehicle objects.

## ALGORITHM :
1.Start the program.

2.Import java.util.Scanner.

3.Define a class Vehicle with the following attributes:
 String number
 String type
 String owner

4.In the main method, create a Scanner object to take input.

5.Create the first object v1 of class Vehicle.

6.Read values for number, type, and owner and assign them to v1.

7.Create the second object v2 of class Vehicle.

8.Read values for number, type, and owner and assign them to v2.

9.Display the details of v1 (number, type, owner).

10.Display the details of v2 (number, type, owner).

11.Stop the program.




## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: VISMAYA.V
RegisterNumber: 212224060310
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
class Vehicle
{
    String number;
    String type;
    String owner;
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Vehicle v1 = new Vehicle();
        v1.number = sc.next();
        v1.type = sc.next();
        v1.owner = sc.next();

        Vehicle v2 = new Vehicle();
        v2.number = sc.next();
        v2.type = sc.next();
        v2.owner = sc.next();

        System.out.println(v1.number + " | " + v1.type + " | " + v1.owner);
        System.out.println(v2.number + " | " + v2.type + " | " + v2.owner);

        
    }
}


```
## OUTPUT:

<img width="1223" height="352" alt="image" src="https://github.com/user-attachments/assets/41223601-f0f2-419c-9080-14b17183d807" />


## RESULT:
Therefore,the program was executed successfully.

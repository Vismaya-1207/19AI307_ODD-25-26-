# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called Person with private instance variables name, age. and country. Provide public getter and setter methods to access and modify these variables.

## AIM:
To write a Java program to create a class Person with private variables name, age, and country, and to access and modify them using public getter and setter methods.

## ALGORITHM :
1.Start the program.

2.Import java.util.Scanner.

3.Define a class Person.

4.Declare private instance variables:
 String name
 int age
 String country

5.Define a public method set(String name, int age, String country) to assign values to the variables.

6.Define a public method get() to display the values of name, age, and country.

7.In the main method, create a Scanner object to take input.

8.Create an object p1 of class Person.

9.Read the name, age, and country from the user.

10.Call the set() method to assign values to the object.

11.Call the get() method to display the details.

12.Stop the program.





## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: VISMAYA.V
RegisterNumber:212224060310 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
public class Person
{
    private String name;
    private int age;
    private String country;
    public void set(String name,int age,String country)
    {
        this.name=name;
        this.age=age;
        this.country=country;
    }
    public void get()
    {
        System.out.printf("Person 1\n");
        System.out.printf("Name: %s\n",name);
        System.out.printf("Age: %d\n",age);
        System.out.printf("Country: %s\n",country);
    }
    public static void main(String[]args)
    {
        Scanner sc=new Scanner(System.in);
        Person p1=new Person();
        String name=sc.nextLine();
        int age=sc.nextInt();
        sc.nextLine();
        String country=sc.nextLine();
        p1.set(name,age,country);
        p1.get();
    }
}




```
## OUTPUT:

<img width="1220" height="563" alt="image" src="https://github.com/user-attachments/assets/396c69c2-c83d-43a2-86d6-ee3cec432e84" />


## RESULT:
Therefore,the program was executed successfully.

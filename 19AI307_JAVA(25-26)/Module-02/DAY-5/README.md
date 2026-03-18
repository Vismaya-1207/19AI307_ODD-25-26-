# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Employee with method display(). Inside display(), return the current object using this. Create another method that calls display().printName()

## AIM:
To create an Employee class where the display() method returns the current object using this, and demonstrate calling display().printName() from another method.

## ALGORITHM :
1.Start the program.

2.Import java.util.Scanner.

3.Define a class Employee.

4.Declare a String variable name.

5.Define a method set(String name) to assign the value to the instance variable using this.

6.Define a method display() that returns the current object using this.

7.Define a method print() to display the employee name.

8.In the main method, create a Scanner object to take input.

9.Read a string value (employee name) from the user.

10.Create an object e of class Employee.

11.Call the set() method to assign the name.

12.Call display() method and use method chaining to call print() as e.display().print().

13.Display the employee name.

14.Stop the program.



## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: VISMAYA.V
RegisterNumber: 212224060310 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
public class Employee
{
    String name;
    void set(String name)
    {
        this.name=name;
    }
    Employee display()
    {
        return this;
    }
    void print()
    {
        System.out.printf("Employee Name: %s",this.name);
    }
    public static void main(String[]args)
    {
        Scanner sc=new Scanner(System.in);
        String str=sc.nextLine();
        Employee e=new Employee();
        e.set(str);
        e.display().print();
        
    }
}
```

## OUTPUT:
<img width="1227" height="351" alt="image" src="https://github.com/user-attachments/assets/401d54cf-f1c9-4d48-8bf2-5f65d59599af" />



## RESULT:
Therefore,the program was executed succesfully.

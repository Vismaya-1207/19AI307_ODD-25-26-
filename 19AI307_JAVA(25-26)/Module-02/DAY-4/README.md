# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Implement a class Employee with a parameterized constructor to initialize id, name, and salary.

## AIM:

To write a Java program to create a class Employee with a parameterized constructor to initialize id, name, and salary, and display the employee details.
## ALGORITHM :
1.Start the program.

2.Import java.util.Scanner.

3.Define a class Employee.

4.Declare instance variables:
 int id
String name
double salary

5.Define a parameterized constructor Employee(int id, String name, double salary) to initialize the variables using this keyword.

6.Define a method disp() to display employee details.

7.In the main method, create a Scanner object to take input.

8.Read employee id, name, and salary from the user.

9.Create an object of class Employee by passing the input values to the constructor.

10.Call the disp() method to display the details.

11.Stop the program.





## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: VISMAYA.V
RegisterNumber:  212224060310
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
class Employee
{
    int id;
    String name;
    double salary;
    Employee(int id,String name,double salary)
    {
        this.id=id;
        this.name=name;
        this.salary=salary;
    }
    public void disp()
    {
        System.out.println("Employee Details:");
        System.out.println("Employee ID: "+id);
        System.out.println("Employee Name: "+name);
        System.out.println("Employee Salary: "+salary);
    }
}
public  class Main
{
    public static void main(String[]args)
    {
        Scanner sc=new Scanner(System.in);
        int id=sc.nextInt();
        sc.nextLine();
        String name=sc.nextLine();
        double salary=sc.nextDouble();
        Employee obj=new Employee(id,name,salary);
        obj.disp();
    }
}

```
## OUTPUT:

<img width="1224" height="560" alt="image" src="https://github.com/user-attachments/assets/8f42cd8d-7da2-4d8e-ada7-3cd555183ef8" />



## RESULT:
Therefore,the program was executed successfully.

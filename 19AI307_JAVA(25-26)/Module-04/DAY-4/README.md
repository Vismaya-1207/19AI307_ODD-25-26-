# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
You’re creating a cross-platform UI tool using the Abstract Factory pattern. Implement factories to create Button and Checkbox for "dark" and "light" themes. Let the user choose the theme, then generate UI components and display their types

## AIM:

To implement the Abstract Factory design pattern in Java to create Button and Checkbox UI components for "dark" and "light" themes based on user input.
## ALGORITHM :
1.Start the program.

2.Define interfaces Button and Checkbox with a render() method.

3.Create concrete classes for each theme: DarkButton, LightButton, DarkCheckbox, and LightCheckbox.

4.Define an interface UIFactory with methods createButton() and createCheckbox().

5.Implement DarkThemeFactory and LightThemeFactory to create respective UI components.

6.In the main method, take user input for the theme.

7.Convert the input to lowercase.

8.Use an if-else statement to select the appropriate factory (DarkThemeFactory or LightThemeFactory).

9.Use the factory to create a Button and a Checkbox.

10.Call the render() method to display their types.

11.If the input is invalid, display an error message.

12.End the program.





## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by:VISMAYA.V
RegisterNumber:212224060310  
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

interface Button { void render(); }
interface Checkbox { void render(); }
class DarkButton implements Button
{
    public void render()
    {
        System.out.println("Dark Button created");
    }
}
class LightButton implements Button
{
    public void render()
    {
        System.out.println("Light Button created");
    }
}
class DarkCheckbox implements Checkbox
{
    public void render()
    {
        System.out.println("Dark Checkbox created");
    }
}
class LightCheckbox implements Checkbox
{
    public void render()
    {
        System.out.println("Light Checkbox created");
    }
}
interface UIFactory
{
    Button createButton();
    Checkbox createCheckbox();
}
class DarkThemeFactory implements UIFactory
{
    public Button createButton()
    {
        return new DarkButton();
    }
    public Checkbox createCheckbox()
    {
        return new DarkCheckbox();
    }
}
class LightThemeFactory implements UIFactory
{
    public Button createButton()
    {
        return new LightButton();
    }
    public Checkbox createCheckbox()
    {
        return new LightCheckbox();
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String theme = scanner.nextLine().toLowerCase();
        UIFactory factory;
        if (theme.equals("dark")) factory = new DarkThemeFactory();
        else if (theme.equals("light")) factory = new LightThemeFactory();
        else {
            System.out.println("Invalid theme");
            return;
        }
        factory.createButton().render();
        factory.createCheckbox().render();
    }
}





```
## OUTPUT:


<img width="1280" height="416" alt="image" src="https://github.com/user-attachments/assets/21d2eea6-0573-4ebc-8cbf-ca0c649929e9" />


## RESULT:
Therefore,the program was executed successfully.

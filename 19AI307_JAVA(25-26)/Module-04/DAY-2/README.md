# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
At an international airport, only one Radar Control Tower exists. This tower is responsible for handling all flight communications regardless of how many flights are coming in. Each incoming flight must contact this tower to register its approach.

To ensure safety and consistency, all flights must communicate with the same instance of the tower. If multiple towers are created, it may lead to inconsistent instructions — a huge risk in aviation.

Your task is to simulate this system using the Singleton pattern.

## AIM:
To implement the Singleton design pattern in Java to ensure only one instance of a Radar Control Tower handles all flight registrations.

## ALGORITHM :
1.Start the program.

2.Create a class RadarControlTower.

3.Declare a static instance of the class.

4.Make the constructor private to restrict object creation.

5.Create a static method getInstance():

If instance is null, create a new object.

6.Return the same instance every time.

7.Create a method registerFlight() to count and return total flights.

8.In main(), read number of flights.

9.For each flight:

Get the single instance using getInstance().

Register the flight and display total count.

10.Stop the program.





## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: VISMAYA.V
RegisterNumber: 212224060310 
*/
```

## SOURCE CODE:
```
import java.util.*;

class RadarControlTower 
{
    private static RadarControlTower instance;
    static int flightCount=0;
    private RadarControlTower()
    {
        
    }
    public static RadarControlTower getInstance()
    {
      if(instance==null)
      {
          instance=new RadarControlTower();
      }
      return instance;
    }
    public int registerFlight(String flight)
    {
        flightCount++;
        return flightCount;
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine();  // consume newline

        for (int i = 0; i < n; i++) {
            String flight = sc.nextLine();
            RadarControlTower tower = RadarControlTower.getInstance();
            int total = tower.registerFlight(flight);
            System.out.println(flight + " registered with Radar Control Tower. Total Flights: " + total);
        }
    }
}

```

## OUTPUT:
<img width="1218" height="380" alt="image" src="https://github.com/user-attachments/assets/ffce620c-27a9-4d64-a051-121182b20622" />



## RESULT:
Therefore,the program was executed successfully.

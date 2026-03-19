# Ex.No:3(C) ABSTRACTION

## QUESTION:
Description:
Create abstract class GameScore with method finalScore().
Subclasses:

ArcadeGame: score = baseScore + (level × 100)

PuzzleGame: score = (attempts ≤ 3) ? 1000 - (attempts × 100) : 500

## AIM:
To create an abstract class and use inheritance to calculate the final score for different types of games.

## ALGORITHM :
1.Start the program.

2.Create an abstract class Game with abstract method finalScore().

3.Create subclass Arcade:

Take base and level as input.

Calculate score = base + (level × 100).

4.Create subclass Puzzle:

5.Take attempts as input.

If attempts ≤ 3, score = 1000 − (attempts × 100), else score = 500.

6.In main(), read game type.

If type = 1, create Arcade object and display score.

If type = 2, create Puzzle object and display score.

7.Stop the program.





## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by:VISMAYA.V 
RegisterNumber:212224060310 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
abstract class Game
{
    abstract int finalScore();
}
class Arcade extends Game
{
    int base;
    int level;
    Arcade(int base,int level)
    {
        this.base=base;
        this.level=level;
    }
    int finalScore()
    {
        return base+(level*100);
    }
}
class Puzzle extends Game
{
    int att;
    Puzzle(int att)
    {
        this.att=att;
    }
    int finalScore()
    {
        return (att<=3)?1000-(att*100):500;
    }
}
public class Main
{
    public static void main(String[]args)
    {
        Scanner sc=new Scanner(System.in);
        int type=sc.nextInt();
        if(type==1)
        {
            int base=sc.nextInt();
            int level=sc.nextInt();
            Arcade a=new Arcade(base,level);
            System.out.println(a.finalScore());
        }
        else if(type==2)
        {
            int att=sc.nextInt();
            Puzzle p=new Puzzle(att);
            System.out.println(p.finalScore());
        }
    }
}
```

## OUTPUT:
<img width="1239" height="338" alt="image" src="https://github.com/user-attachments/assets/10d852be-a8e2-4de2-b62e-65b0c80b683d" />



## RESULT:
Therefore,the program was executed successfully.

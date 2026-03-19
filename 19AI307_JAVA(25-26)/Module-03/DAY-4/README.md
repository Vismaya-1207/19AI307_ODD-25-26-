# Ex.No:3(D)    INTERFACE 

## QUESTION:
You're building the equalizer system for a music app like BeatBoxx. The equalizer has 3 basic sound modes:

BassBoost
VocalBoost
Balanced
Each mode behaves differently and alters the sound experience. The app uses a SoundMode interface that each mode implements.

## AIM:
To create a Java program using an interface to implement different sound modes (Bass, Vocal, Balanced) and apply the selected mode.

## ALGORITHM :
1.Start the program.

2.Create an interface Sound with method apply().

3.Create classes Bass, Vocal, and Balanced that implement Sound.

4.Define the apply() method in each class with appropriate output.

5.In main(), read the sound mode from the user.

6.Use switch to select the mode:

If "bass", create Bass object.

If "vocal", create Vocal object.

If "balanced", create Balanced object.

7.If input is invalid, display error message.

8.Call apply() method for the selected mode.

9.Stop the program.





## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: 
RegisterNumber:  
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
interface Sound
{
    void apply();
}
class Bass implements Sound
{
    public void apply()
    {
        System.out.println("Bass Boost applied. Feel the beat drop!");
    }
}
class Vocal implements Sound
{
    public void apply()
    {
        System.out.println("Vocal Boost enabled. Enjoy crystal-clear lyrics!");
    }
}
class Balanced implements Sound
{
    public void apply()
    {
        System.out.println("Balanced mode set. A perfect blend of bass and vocals.");
    }
}
public class Main
{
    public static void main(String[]args)
    {
        Scanner sc=new Scanner(System.in);
        String mode=sc.nextLine().toLowerCase();
        Sound s;
        switch(mode)
        {
            case "bass":
                s=new Bass();
                break;
                case "vocal":
                    s=new Vocal();
                    break;
                    case "balanced":
                        s=new Balanced();
                        break;
                        default:
                            System.out.println("Invalid mode selected.");
                            return;
        }
        s.apply();
        
    }
}
```


## OUTPUT:
<img width="1233" height="393" alt="image" src="https://github.com/user-attachments/assets/ecb753c9-7dbe-497e-a317-9580b689a3d6" />



## RESULT:
Therfore,the program was executed successfully.

# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Synchronize deposit method in a BankAccount class, simulate deposits from multiple threads.

## AIM:
To demonstrate synchronization by implementing a thread-safe deposit method in a BankAccount class and simulating deposits from multiple threads.

## ALGORITHM :
1.Start the program.

2.Create a BankAccount class with a balance variable.

3.Define a synchronized deposit() method to update the balance safely.

4.Create a thread class that performs deposit operations.

5.In the main method, create a shared BankAccount object.

6.Create multiple thread objects and pass the same account reference.

7.Start all threads.

8.Wait for threads to finish (optional using join()).

9.Display the final balance.

10.End the program.	





## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: VISMAYA V
RegisterNumber:  212224060310
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class BankAccount {
    int balance = 0;

    synchronized void deposit(int amount) {
        balance = balance + amount;
    }
}

class MyThread extends Thread {
    BankAccount acc;
    int amt;

    MyThread(BankAccount acc, int amt) {
        this.acc = acc;
        this.amt = amt;
    }

    public void run() {
        acc.deposit(amt);
    }
}

public class Main {
    public static void main(String[] args) throws Exception {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        BankAccount acc = new BankAccount();

        MyThread[] t = new MyThread[n];

        for (int i = 0; i < n; i++) {
            int amount = sc.nextInt();
            t[i] = new MyThread(acc, amount);
            t[i].start();
        }

        for (int i = 0; i < n; i++) {
            t[i].join();
        }

        System.out.println("Final Balance: " + acc.balance);
    }
}




```
## OUTPUT:
<img width="1283" height="559" alt="image" src="https://github.com/user-attachments/assets/99c1117d-38b6-4d85-97b1-551f43e8fc3e" />



## RESULT:
Therefore,the program was executed successfully.

# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Print "Hello" and "World" alternately from two threads using synchronized blocks.


## AIM:
To print "Hello" and "World" alternately using two threads by synchronizing their execution with wait() and notify().


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a SharedPrinter class with a boolean flag to control turns.
4.	In printHello(), print “Hello” only when it's the Hello turn; otherwise call wait().
5.	After printing, switch the turn and call notify().
6.	In printWorld(), do the same but for “World”, waiting when it’s not its turn.
7.	In main(), create two threads calling these methods and start them to print alternately.





## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: Sakthi Priya S
RegisterNumber:  212222040140
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class SharedPrinter {
    private boolean helloTurn = true; 

    public synchronized void printHello(int times) {
        for (int i = 0; i < times; i++) {
            while (!helloTurn) { 
                try {
                    wait();
                } catch (InterruptedException e) {
                    e.printStackTrace();
                }
            }
            System.out.println("Hello");
            helloTurn = false;
            notify(); 
        }
    }

    public synchronized void printWorld(int times) {
        for (int i = 0; i < times; i++) {
            while (helloTurn) { 
                try {
                    wait();
                } catch (InterruptedException e) {
                    e.printStackTrace();
                }
            }
            System.out.println("World");
            helloTurn = true;
            notify(); 
        }
    }
}

public class HelloWorldThreads {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt(); 

        SharedPrinter printer = new SharedPrinter();

        Thread t1 = new Thread(() -> printer.printHello(n));
        Thread t2 = new Thread(() -> printer.printWorld(n));

        t1.start();
        t2.start();

        sc.close();
    }
}
```







## OUTPUT:
<img width="1320" height="769" alt="image" src="https://github.com/user-attachments/assets/c3a24ec2-bc42-4c64-baa7-f97499be4728" />




## RESULT:
Thus,the Program is executed Successfully.


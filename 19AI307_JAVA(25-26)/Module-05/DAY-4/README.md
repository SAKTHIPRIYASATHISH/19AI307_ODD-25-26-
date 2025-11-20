# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for set the priority and name of the current thread.


## AIM:
To set the name and priority of the current thread in Java using Thread.currentThread(), and display the updated thread details.


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the desired thread name from the user.
4.	Get the current thread using Thread.currentThread().
5.	Set the thread’s name with setName().
6.	Set the thread’s priority with setPriority().
7.	Print the thread’s name, priority, and full thread details.





## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: Sakthi Priya S
RegisterNumber: 212222040140 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class SetCurrentThreadExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

       
        String threadName = sc.nextLine();

        
        Thread t = Thread.currentThread();

        
        t.setName(threadName);
        t.setPriority(2);

        
        System.out.println("Priority of Thread: " + t.getPriority());
        System.out.println("Name of Thread: " + t.getName());
        System.out.println(t);

        sc.close();
    }
}
```







## OUTPUT:
<img width="1289" height="345" alt="image" src="https://github.com/user-attachments/assets/a263e1ad-cef1-45f3-8a53-8a82fef009a5" />





## RESULT:
Thus,the Program is executed Successfully.


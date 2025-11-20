# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program where the inner class is declared private and accessed through a method in the outer class. 


## AIM:
To write a Java program where a private inner class is declared inside an outer class and accessed indirectly using a public method of the outer class.


## ALGORITHM :
```
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an outer class.
4.	Declare an inner class inside it as private.
5.	Inside the inner class, define a method
6.	In the outer class, define a public method that:
      ->Creates an object of the private inner class.
  	   ->Calls its method.
7. In the main() method, create an object of the outer class and call the public method to access the inner class.
```





## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: Sakthi Priya S
RegisterNumber: 212222040140 
*/
```

## SOURCE CODE:
```
import java.util.*;

public class Main {
    private class Inner {
        int data;
        Inner(int data) {
            this.data = data;
        }
        void display() {
            System.out.println("Data set inside private inner class: " + data);
        }
    }

    void accessInner(int num) {
        Inner inner = new Inner(num);
        inner.display();
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        Main outer = new Main();
        outer.accessInner(num);
        sc.close();
    }
}
```







## OUTPUT:
<img width="1252" height="395" alt="image" src="https://github.com/user-attachments/assets/584a1470-8c02-437e-81af-d5de7777da38" />




## RESULT:
Thus,the Program is executed Successfully.


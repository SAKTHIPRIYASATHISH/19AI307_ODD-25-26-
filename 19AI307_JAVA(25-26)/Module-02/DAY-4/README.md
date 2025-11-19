# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a program to access a static variable using both class name and object.


## AIM:
To write a Java program that demonstrates how to access a static variable using both the class name and an object of the class.


## ALGORITHM :
```
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class (e.g., Demo) with a static variable such as static int count = 10;.
4.	Inside the main method:
    ->Access the static variable using the class name: Demo.count.
5. Create an object of the class: Demo obj = new Demo();.
6. Access the same static variable using the object: obj.count.
7. Print both values to show that static variables are shared and can be accessed both ways.
8. End the program.
```





## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: Sakthi Priya S
RegisterNumber:  212222040140
*/
```

## SOURCE CODE:
```
import java.util.*;
class Example{
    static int num;
}
public class Main{
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        Example.num=sc.nextInt();
        System.out.println("Accessing using class name: "+Example.num);
        Example obj=new Example();
        System.out.println("Accessing using object: "+obj.num);
        
    }
}
```







## OUTPUT:
<img width="1240" height="422" alt="image" src="https://github.com/user-attachments/assets/cd84d4e1-2306-4011-9809-bbc614b8acc7" />




## RESULT
Thus,the Program is executed Successfully.


# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Write a Java program to calculate the factorial of a number using a for loop. The factorial of n is the product of all positive integers less than or equal to n.


## AIM:
To write a Java program that calculates the factorial of a given number using a for loop, where the factorial of n is the product of all positive integers from 1 to n.


## ALGORITHM :
```
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the input number n.
4.	Initialize a variable fact = 1.
5.	Use a for loop from i = 1 to i <= n:
      ->Multiply fact = fact * i.
6. After the loop ends, fact contains the factorial of n.
7. Display the result.
8. End the Program.
```





## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: Sakthi Priya S
RegisterNumber:  212222040140 
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Main{
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        int fact=1;
        for(int i=1;i<=n;i++){
            fact=fact*i;
        }
        System.out.println("Factorial of "+n+" is: "+fact);
        
    }
}
```







## OUTPUT:
<img width="1295" height="354" alt="image" src="https://github.com/user-attachments/assets/08a62bcf-405c-48c0-b4c0-df7751b8a617" />




## RESULT:
Thus,the program is executed successfully.


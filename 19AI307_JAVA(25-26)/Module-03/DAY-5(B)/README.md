# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Find the largest digit in a number using wrapper class methods.


## AIM:
To write a Java program that finds the largest digit in a given number using Wrapper class methods.


## ALGORITHM :
```
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the input number as a String, then convert it to an Integer using Integer.valueOf().
4.	Store the number in variable n and initialize largest = 0.
5.	Repeat while n > 0:
     ->Extract the last digit using digit = n % 10.
  	  ->If digit > largest, update largest = digit.
  	  ->Remove the last digit using n = n / 10.
6. After the loop ends, print the value of largest as the largest digit.
7. End the program.
```





## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: Sakthi Priya S
RegisterNumber:  212222040140
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class LargestDigitFinder {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Integer num = Integer.valueOf(sc.next());
        int largest = 0;
        int n = num;

        while (n > 0) {
            int digit = n % 10;
            if (digit > largest) largest = digit;
            n /= 10;
        }
        System.out.println("The largest digit is: " + largest);
    }
}
```







## OUTPUT:
<img width="1249" height="393" alt="image" src="https://github.com/user-attachments/assets/d1cde23e-7b0a-41e5-98e3-47a3134ec4c0" />




## RESULT:
Thus,the Program is executed Successfully.


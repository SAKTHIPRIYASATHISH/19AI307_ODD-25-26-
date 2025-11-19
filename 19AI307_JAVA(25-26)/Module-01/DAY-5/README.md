# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a Java program to reverse a given string.


## AIM:
To write a Java program that reverses a given string by reading it from the user and displaying its reversed form.


## ALGORITHM :
```
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the input string str.
4.	Create an empty string rev = "".
5.	Loop from the last character of str to the first:
       ->Append each character to rev.
6. After the loop ends, rev contains the reversed string.
7. Display the reversed string.
8. End the Program.
```
 
   





## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by: Sakthi Priya S
RegisterNumber:  212222040140
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class ReverseString {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String str = sc.nextLine();

        String reversed = "";
        for (int i = str.length() - 1; i >= 0; i--) {
            reversed += str.charAt(i);
        }

        System.out.println("Reversed string: " + reversed);

    }
}
```







## OUTPUT:
<img width="1299" height="358" alt="image" src="https://github.com/user-attachments/assets/521fd06a-5282-450c-bf93-2e40e2f54a1e" />





## RESULT:
Thus,the Program is executed successfully.


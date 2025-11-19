# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Write a method that accepts a string and returns whether it contains only lowercase letters or not.


## AIM:
To write a method in Java that accepts a string and checks whether it contains only lowercase letters, returning true if all characters are lowercase and false otherwise.


## ALGORITHM :
```
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Accept the input string str.
4.	Loop through each character of the string.
5.	For each character:
   ->Check if it lies between 'a' and 'z'.
  	->If any character is not lowercase, return false.
6. If the loop completes and all characters are lowercase, return true.
7. End the method.
```





## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: Sakthi Priya S
RegisterNumber:  212222040140
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class Main {
    public static boolean isLowercase(String str) {
       
        for (int i = 0; i < str.length(); i++) {
            if (!Character.isLowerCase(str.charAt(i))) {
                return false;
            }
        }
        return true;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String input = sc.nextLine();

        System.out.println(isLowercase(input));
    }
}

```







## OUTPUT:
<img width="1242" height="361" alt="image" src="https://github.com/user-attachments/assets/ca1d04aa-82de-47ba-9b43-f1eba5141b96" />




## RESULT:
Thus,the Program is executed successfully.


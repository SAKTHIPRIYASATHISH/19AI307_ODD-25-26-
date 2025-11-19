# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
```
Aliens scan DNA numbers:
 ->If the DNA number is divisible by 2 and ends in 4, they accept it.
 ->If the DNA number is divisible by 2 but ends in anything else, it’s a suspect.
 ->If the DNA is odd, they reject it.
The program will print one of the following statements based on the input:
   ->Accepted
   ->Suspect
   ->Rejected
```


## AIM:
To write a program that checks a given DNA number and determines whether it is Accepted, Suspect, or Rejected based on specific conditions using divisibility and last-digit checks.


## ALGORITHM :
```
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the input DNA number n.
4.	Check if n is odd (n % 2 != 0):
      ->If yes → Print "Rejected".
5.If n is even, check the last digit (n % 10):
   ->If last digit is 4 → Print "Accepted".
  	->Else → Print "Suspect".
6.End the program.
```





## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by:  Sakthi Priya S
RegisterNumber:  212222040140
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Main{
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        int a=sc.nextInt();
        if(a%2==0){
            if(a%10==4){
                System.out.println("Accepted");
            }
            else{
                System.out.println("Suspect");
            }
        }
        else{
            System.out.println("Rejected");
        }
    }
}
```







## OUTPUT:
<img width="1238" height="352" alt="image" src="https://github.com/user-attachments/assets/1bad506b-b5ac-469b-85aa-fcb0718adb25" />






## RESULT:
Thus,the program is executed successfully.


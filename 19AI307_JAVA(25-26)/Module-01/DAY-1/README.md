# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
Lovely found a magic number in her notebook and decided to try some spells using the mysterious ++ symbol. But something strange happened — depending on where she placed the ++, the results were different!

She wants to understand:

Post-increment (a++) → value is used first, then incremented

Pre-increment (++a) → value is incremented first, then used

Help Lovely write a program that:

Accepts one integer number.

Applies both post-increment and pre-increment.

Shows the difference in output when using a++ and ++a.

Input Format
One integer (the magic number)

Output Format
Print the results in this format:

Original number = <value>
After post-increment (a++) = <value used>, Now a = <current value>
After pre-increment (++a) = <value used>, Now a = <current value>


## AIM:
To write a Java program that demonstrates the difference between post-increment (a++) and pre-increment (++a) by accepting a number, applying both operations, and displaying the results.


## ALGORITHM :
```
1.	Start the program.
2. Read an integer input a.
3. Display the original value of a.   
4. Apply post-increment:
      ->Store a++ in a variable (value used before increment).
      ->Print the used value and the new value of a.
5.Apply pre-increment:
       ->Store ++a in another variable (increment happens first).
       ->Print the used value and the new value of a.
6.End the program.
```



## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: Sakthi Priya S
RegisterNumber: 212222040140 
*/
```

## Sourcecode.java:
```
import java.util.*;
public class java
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner (System.in);
        int l = sc.nextInt();
       
       
        System.out.println("Original number = "+l);
        int post = l++;
        System.out.println("After post-increment (a++) = "+post+", Now a = "+l);
        int pre = ++l;
        
        System.out.println("After pre-increment (++a) = "+pre+", Now a = "+l);   
    }
    
}
```







## OUTPUT:
<img width="1237" height="395" alt="image" src="https://github.com/user-attachments/assets/ecc56948-3f37-4807-b6dd-c92398d3c17e" />




## RESULT:
Thus,the program is executed successfully.


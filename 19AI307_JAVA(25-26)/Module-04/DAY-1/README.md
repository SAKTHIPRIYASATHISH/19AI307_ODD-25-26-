# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
If an Integer object is set to null, and you attempt to call .toString() on it, what happens? How can you prevent your code from throwing an exception in such cases?



## AIM:
To demonstrate what happens when calling .toString() on a null Integer object and how to prevent a NullPointerException by performing a null check before using the object.


## ALGORITHM :
```
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Scanner object to read user input.
4.	Read an integer using sc.nextInt() and store it in an Integer object s.
5.	Use a try block to handle possible exceptions.
6.	Check:
     ->If s == null or s == 0, explicitly throw a NullPointerException.
  	  ->Else, call s.toString() and print the value.
7. In the catch block, display "Null Integer" if an exception occurs.
8. End the program.
```





## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: Sakthi Priya S
RegisterNumber:  212222040140
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Main
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        
        try
        {
            Integer s=sc.nextInt();
            if(s==null || s==0){
                throw new NullPointerException();
            }
            else{
                System.out.println(s.toString());
            }
        }
        catch(Exception e)
        {
            System.out.println("Null Integer");
        }
    }
}
```







## OUTPUT:
<img width="1318" height="434" alt="image" src="https://github.com/user-attachments/assets/8b95ba31-4a13-4277-84b4-c687d32e6119" />




## RESULT:
Thus,the Program is executed Successfully.


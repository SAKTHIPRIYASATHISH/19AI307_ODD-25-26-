# Ex.No:2(B) METHODS

## QUESTION:
Write a Java program with instance method calculateSum() that sums elements of an integer array. Class name is ArrayOps. Return type is int.


## AIM:
To write a Java program with a class ArrayOps containing an instance method calculateSum() that returns the sum of all elements in an integer array.


## ALGORITHM :
```
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class ArrayOps with an instance method calculateSum(int arr[]).
4.	Inside the method, initialize sum = 0.
5.	Traverse the array using a loop:
    ->Add each element to sum.
6. Return the final sum.
7. In the main method, create an object of ArrayOps.
8. Call calculateSum() with an integer array and print the result.
9. End the Program.
```





## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: Sakthi Priya S
RegisterNumber: 212222040140 
*/
```

## SOURCE CODE:
```
import java.util.*;
public class ArrayOps {

    public static int calculateSum(int [] arr) {
       
        int sum=0;
        for(int i=0;i<arr.length;i++)
        {
            sum+=arr[i];
        }
        return sum;
    }

    public static void main(String[] args) {
       
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        int arr[]=new int[n];
        for(int i=0;i<n;i++)
        {
            arr[i]=sc.nextInt();
        }
        int result=calculateSum(arr);
        System.out.println(result);
    }
}
```







## OUTPUT:
<img width="1296" height="279" alt="image" src="https://github.com/user-attachments/assets/2b69328f-6418-4eb2-9a3b-fc44ea2cbb5c" />





## RESULT:
Thus,the Program is executed Successfully.


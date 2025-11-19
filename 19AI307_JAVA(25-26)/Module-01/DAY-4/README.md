# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java Program to count Even and Odd Numbers in an Array.


## AIM:
To write a Java program that reads an array of numbers and counts how many elements are even and how many are odd.


## ALGORITHM :
```
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the size of the array n.
4.	Declare an array of size n and input all elements.
5.	Initialize two counters: evenCount = 0, oddCount = 0.
6.	Traverse the array using a loop:
     ->If arr[i] % 2 == 0, increment evenCount.
  	  ->Else, increment oddCount.
7. Print the number of even and odd elements.
8. End the Program.
```





## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: Sakthi Priya S
RegisterNumber:  21222040140 
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Main{
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        int[] arr=new int[n];
        int even=0;
        int odd=0;
        for(int i=0;i<n;i++){
            arr[i]=sc.nextInt();
            if(arr[i]%2==0){
                even++;
            }
            else{
                odd++;
            }
            
            
        }
        System.out.println("Number of even elements: " + even);
        System.out.println("Number of odd elements: " + odd);
    }
}
```







## OUTPUT:
<img width="1297" height="681" alt="image" src="https://github.com/user-attachments/assets/6b6fbedc-c2c1-469b-8f01-f83d25470ed5" />




## RESULT:
Thus,the program is executed successfully.


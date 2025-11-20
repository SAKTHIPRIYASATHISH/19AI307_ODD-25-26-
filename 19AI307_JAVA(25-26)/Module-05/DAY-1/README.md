# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a Java program to write text into a file using FileOutputStream. 


## AIM:
To write text data into a file using FileOutputStream in Java by converting a string into bytes and storing it in a specified file.


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Declare the file name and text to be written.
4.	Create a FileOutputStream object for the file.
5.	Convert the text into a byte array using getBytes().
6.	Write the bytes to the file using write().
7.	Close the FileOutputStream.
8.	Print a success message; handle exceptions using try–catch.





## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: Sakthi Priya S
RegisterNumber:  212222040140
*/
```

## SOURCE CODE:
```
import java.io.FileOutputStream;
public class Main{
    public static void main(String[] args){
        try{
            String filename="sample.txt";
            String text="Welcome";
            FileOutputStream fos=new FileOutputStream(filename);
            fos.write(text.getBytes());
            fos.close();
            System.out.println("File written successfully.");
            
        }
        catch(Exception e){
            System.out.println(e);
        }
    }
}
```







## OUTPUT:
<img width="1245" height="459" alt="image" src="https://github.com/user-attachments/assets/1f5d9ae9-400b-4ba7-9678-33d8973aa353" />




## RESULT:
Thus,the PRogram is executed Successfully.


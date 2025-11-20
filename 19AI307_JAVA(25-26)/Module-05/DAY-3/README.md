# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Write a program to count the number of characters in a file.


## AIM:
To write user-entered text into a file and count the total number of characters written using Java file handling.


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read a line of text from the user.
4.	Create a FileWriter to write the text into "data.txt".
5.	Write the text to the file and close the writer.
6.	Count characters using text.length().
7.	Print the character count; handle exceptions if any.





## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: Sakthi Priya S
RegisterNumber:  212222040140
*/
```

## SOURCE CODE:
```
import java.io.*;
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String text = sc.nextLine();

        try {
            FileWriter fw = new FileWriter("data.txt");
            fw.write(text);
            fw.close();

            int count = text.length();
            System.out.println("Number of characters written to the file: " + count);

        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}

```







## OUTPUT:
<img width="1249" height="380" alt="image" src="https://github.com/user-attachments/assets/b9048f6e-9725-4c8b-9aa0-09207884ff11" />





## RESULT:
Thus,the Program is executed Successfully


# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
```
In a large office, multiple departments send print jobs to a shared central printer. To manage load and prevent collision, a Print Spooler Manager handles all job submissions.

The IT team insists that there should be only one spooler manager instance in the entire system. Regardless of how many jobs or departments exist, all jobs must pass through this one manager.

Your task is to simulate a singleton print job queue. Each print job submitted increases the queue count.

Hidden Clue:
Use Singleton to manage shared access.

Count and log each print job submission.

Validate that state is preserved across all accesses.

Input Format:
First line: Integer n – number of print jobs

Next n lines: Each line contains the department name submitting the print job.

Output Format:
For each job, print:


[Department] submitted a print job. Total Jobs in Queue: [count]
```


## AIM:
To simulate a shared print job queue using the Singleton Design Pattern, ensuring that only one PrintSpoolerManager object handles all print job submissions and maintains a common job count across all departments.


## ALGORITHM :
```
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define a PrintSpoolerManager class:
    ->Declare a private static instance of the class.
  	 ->Make the constructor private to prevent external object creation.
  	 ->Provide a getInstance() method that returns the single instance, creating it only once.
  	 ->Maintain a jobCount variable and increment it for every submitted job.
4. In main(), read the number of print jobs n.
5. Loop n times:
    ->Read the department name.
    ->Call PrintSpoolerManager.getInstance() to get the shared singleton object.
    ->Submit the print job using submitJob(dept) which increments the shared jobCount.
    ->Print: [Department] submitted a print job. Total Jobs in Queue: [count]
6. End the program.
```





## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: Sakthi Priya S
RegisterNumber:  212222040140
*/
```

## SOURCE CODE:
```
import java.util.*;

class PrintSpoolerManager {
    private static PrintSpoolerManager instance; 
    private int jobCount; 
    private PrintSpoolerManager() {
        jobCount = 0;
    }
    public static PrintSpoolerManager getInstance() {
        if (instance == null) {
            instance = new PrintSpoolerManager();
        }
        return instance;
    }
    public int submitJob(String department) {
        jobCount++;
        return jobCount;
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String dept = sc.nextLine();
            PrintSpoolerManager spooler = PrintSpoolerManager.getInstance(); 
            int total = spooler.submitJob(dept);
            System.out.println(dept + " submitted a print job. Total Jobs in Queue: " + total);
        }
    }
}
```







## OUTPUT:
<img width="1243" height="582" alt="image" src="https://github.com/user-attachments/assets/f562cff8-956e-496f-afc2-24e6b49d9a4a" />




## RESULT:
Thus,the Program is executed Successfully.


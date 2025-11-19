# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
```
Create a Super class Person with fields name and age. Create a subclass Student that inherits from Person and adds a field marks (integer). Implement a method in Student called calculateGrade() which returns the grade based on the marks:
  -> Marks ≥ 90: Grade A
  ->Marks ≥ 75 and < 90: Grade B
  ->Marks ≥ 50 and < 75: Grade C
  ->Marks < 50: Grade F
```


## AIM:
To create a superclass Person with fields name and age, and a subclass Student that inherits these fields and adds a new field marks. Also, to implement a method calculateGrade() in Student that returns a grade based on the marks.


## ALGORITHM :
```
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a superclass Person with fields name and age.
4.	Create a subclass Student that extends Person and adds an integer field marks.
5.	Inside Student, define a method calculateGrade():
     ->If marks ≥ 90, return "A".
  	  ->Else if marks ≥ 75, return "B".
  	  ->Else if marks ≥ 50, return "C".
  	  ->Else return "F".
6. In the main method:
     ->Create a Student object.
     ->Assign values to name, age, and marks.
     ->Call calculateGrade() and display the grade.
7. End the Program.
```





## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: Sakthi Priya S
RegisterNumber: 212222040140 
*/
```

## SOURCE CODE:
```
import java.util.*;

class Person {
    String name;
    int age;

    Person(String name, int age) {
        this.name = name;
        this.age = age;
    }
}

class Student extends Person {
    int marks;

    Student(String name, int age, int marks) {
        super(name, age);
        this.marks = marks;
    }

    String calculateGrade() {
        if (marks >= 90) return "A";
        else if (marks >= 75) return "B";
        else if (marks >= 50) return "C";
        else return "F";
    }
    void displayStudentDetails() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
        System.out.println("Marks: " + marks);
        System.out.println("Grade: " + calculateGrade());
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

      
        String name = sc.nextLine();
        int age = sc.nextInt();
        int marks = sc.nextInt();

        Student s = new Student(name, age, marks);

        
        s.displayStudentDetails();
        
        sc.close();
    }
}
```







## OUTPUT:
<img width="1295" height="672" alt="image" src="https://github.com/user-attachments/assets/78e9aacc-f0f4-4f07-8d31-1f8b99e42103" />




## RESULT:
Thus,the Program is executed Successfully.


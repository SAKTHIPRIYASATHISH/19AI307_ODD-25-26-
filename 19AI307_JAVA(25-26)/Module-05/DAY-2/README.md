# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a Java program to serialize a collection of objects (like ArrayList<Student>) into a file.


## AIM:
To serialize and deserialize a collection of Student objects using ObjectOutputStream and ObjectInputStream, storing the list in a file and later retrieving it.


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Student class implementing Serializable
4.	Read n students from the user and store them in an ArrayList<Student>.
5.	Use ObjectOutputStream to write the ArrayList to a file (serializeStudents).
6.	Use ObjectInputStream to read the ArrayList back from the file (deserializeStudents).
7.	Display the deserialized student objects.






## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: Sakthi Priya S
RegisterNumber: 212222040140  
*/
```

## SOURCE CODE:
```
import java.io.*;
import java.util.*;


class Student implements Serializable {
    private static final long serialVersionUID = 1L;

    private int id;
    private String name;
    private double marks;

    public Student(int id, String name, double marks) {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }

    @Override
    public String toString() {
        return "Student{id=" + id + ", name='" + name + "', marks=" + marks + "}";
    }
}

public class StudentSerializationUserInput {


    public static void serializeStudents(List<Student> students, String fileName) {
        try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream(fileName))) {
            oos.writeObject(students);
            System.out.println("Students serialized successfully into: " + fileName);
        } catch (IOException e) {
            System.out.println("Error during serialization: " + e.getMessage());
        }
    }

    
    @SuppressWarnings("unchecked")
    public static List<Student> deserializeStudents(String fileName) {
        List<Student> students = null;
        try (ObjectInputStream ois = new ObjectInputStream(new FileInputStream(fileName))) {
            students = (List<Student>) ois.readObject();
            System.out.println("Students deserialized successfully from: " + fileName);
        } catch (IOException | ClassNotFoundException e) {
            System.out.println("Error during deserialization: " + e.getMessage());
        }
        return students;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        List<Student> students = new ArrayList<>();

        int n = scanner.nextInt();
        scanner.nextLine(); 

        for (int i = 0; i < n; i++) {
            int id = scanner.nextInt();
            scanner.nextLine(); 
            String name = scanner.nextLine();
            double marks = scanner.nextDouble();
            scanner.nextLine();
            students.add(new Student(id, name, marks));
        }

        String fileName = "students.dat";
        serializeStudents(students, fileName);

        List<Student> deserializedStudents = deserializeStudents(fileName);
        if (deserializedStudents != null) {
            System.out.println("\nDeserialized Students:");
            for (Student s : deserializedStudents) {
                System.out.println(s);
            }
        }

        scanner.close();
    }
}
```







## OUTPUT:
<img width="1303" height="768" alt="image" src="https://github.com/user-attachments/assets/bc42939c-3d1e-47d5-a1f2-3129e4a1f047" />




## RESULT:
Thus,the Program is executed Successfully.


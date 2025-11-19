# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class Car with attributes brand, model, year. Create 2 objects and print their details.


## AIM:
To create a Java class Car with attributes brand, model, and year, then create two objects of the class and print their details.


## ALGORITHM :
```
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define a class Car with attributes: brand, model, year.
4.	Inside the main method, create two objects of the Car class.
5.	Assign values to the attributes of each object.
6.	Print the details (brand, model, year) of both Car objects.
7.	End the program.
```





## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: Sakthi Priya S
RegisterNumber:  212222040140
*/
```

## SOURCE CODE:
```
class Car
{
    String brand,model;
    int year;
}
public class prog {
    public static void main(String[] args) {
        Car car1 = new Car();
        car1.brand = "Toyota";
        car1.model = "Innova";
        car1.year = 2022;

        Car car2 = new Car();
        car2.brand = "Hyundai";
        car2.model = "i20";
        car2.year = 2021;

        System.out.println("Car 1: " + car1.brand + " " + car1.model + " " + car1.year);
        System.out.println("Car 2: " + car2.brand + " " + car2.model + " " + car2.year);
    }
}
```







## OUTPUT:
<img width="1292" height="286" alt="image" src="https://github.com/user-attachments/assets/0c6684b1-8dc2-4915-8c0d-8a36dba5311a" />




## RESULT:
Thus,the Program is executed successfully.


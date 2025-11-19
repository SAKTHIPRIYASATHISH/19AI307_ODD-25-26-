# Ex.No:3(b) POLYMORPHISM

## QUESTION:
```
Write a Java program that calculates the area of different shapes using method overloading. Create a class AreaCalculator with:
 ->area(int side) for square
 ->area(int length, int breadth) for rectangle
 ->area(double radius) for circle
```


## AIM:
To write a Java program that demonstrates method overloading by calculating the area of different shapes (square, rectangle, and circle) using overloaded area() methods in a class AreaCalculator.


## ALGORITHM :
```
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class AreaCalculator.
4.	Overload the method area() in three forms:
    ->area(int side) → calculate area of a square (side * side).
  	 ->area(int length, int breadth) → calculate area of a rectangle (length * breadth).
  	 ->area(double radius) → calculate area of a circle (3.14 * radius * radius).
5. In the main method:
     ->Create an object of AreaCalculator.
     ->Call each overloaded method with required parameters.
     ->Print the results.
6. End the program.
```





## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: Sakthi Priya S
RegisterNumber:  212222040140
*/
```

## SOURCE CODE:
```
import java.util.*;

class AreaCalculator{
    int side, l, b;
    double r;
    
    AreaCalculator(int side, int l, int b, double r){
        this.side = side;
        this.l = l;
        this.b = b;
        this.r = r;
    }
    
    void area(int side){
        System.out.println("Area of square: " + (side*side));
    }
    void area(int l, int b){
        System.out.println("Area of rectangle: " + (l*b));
    }
    void area(double r){
        System.out.println("Area of circle: " + (Math.PI * r * r));
    }
}
class prog{
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int s = sc.nextInt();
        int l = sc.nextInt();
        int b = sc.nextInt();
        double r = sc.nextDouble();
        
        AreaCalculator a = new AreaCalculator(s,l,b,r);
        a.area(s);
        a.area(l,b);
        a.area(r);
    }
}
```







## OUTPUT:
<img width="1305" height="529" alt="image" src="https://github.com/user-attachments/assets/e1d983b5-d1e8-4991-a545-b5e8db4ef0a7" />




## RESULT:
Thus,the Program is executed Successfully.


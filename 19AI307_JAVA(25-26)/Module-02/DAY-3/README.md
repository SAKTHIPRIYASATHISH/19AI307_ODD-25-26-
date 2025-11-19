# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called “Book” with private instance variables title, author, and price. Provide public getter and setter methods to access and modify these variables. Add a method called applyDiscount() that takes a percentage as a parameter and reduces the price by that percentage.


## AIM:
To write a Java program that defines a class Book with private instance variables title, author, and price, and provides public getter and setter methods to access and modify them. Also, to implement a method applyDiscount() that reduces the price by a given percentage.


## ALGORITHM :
```
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class Book with private variables: title, author, price.
4.	Write public setter methods to assign values to these variables.
5.	Write public getter methods to retrieve these values.
6.	Define a method applyDiscount(double percent):
     ->Calculate discount amount: discount = price * percent / 100.
  	  ->Subtract the discount from the current price.
7. In the main method:
    ->Create an object of Book.
    ->Use setter methods to assign title, author, and price.
    ->Call applyDiscount() to reduce the price.
    ->Use getter methods to print updated details.
8. End the Program.
```





## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: Sakthi Priya S
RegisterNumber: 212222040140  
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class Book {
    private String title;
    private String author;
    private double price;

    public String getTitle() {
        return title;
    }

    public String getAuthor() {
        return author;
    }

    public double getPrice() {
        return price;
    }


    public void setTitle(String title) {
        this.title = title;
    }

    public void setAuthor(String author) {
        this.author = author;
    }

    public void setPrice(double price) {
        this.price = price;
    }

    public void applyDiscount(double percentage) {
        if (percentage > 0 && percentage <= 100) {
            price = price - (price * (percentage / 100));
        }
}

    public void display() {
        System.out.println("Title: " + title);
        System.out.println("Author: " + author);
        System.out.printf("Discounted Price: %.2f\n", price);
        System.out.println("-------------------------");
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        
        Book book = new Book();

  
        book.setTitle(scanner.nextLine());

        book.setAuthor(scanner.nextLine());

        double price = scanner.nextDouble();
        book.setPrice(price);


        double discount = scanner.nextDouble();

        book.applyDiscount(discount);
         
        book.display();

        scanner.close();
    }
}
```







## OUTPUT:
<img width="1299" height="679" alt="image" src="https://github.com/user-attachments/assets/d810a1cb-cb54-40a0-9385-a7b1fdc8fb17" />




## RESULT:
Thus,the Program is executed Successfully.


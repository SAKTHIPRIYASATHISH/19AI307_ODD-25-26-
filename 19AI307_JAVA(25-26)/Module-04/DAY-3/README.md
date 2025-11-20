# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
Implement a system where a Library contains multiple Book objects. Each Book is created inside the Library. Books can't exist independently (Composition).


## AIM:
To implement a system using composition where a Library contains multiple Book objects. The Book objects are created inside the Library and cannot exist independently of it.


## ALGORITHM :
```
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Book class with properties like title/author.
4.	Create a Library class that:
     ->Contains a list or array of Book objects.
  	  ->Provides a method to create and add new Book objects inside the library.
5. In the Library constructor, initialize the book collection.
6. When a book is added, create a Book object inside the Library method (not in main).
7. In main(), create a Library object.
8. Call the library method to add books.
9. Display all books stored inside the library to confirm composition.
10. End the program.
```





## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: Sakthi Priya S
RegisterNumber: 212222040140 
*/
```

## SOURCE CODE:
```
import java.util.*;

public class CompositionExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Library library = new Library();

        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String title = sc.nextLine();
            String author = sc.nextLine();
            library.addBook(title, author);
        }

        library.showBooks();
        sc.close();
    }
}

class Book {
    private String title;
    private String author;

    public Book(String title, String author) {
        this.title = title;
        this.author = author;
    }

    public String getDetails() {
        return title + " by " + author;
    }
}
class Library {
    private List<Book> books;

    public Library() {
        books = new ArrayList<>();
    }

    
    public void addBook(String title, String author) {
        books.add(new Book(title, author));
    }

    public void showBooks() {
        System.out.println("Books in Library:");
        for (Book b : books) {
            System.out.println("- " + b.getDetails());
        }
    }
}
```







## OUTPUT:
<img width="1293" height="649" alt="image" src="https://github.com/user-attachments/assets/fcb8449b-7dc3-422d-af58-52bc136e9ff2" />




## RESULT:
Thus,the Program is executed Successfully.


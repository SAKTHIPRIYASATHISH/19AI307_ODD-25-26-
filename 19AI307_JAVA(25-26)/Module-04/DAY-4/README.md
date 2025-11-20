# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
You’re creating a cross-platform UI tool using the Abstract Factory pattern. Implement factories to create Button and Checkbox for "dark" and "light" themes. Let the user choose the theme, then generate UI components and display their types


## AIM:
To implement the Abstract Factory Design Pattern that creates UI components (Button and Checkbox) for two themes: Dark and Light.The user selects the theme, and the program generates the corresponding components and displays their types.


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create interfaces for Button and Checkbox.
4.	Create Dark and Light versions of each product.
5.	Make an interface UIFactory with methods to create components.
6.	Implement DarkFactory and LightFactory.
7.	Read user theme choice.Create the matching factory object.
8.	Use the factory to create a Button and a Checkbox.
9.	Print their types.
10.	End the Program.





## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: Sakthi Priya S
RegisterNumber:  212222040140
*/
```

## SOURCE CODE:
```
import java.util.*;


interface Button {
    void render();
}

interface Checkbox {
    void render();
}


class DarkButton implements Button {
    public void render() {
        System.out.println("Dark Button created");
    }
}

class LightButton implements Button {
    public void render() {
        System.out.println("Light Button created");
    }
}

class DarkCheckbox implements Checkbox {
    public void render() {
        System.out.println("Dark Checkbox created");
    }
}

class LightCheckbox implements Checkbox {
    public void render() {
        System.out.println("Light Checkbox created");
    }
}


interface UIFactory {
    Button createButton();
    Checkbox createCheckbox();
}


class DarkThemeFactory implements UIFactory {
    public Button createButton() {
        return new DarkButton();
    }
    public Checkbox createCheckbox() {
        return new DarkCheckbox();
    }
}

class LightThemeFactory implements UIFactory {
    public Button createButton() {
        return new LightButton();
    }
    public Checkbox createCheckbox() {
        return new LightCheckbox();
    }
}


class FactoryProducer {
    public static UIFactory getFactory(String theme) {
        if (theme.equalsIgnoreCase("dark")) {
            return new DarkThemeFactory();
        } else if (theme.equalsIgnoreCase("light")) {
            return new LightThemeFactory();
        }
        return null;
    }
}


public class AbstractFactoryDemo {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String theme = sc.nextLine().trim();

        UIFactory factory = FactoryProducer.getFactory(theme);

        if (factory != null) {
            Button button = factory.createButton();
            Checkbox checkbox = factory.createCheckbox();
            button.render();
            checkbox.render();
        } else {
            System.out.println("Invalid theme");
        }

        sc.close();
    }
}
```






## OUTPUT:
<img width="1295" height="405" alt="image" src="https://github.com/user-attachments/assets/3284a792-bb04-4a86-9df9-b123038eee49" />




## RESULT:
Thus,the Program is executed Successfully.


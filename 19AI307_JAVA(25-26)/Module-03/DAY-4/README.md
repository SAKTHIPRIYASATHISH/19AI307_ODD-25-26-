# Ex.No:3(D)    INTERFACE 

## QUESTION:
```
Two types of traffic controllers decide whether a vehicle can pass based on signal color. The decision logic varies by controller.
 ->AggressiveController: Allows only if "GREEN".
 ->DefensiveController: Allows for "GREEN" or "YELLOW".
Input Format:
signalColor
controllerType
signalColor: A string indicating the signal color (GREEN, YELLOW, RED)
controllerType: An integer (1 for AggressiveController, 2 for DefensiveController)
Output Format:
Print "GO"       → if vehicle is allowed to move  
Print "STOP"     → if vehicle must stop
```


## AIM:
To write a Java program that uses two types of traffic controllers—AggressiveController and DefensiveController—to decide whether a vehicle can move based on the given signal color and controller type.


## ALGORITHM :
```
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the input signalColor (GREEN, YELLOW, RED).
4.	Read the controllerType (1 = Aggressive, 2 = Defensive).
5.	If controllerType = 1 (AggressiveController):
   ->Allow only if signalColor is "GREEN" → Print "GO".
  	->Otherwise → Print "STOP".
6. If controllerType = 2 (DefensiveController):
    ->Allow if signalColor is "GREEN" or "YELLOW" → Print "GO".
    ->Otherwise → Print "STOP".
7. End the program.
```






## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: Sakthi Priya S
RegisterNumber: 212222040140 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;


interface TrafficController {
    String decide(String signalColor);
}


class AggressiveController implements TrafficController {
    public String decide(String signalColor) {
        if (signalColor.equalsIgnoreCase("GREEN"))
            return "GO";
        else
            return "STOP";
    }
}

class DefensiveController implements TrafficController {
    public String decide(String signalColor) {
        if (signalColor.equalsIgnoreCase("GREEN") || signalColor.equalsIgnoreCase("YELLOW"))
            return "GO";
        else
            return "STOP";
    }
}
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        
        String signalColor = sc.next();
        int controllerType = sc.nextInt();
        sc.close();

        TrafficController controller;

        if (controllerType == 1)
            controller = new AggressiveController();
        else if (controllerType == 2)
            controller = new DefensiveController();
        else {
            System.out.println("Invalid controller type");
            return;
        }

        System.out.println(controller.decide(signalColor));
    }
}

```







## OUTPUT:
<img width="1248" height="345" alt="image" src="https://github.com/user-attachments/assets/1956c687-138c-4ef8-badf-1e4885069fd8" />




## RESULT:
Thus,the Program is executed Successfully.


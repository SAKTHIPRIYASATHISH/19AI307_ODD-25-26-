# Ex.No:3(C) ABSTRACTION

## QUESTION:
```
Description:
Create abstract class GameScore with method finalScore().
Subclasses:
ArcadeGame: score = baseScore + (level × 100)
PuzzleGame: score = (attempts ≤ 3) ? 1000 - (attempts × 100) : 500
Input Format:
First line: 1 or 2
Second line: base, level (or attempts)
Output Format:
Final score (int)
```


## AIM:
To write a Java program that defines an abstract class GameScore with an abstract method finalScore(), and two subclasses ArcadeGame and PuzzleGame that compute the final score based on their own rules.


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an abstract class GameScore with an abstract method finalScore().
4.	Create subclass ArcadeGame:
   ->Store baseScore and level.
  	->Implement finalScore() as: score = baseScore + (level × 100)
5. Create subclass PuzzleGame:
    ->Store number of attempts.'
    ->Implement finalScore() as:
        ->If attempts ≤ 3: score = 1000 - (attempts × 100)
        ->Else: score = 500
6. Read input:
     ->If first line = 1 → create ArcadeGame object.
     ->If first line = 2 → create PuzzleGame object.
7. Call the finalScore() method and print the result.
8. End the program.
   





## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: Sakthi Priya S
RegisterNumber:  212222040140
*/
```

## SOURCE CODE:
```
import java.util.*;

abstract class GameScore {
    abstract int finalScore();
}

class ArcadeGame extends GameScore {
    int baseScore, level;

    ArcadeGame(int baseScore, int level) {
        this.baseScore = baseScore;
        this.level = level;
    }

    @Override
    int finalScore() {
        return baseScore + (level * 100);
    }
}

class PuzzleGame extends GameScore {
    int attempts;

    PuzzleGame(int attempts) {
        this.attempts = attempts;
    }

    @Override
    int finalScore() {
        return (attempts <= 3) ? 1000 - (attempts * 100) : 500;
    }
}
public class GameScoreCalculator {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int type = sc.nextInt();
        GameScore game;
        if (type == 1) {
            int base = sc.nextInt();
            int level = sc.nextInt();
            game = new ArcadeGame(base, level);
        } else {
            int attempts = sc.nextInt();
            game = new PuzzleGame(attempts);
        }
        System.out.println(game.finalScore());
    }
}


```







## OUTPUT:
<img width="1239" height="350" alt="image" src="https://github.com/user-attachments/assets/5e345a89-a583-4cde-932f-48ed16128ee6" />





## RESULT:
Thus,the Program is executed Successfully.



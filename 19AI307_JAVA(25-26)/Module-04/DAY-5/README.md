# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Create an Article class where changes to the content are saved as mementos. Let the user view and restore any saved version.


## AIM:
To implement the Memento Design Pattern where an Article class saves its content changes as mementos, allowing the user to view, store, and restore any previous version of the article.


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create Memento to store article content.
4.	Article class saves content using saveToMemento() and restores using restoreFromMemento().
5.	Caretaker keeps a list of mementos
6.	On each content change, store a new memento in the list.
7.	User selects any memento index to view or restore that version.





## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: Sakthi Priya S
RegisterNumber:  212222040140
*/
```

## SOURCE CODE:
```
import java.util.*;
class Article {
    private String content;

    public void setContent(String content) {
        this.content = content;
    }

    public String getContent() {
        return content;
    }

    public ArticleMemento save() {
        return new ArticleMemento(content);
    }

    public void restore(ArticleMemento memento) {
        this.content = memento.getContent();
    }
}
class ArticleMemento {
    private final String content;

    public ArticleMemento(String content) {
        this.content = content;
    }

    public String getContent() {
        return content;
    }
}

class ArticleHistory {
    private List<ArticleMemento> versions = new ArrayList<>();

    public void saveVersion(Article article) {
        versions.add(article.save());
    }

    public ArticleMemento getVersion(int index) {
        if (index >= 0 && index < versions.size()) {
            return versions.get(index);
        }
        return null;
    }
}

public class ArticleManager {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Article article = new Article();
        ArticleHistory history = new ArticleHistory();

        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String content = sc.nextLine();
            article.setContent(content);
            history.saveVersion(article);
        }

        int index = sc.nextInt(); 

        ArticleMemento memento = history.getVersion(index);
        if (memento != null) {
            article.restore(memento);
            System.out.println(article.getContent());
        } else {
            System.out.println("Invalid version");
        }

        sc.close();
    }
}

```







## OUTPUT:
<img width="1252" height="686" alt="image" src="https://github.com/user-attachments/assets/c16ab063-5c19-4477-b835-328b84a50bc6" />




## RESULT:
Thus,the Program is executed Successfully.


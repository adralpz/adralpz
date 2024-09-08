```console
adrianlopez@github:~$ ./welcome.sh
```

```
________________________________________
/ Welcome to my code pasture! Here is    \
| where we cultivate knowledge and       |
\ harvest solutions.                     /
 ----------------------------------------
        \   ^__^
         \  (oo)\_______
            (__)\       )\/\
                ||----w |
                ||     ||
```

```console
adrianlopez@github:~$ cat MyProfile.java
```


```java
public class MyProfile {

    private static final String NAME = "Adrián López Espejo";
    private static final String PROFESSION = "Software Developer";
    private static final String MOTTO = "Embracing failure as a path to mastery";
    private static final String LINKEDIN = "https://www.linkedin.com/in/adrian-lopez-espejo/";
    private static final String[] SKILLS = {
        "Java", "Spring Boot", "Microservices", "SQL", 
        "Git", "OracleDB", "Docker", "CI/CD",
        "TDD", "Kubernetes (learning)", "TypeScript (learning)"
    };
    private static final String LEARNING = "Currently learning Kubernetes and TypeScript, with an interest in Golang.";
    private static final String BOOKS = "Books read: 'Software Craftsmanship' and 'The Pragmatic Programmer'.";

    public static void main(String[] args) {
        MyProfile profile = new MyProfile();
        profile.displayProfile();
    }

    private void displayProfile() {
        printSection(this::printProfileDetails);
        printSection(this::printSkills);
        printSection(this::printLearning);
        printSection(this::printBooks);
        printSection(this::printFooter);
    }

    private void printSection(Runnable section) {
        section.run();
    }

    private void printSkills() {
        System.out.println("Skills      :");
        for (String skill : SKILLS) {
            System.out.printf("    - %s%n", skill);
        }
    }

    private void printLearning() {
        System.out.printf("Learning    : %s%n", LEARNING);
    }

    private void printBooks() {
        System.out.printf("Books       : %s%n", BOOKS);
    }

    private void printFooter() {
        System.out.println("Feel free to explore my work and connect with me");
    }
}
```

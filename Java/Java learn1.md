### Switch statements 
```Java
import java.util.*; // import Scanner class
public class Main {
    public static void main(String[] args) {
        int a, b;
        Scanner input = new Scanner(System.in);
        System.out.println("Enter First Number: ");
        a = input.nextInt();
        System.out.println("Enter Second Number: ");
        b = input.nextInt();
        char c;
        System.out.println("Enter the operator +, -, *, /, or % : ");
        c = input.next().charAt(0);

        // switch statements
        switch (c) {
            case '+':
            System.out.println(a + " + " + b + " = " + (a + b));
            break;
            case '-':
            System.out.println(a + " - " + b + " = " + (a - b));
            break;
            case '*':
            System.out.println(a + " * " + b + " = " + (a * b));
            break;
            case '/':
            System.out.println(a + " % " + b + " = " + (a % b));
            break;
            case '%':
            System.out.println(a + " % " + b + " = " + (a % b));
            break;
            default:
            System.out.println("You have entered incorrect operator!");
        }
    }
}
```
### While Loop Examples
```Java
public class Main {
    public static void main(String[] args) {
        int i = 3;

        while (i > 0) {
            System.out.println(i);
            i--;
        }
        System.out.println("Happy New Year!");
    }
}
```
<p>While loop combined with an if else statement, let's say we play game of Yatzy:</p>

```Java
public class Main {
    public static void main(String[] args) {
        int dice = 1;

        while (dice <= 6) {
            if (dice < 6) {
                System.out.println("No Yatzy.");
            } else {
                System.out.println("Yatzy!");
            }
            dice = dice + 1;
        }
    }
}
```
### For Loop Examples
```Java
public class Main {
    public static void main(String[] args) {
        
        for (int i = 0; i <= 100; i += 10) {
            System.out.println(i);
        }
    }
}
```
```Java
public class Main {
    public static void main(String[] args) {
        
        for (int i = 0; i <= 10; i = i + 2) {
            System.out.println(i);
        }
    }
}
```
```Java
public class Main {
    public static void main(String[] args) {
        int n = 10;

        for (int i = 1; i <= n; i++) {
            System.out.println(i + " x " + n + " = " + (i * n) );
        }
    }
}
```
### Java methods
```Java
public class Main {
    public static void main(String[] args) {
        Main t1 = new Main();
        Main.gmail_method();
        System.out.println("All methods excuted!..");
    }

    static void gmail_method() {
        Main t1 = new Main();
        t1.product_method();
        System.out.println("Index: 10 messages unread!");   // static to non static
    }

    void product_method() {
        Main t1 = new Main();
        t1.windows_method();
        System.out.println("Google products Apps most use android");    // non static to non static
    }

    void windows_method() {
        Main.spotify_method();
        System.out.println("Windows 11 update 11.4.201.001 installing");    // non static to static
    }

    static void spotify_method() {
        Main.college_method();
        System.out.println("Play On High On Love Song");    // static to static
    }

    static void college_method() {
        int a = 2024;
        String b = "recent graduates in ";
        System.out.println("I am Hariharan " + b + a + " completed."); 
    }
}
```
### Output
```
I am Hariharan recent graduates in 2024 completed.
Play On High On Love Song
Windows 11 update 11.4.201.001 installing
Google products Apps most use android
Index: 10 messages unread!
All methods excuted!..
```
### Java method parameters
<p>Parameters and arguments</p>
<p>Java return methods</p>

```Java
public class Main {
    public static void main(String[] args) {
        Main t1 = new Main();
        Main.gmail_method();
        t1.product_method();
        String google = t1.product_method();
        System.out.println(google);
        Main.windows_method("11.4.201.001");
        
        String student = t1.college_method(2024);
        System.out.println("I am Hariharan " + student + " completed.");
        System.out.println("All methods excuted!..");
    }

    static void gmail_method() {
        System.out.println("Index: 10 messages unread!");   // no return, no arguments
    }
    
    String product_method() {
        return "Google products Apps most use android";   // with return, no arguments   
    }

    static void windows_method(String a) {
        System.out.println("Windows 11 update " + a + " Installing");   // no return, with arguments
    }

    String college_method(int a) {
        String b = "recent graduates in " + a;   // with return, with arguments
        return b;   // added return statement
    }
}
```
### Output
```
Index: 10 messages unread!
Google products Apps most use android
Windows 11 update 11.4.201.001 Installing
I am Hariharan recent graduates in 2024 completed.
All methods excuted!..
```
### Java method overloading
<p>Two methods, add numbers different type:</p>

```Java
public class Main {
    static int plus_method(int a, int b) {
        return a + b;
    }

    static double double_method(double a, double b) {
        return a + b;
    }
    public static void main(String[] args) {  
        int t1 = Main.plus_method(5, 10 );
        System.out.println("Int value: " + t1);

        double t2 = Main.double_method(4.5d, 10.5d);
        System.out.println("Double value: " + t2);
       
    }
}
```
<p>methods overloading ( Multiple methods, same name with different parameters )</p>

```Java
public class Main {
    static int plus_method(int a, int b) {
        return a + b;
    }

    static double plus_method(double a, double b) {
        return a + b;
    }

    public static void main(String[] args) {    // methods overloading
        int t1 = Main.plus_method(5, 10 );
        System.out.println("Int value: " + t1);

        double t2 = Main.plus_method(4.5d, 10.5d);
        System.out.println("Double value: " + t2);
       
    }
}
```
### Static vs public
```Java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello World");
        Main.print_A();
    }
    static void print_A() { // static to non static
        System.out.println("Class A");
        Main t1 = new Main();
        t1.print_B();
    }
    public void print_B() { // non static to non static
        System.out.println("Class B");
        Main t2 = new Main();
        t2.print_C();
    }
    public void print_C() { // non static to static
        System.out.println("Class C");
        Main.print_D();
    }
    static void print_D() { // static to static
        System.out.println("Class D");
        Main.print_E();
    }
    static void print_E() {
        System.out.println("Class E");
    }
}
```
### Output
```
Hello World
Class A
Class B
Class C
Class D
Class E
```

### Java Inheritance type
<ol>
    <li>Single Inheritance</li>
    <li>Multilevel Inheritance</li>
    <li>Hierarchical Inheritance</li>
    <li>Multiple Inheritance</li>
    <li>Hybrid Inheritance</li>
</ol>

### Single Inheritance
<p>One parent class and one child class</p>

```Java
class One {
    public void print_A() {
        System.out.println("Class A");
    }
}

class Two extends One {
    public void print_B() {
        System.out.println("Class B");
    }

    public static void main(String[] args) {
        Two t1 = new Two();
        t1.print_A();  // call parent class => One
        t1.print_B();  // call child class => Two
    }
}
```
### Output
```
Class A
Class B
```
### Multilevel Inheritance
<p>One parent class and more than child class</p>

```Java
class One {
    public void gmail_method() {
        System.out.println("Index: 10 messages unread!");
    }
}

class Two extends One {
    public void product_method() { 
        System.out.println("Gooogle products Apps most use android");
    }
}

class Three extends Two {
    public void windows_method() {
        System.out.println("Windows 11 update 11.401.415");
    }
}
    public static void main(String[] args) {
        Three t1 = new Three();
        t1.gmail_method();  // call One class => access attributes, method
        t1.product_method(); // call Two class => access attributes, method
        t1.windows_method(); // call Three class
    }
```
### Hierarchical Inheritance
<p>One child class and more than parent class</p>

```Java

```

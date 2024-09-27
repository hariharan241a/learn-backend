ArithmeticException
-------------------
```java
public class Main {
    public static void main(String[] args) {
        System.out.println(0);
        System.out.println(1);
        System.out.println(2/0); // 2/0 not division value
    }
}
```
`Output`

```
0
1
Exception in thread "main" java.lang.ArithmeticException: / by zero
        at Main.main(Main.java:5)
```
NullPointerException
--------------------
```java
public class Main {
    public static void main(String[] args) {
        String s = null;
        System.out.println(s.length());
    }
}
```
`Output`

```
Exception in thread "main" java.lang.NullPointerException: Cannot invoke "String.length()" because "s" is null
        at Main.main(Main.java:4)
```
StringIndexOutOfBoundsException
-------------------------------
```java
public class Main {
    public static void main(String[] args) {
        String s = "Java"; 
        System.out.println(s.charAt(4));
    }
}
```
`Output`

```
Exception in thread "main" java.lang.StringIndexOutOfBoundsException: Index 4 out of bounds for length 4
        at java.base/jdk.internal.util.Preconditions$1.apply(Preconditions.java:55)
        at java.base/jdk.internal.util.Preconditions$1.apply(Preconditions.java:52)
        at java.base/jdk.internal.util.Preconditions$4.apply(Preconditions.java:213)
        at java.base/jdk.internal.util.Preconditions$4.apply(Preconditions.java:210)
        at java.base/jdk.internal.util.Preconditions.outOfBounds(Preconditions.java:98)
        at java.base/jdk.internal.util.Preconditions.outOfBoundsCheckIndex(Preconditions.java:106)
        at java.base/jdk.internal.util.Preconditions.checkIndex(Preconditions.java:302)
        at java.base/java.lang.String.checkIndex(String.java:4930)
        at java.base/java.lang.StringLatin1.charAt(StringLatin1.java:46)
        at java.base/java.lang.String.charAt(String.java:1629)
        at Main.main(Main.java:4)
```
ArrayIndexOutOfBoundsException
------------------------------
```java
public class Main {
    public static void main(String[] args) {
       int num[] = new int[3];
       num[0] = 10;
       num[1] = 20;
       num[2] = 30;
       System.out.println(num[3]);
    }
}
```
`Output`

```
Exception in thread "main" java.lang.ArrayIndexOutOfBoundsException: Index 3 out of bounds for length 3
        at Main.main(Main.java:7)
```
IndexOutOfBoundsException
-------------------------
```java
import java.util.List;
import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
       List li = new ArrayList();
       li.add(10);
       li.add(20);
       li.add(30);
       System.out.println(li.get(3));
    }
}
```
`Output`

```
Exception in thread "main" java.lang.IndexOutOfBoundsException: Index 3 out of bounds for length 3
        at java.base/jdk.internal.util.Preconditions.outOfBounds(Preconditions.java:100)
        at java.base/jdk.internal.util.Preconditions.outOfBoundsCheckIndex(Preconditions.java:106)
        at java.base/jdk.internal.util.Preconditions.checkIndex(Preconditions.java:302)
        at java.base/java.util.Objects.checkIndex(Objects.java:365)
        at java.base/java.util.ArrayList.get(ArrayList.java:428)
        at Main.main(Main.java:10)
```
NumberFormatException
---------------------
```java
public class Main {
    public static void main(String[] args) {
       String s = "1234@j";
       int num = Integer.parseInt(s);
       System.out.println(num);
    }
}
```
`Output`

```
Exception in thread "main" java.lang.NumberFormatException: For input string: "1234@j"
        at java.base/java.lang.NumberFormatException.forInputString(NumberFormatException.java:67)
        at java.base/java.lang.Integer.parseInt(Integer.java:588)
        at java.base/java.lang.Integer.parseInt(Integer.java:685)
        at Main.main(Main.java:4)
```
InputMismatchException
----------------------
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        System.out.print("enter value: ");

        int Int = scan.nextInt();
        System.out.println(Int);
    }
}
```
`Output`

```
enter value: abc
Exception in thread "main" java.util.InputMismatchException
        at java.base/java.util.Scanner.throwFor(Scanner.java:964)
        at java.base/java.util.Scanner.next(Scanner.java:1619)
        at java.base/java.util.Scanner.nextInt(Scanner.java:2284)
        at java.base/java.util.Scanner.nextInt(Scanner.java:2238)
        at Main.main(Main.java:8)
```

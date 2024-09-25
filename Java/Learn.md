Partial abstraction (abstract class)
------------------------------------
<p>contains use both abstracts and non abstract methods</p>
<p>we can't create object</p>
<p>contains use (extends) keywords</p>

`Yahoo.java`
```java
public abstract class Yahoo {

    abstract void AccountID(); // abstract method not use logic

    public void AccountPwd() { // non abstarct method use any logic
        System.out.println("Login successful..");
    }
    
    abstract void YahooCloud(); // abstract method not use logic
}
```
`LoginPage.java`
```java
public class LoginPage extends Yahoo {
    @Override
    public void AccountID() {
        System.out.println("hariharan123");
    }

    public void YahooCloud() {
        System.out.println("Storage used: 11% of 5 GB");
    }
    public static void main(String[] args) {
        LoginPage scan = new LoginPage();
        scan.AccountID();
        scan.AccountPwd();
        scan.YahooCloud();
    }
}
```
`Output`
```
hariharan123
Login successful..
Storage used: 11% of 5 GB
```
Fully abstraction (interface class)
-----------------------------------
<p>only abstract method use</p>
<p>we can't create object</p>
<p>contains use (implementation) keywords</p>

`Yahoo.java`
```java
public interface Yahoo {

    // only use abstract method
    abstract void AccountID();
    abstract void YahooCloud(); // not use any logic
}
```
`LoginPage.java`
```java
public class LoginPage implements Yahoo {
    @Override
    public void AccountID() {
        System.out.println("hariharan123");
    }

    public void YahooCloud() {
        System.out.println("Storage used: 11% of 5 GB");
    }
    public static void main(String[] args) {
        LoginPage scan = new LoginPage();
        scan.AccountID();
        scan.YahooCloud();
        
    }
}
```
`Output`
```
hariharan123
Storage used: 11% of 5 GB
```
note
----
<p>abstract method      => not use any business logic.</p>
<p>non abstract method  => use any business logic.</p>

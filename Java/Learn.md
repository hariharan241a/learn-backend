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

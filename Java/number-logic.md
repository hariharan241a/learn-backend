<h5>Prime Number Check:</h5>
<p>1. Write a program to check if a given number is a prime number.</p>

`method:1`
```java
import java.util.*;
public class Main {
    // method to check a num
    public static boolean isPrime(int val) {
        // setp1 
        if (val <= 1) {
            return false;
        }

        // step 2
        for (int i = 2; i <= Math.sqrt(val); i++) { // Math.sqrt(17) = 4
            // 2 <= 4
            //step 3
            if (val % i == 0) {
                return false;
            }
        }
        return true;
    }

    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        System.out.print("Enter num: ");

        // read the input num
        int num = scan.nextInt();

        // step 5 check print result
        if (isPrime(num)) { // 17, 6
            System.out.println(num + " is a prime number");
        } else {
            System.out.println(num + " is not prime number");
        }
    }
}
```
<p>Explain iteration:</p>

```
The loop runs with i = 2, 3, 4.
For i = 2, 17 % 2 is 1, so the loop continues.
For i = 3, 17 % 3 is 2, so the loop continues.
For i = 4, 17 % 4 is 1, so the loop continues.
```
`method:2`
```java
public class Main {
    public static void main(String[] args) {
        int val = 17; 
        boolean isPrime = true;
        
        for (int i = 2; i <= Math.sqrt(val); i++) {
            if (val % i == 0) {
                isPrime = false;
                break;
            }
        }
        
        if (isPrime) {
            System.out.println(val + " is a prime number.");
        } else {
            System.out.println(val + " is not a prime number.");
        }
    }
}
```
<h5>Palindrome Number:</h5>
<p>2. Write a program to check if a given number is a palindrome.</p>

```java
public class Main {
    public static void main(String[] args) {
        int num = 123;
        int rem = 0;
        int rev = 0;

        while (num > 0) {
            rem = num % 10;
            rev = rev * 10 + rem;
            num = num / 10;
        }

        if (rev == num) {
            System.out.println("Palindrome");
        } else {
            System.out.println("Not palindrome");
        }

        System.out.println("Reversed number: " + rev);
    }
}
```
<p>Output:</p>

```
Not palindrome
Reversed number: 321
```
<p>Explain iteration:</p>

```
First Iteration:
rem = 123 % 10 → rem = 3
rev = 0 * 10 + 3 → rev = 3
num = 123 / 10 → num = 12

Second Iteration:
rem = 12 % 10 → rem = 2
rev = 3 * 10 + 2 → rev = 32
num = 12 / 10 → num = 1

Third Iteration:
rem = 1 % 10 → rem = 1
rev = 32 * 10 + 1 → rev = 321
num = 1 / 10 → num = 0
```
`method:2`
```java
class Main {
    public static void main(String[] args) {
        int num = 121;
        int originalNum = num; // Store the original number
        int rem = 0;
        int rev = 0;

        while (num > 0) {
            rem = num % 10;
            rev = rev * 10 + rem;
            num = num / 10;
        }

        if (rev == originalNum) {
            System.out.println("Palindrome");
        } else {
            System.out.println("Not palindrome");
        }

        System.out.println("Reversed number: " + rev);
    }
}
```
<p>Output:</p>

```
Palindrome
Reversed number: 121
```
<h5>Reverse a Number:</h5>
<p>3. Write a program to reverse the digits of a given number.</p>

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter a number: ");
        int number = scanner.nextInt();

        int reversedNumber = 0;

        // number without using built-in functions
        while (number != 0) {
            int digit = number % 10;  // get last digit => 4, 3, 2, 0
            reversedNumber = reversedNumber * 10 + digit;  // add reversed number => 4, 43, 432, 
            number /= 10;  // remove last digit from original number => 123, 12, 
        }

        // Output
        System.out.println("Reversed number: " + reversedNumber);
        
        scanner.close();
    }
}
```
<p>Output:</p>

```
Enter a number: 1234
Reversed number: 4321
```
<p>Explain iteration:</p>

```
Step-by-Step Execution:

First Iteration:
Original number: 1234
digit = 1234 % 10 → 4
reversedNumber = 0 * 10 + 4 → 4
number = 1234 / 10 → 123

Second Iteration:
Original number: 123
digit = 123 % 10 → 3
reversedNumber = 4 * 10 + 3 → 43
number = 123 / 10 → 12

Third Iteration:
Original number: 12
digit = 12 % 10 → 2
reversedNumber = 43 * 10 + 2 → 432
number = 12 / 10 → 1

Fourth Iteration:
Original number: 1
digit = 1 % 10 → 1
reversedNumber = 432 * 10 + 1 → 4321
number = 1 / 10 → 0
```
<h5>Sum of digit:</h5>
<p>4. Write a program to find the sum of the digits of a given number.</p>

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int number = scanner.nextInt();

        int sum = 0;

        // Process each digit
        while (number != 0) {
            sum += number % 10; // Add the last digit to the sum
            number /= 10; // Remove the last digit
        }

        System.out.println("The sum of the digits is: " + sum);
    }
}
```
<p>Output:</p>

```
Enter a number: 123
The sum of the digits is: 6
```
<p>Explain iteration:</p>

```
First Iteration:
number = 123
sum += 123 % 10 → sum = 0 + 3 → sum = 3
number /= 10 → number = 123 / 10 → number = 12

Second Iteration:
number = 12
sum += 12 % 10 → sum = 3 + 2 → sum = 5
number /= 10 → number = 12 / 10 → number = 1

Third Iteration:
number = 1
sum += 1 % 10 → sum = 5 + 1 → sum = 6
number /= 10 → number = 1 / 10 → number = 0
```
<h5>Check Number Odd or Even:</h5>
<p>5. Java program to check if the given number is a odd or even number.</p>

`Using Bitwise AND Operator`
```java
public class Main {
    public static void main(String[] args) {
        int num = 23;
        if ((num & 1) == 0) {
            System.out.println("even number"); // 23 & 1 = 1, 1 == 0
        } else {
            System.out.println("odd number");
        }
    }
}
```
`Using Modulus Operator`
```java
public class Main {
    public static void main(String[] args) {
        int num = 23;
        if (num % 2 == 0) {
            System.out.println("even number"); // 23 % 2 = 1, 1 == 0
        } else {
            System.out.println("odd number");
        }
    }
}
```
`Using Division and Multiplication`
```java
public class Main {
    public static void main(String[] args) {
        int num = 23;
        if ((num / 2) * 2 == num) {	// ((23 / 2) * 2 == 23) | 23 / 2 = 11           
            System.out.println("even number");
        } else {
            System.out.println("odd number");
        }
    }  
}
```
<h5>Count and Sum Odd Numbers:</h5>
<p>6. Print of odd number in b/w 1 to 100.</p>

```java
class Main {
    public static void main(String[] args) {
        int count = 0, sum = 0;
        
        for (int i = 1; i <= 100; i++) {
            if ((i % 2) == 1) { // Check if the number is odd
                count++;
                sum = sum + i;
            }
        }
        System.out.println("count: " + count);
        System.out.println("sum: " + sum);
    }
}
```
<p>Output:</p>

```
count: 50
sum: 2500
```
<p>Explain iteration:</p>

```
Iteration 1 (i = 1):
(1 % 2) == 1 is true (1 is odd).
count is incremented to 1.
sum is updated to 1 (sum = 0 + 1).

Iteration 2 (i = 2):
(2 % 2) == 1 is false (2 is even).
count remains 1.
sum remains 1.

Iteration 3 (i = 3):
(3 % 2) == 1 is true (3 is odd).
count is incremented to 2.
sum is updated to 4 (sum = 1 + 3).

Iteration 4 (i = 4):
(4 % 2) == 1 is false (4 is even).
count remains 2.
sum remains 4.

Iteration 5 (i = 5):
(5 % 2) == 1 is true (5 is odd).
count is incremented to 3.
sum is updated to 9 (sum = 4 + 5).
```
<h5>Swap Two Numbers:</h5>
<p>7. Swap two numbers with using a third variable in java.</p>

```java
Swap the number a = 20, b = 50,
class Main {
    public static void main(String[] args) {
        int a = 20, b = 50, c = 0; // c temp variable
        System.out.println("before swapping a: " + a);
        System.out.println("before swapping b: " + b);
        
        // logical
        c = a; // c = 0, a = 20, == 20
        a = b; // a = 20, b = 50 == 50
        b = c; // c = a == 20
        System.out.println("after swapping a: " + a);
        System.out.println("after swapping b: " + b);
    }
}
```
<p>Output:</p>

```
before swapping a: 20
before swapping b: 50
after swapping a: 50
after swapping b: 20
```
<h5>Swap Without Third Variable:</h5>
<p>8. Swap two numbers without using a third variable in java.</p>

```java
class Main {
    public static void main(String[] args) {
        int a = 20, b = 50;

        System.out.println("before swapping a: " + a);
        System.out.println("before swapping b: " + b);

        // Swapping logic using arithmetic
        a = a + b; // a = 20 + 50 = 70
        b = a - b; // b = 70 - 50 = 20
        a = a - b; // a = 70 - 20 = 50

        System.out.println("after swapping a: " + a);
        System.out.println("after swapping b: " + b);
    }
}
```
<p>Output:</p>

```
before swapping a: 20
before swapping b: 50
after swapping a: 50
after swapping b: 20
```

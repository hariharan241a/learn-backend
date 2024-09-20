<h4>Triangle pattern</h4>
<p>Increasing triangle</p>
<ol>
  <li>Left increasing triangle</li>
  <li>Right increasing triangle</li>
</ol>
<p>Decreasing triangle</p>
<ol>
  <li>Left decreasing triangle</li>
  <li>Right decreasing triangle</li>
</ol>

<h4>Left increasing triangle</h4>

```Java
class Pattern {
    public static void main(String[] args) {
        int n = 6;

        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print("*");     
            }
            System.out.println();
        }
    }
}
```
<h4>Output</h4>

```
* 
* * 
* * * 
* * * * 
* * * * * 
* * * * * * 
```
<h4>Left decreasing triangle</h4>

```Java
class Pattern {
    public static void main(String[] args) {
        int n = 6;

        for (int i = n; i >= 1; i--) {
            for (int j = 1; j <= i; j++) {
                System.out.print("*");     
            }
            System.out.println();
        }
    }
} 
```
<h4>Output</h4>

```
* * * * * * 
* * * * * 
* * * * 
* * * 
* * 
* 
```
<h4>Right increasing triangle</h4>

```Java
class Pattern {
    public static void main(String[] args) {
        int n = 7;

        for(int i = 1; i <= n; i++) {
            for(int j = i; j < n; j++) {
                System.out.print("  ");
            }
            for(int j = 1; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}
```
<h4>Output</h4>

```
          * 
        * * 
      * * * 
    * * * * 
  * * * * * 
* * * * * * 
```
<h4>Right decreasing triangle</h4>

```Java
class Pattern {
    public static void main(String[] args) {
        int n = 7;  // count of line

        for (int i = n; i >= 1; i--) {
            // print leading spaces
            for (int j = n; j > i; j--) {
                System.out.print("  ");
            }
            // print stars with spaces between them
            for (int j = 1; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}
```
<h4>Output</h4>

```
* * * * * * 
  * * * * * 
    * * * * 
      * * * 
        * * 
          * 
```

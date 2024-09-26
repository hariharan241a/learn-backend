<h5>List</h5>
<p>List is pre-defined interface which is present in java.util package</p>
<p>List is an index based</p>
<p>List allows duplicate</p>
<p>List prints in insertion order</p>
<h5>Types of List (OR) Classes of List:</h5>
<ul>
  <li>ArrayList</li>
  <li>LinkedList</li>
  <li>Vector</li>
  <li>Stack</li>
</ul>

```Java
import java.util.List;
import java.util.ArrayList;

public class ArraylistClass {
    public static void main(String[] args) {
        List li = new ArrayList<>(); 
        
        // to add the value
        li.add(10);
        li.add("Java");
        li.add('M');
        li.add(10);
        li.add(true);

        // print List
        System.out.println(li); // Output: [10, Java, M, 10, true]

        // List get size
        int size = li.size();
        System.out.println(size); // Output: 5
        
        // List set value
        li.set(1, 5.4);
        System.out.println(li); // Output: [10, 5.4, M, 10, true]

        // remove value
        li.remove(2);
        System.out.println(li); // Output: [10, 5.4, 10, true]

        // iterating using for loop
        for (int i = 0; i < li.size(); i++) {
            System.out.println(li.get(i)); // Outputs: 10, 5.4, 10, true
        }

        // for-each loop
        for (Object i : li) {
            System.out.println(i); // Outputs: 10, 5.4, 10, true
        }

        // check value
        boolean contains = li.contains(10);
        System.out.println(contains); // Output: true
    }
}
```
```Java
import java.util.ArrayList;
import java.util.List;
import java.util.Collections;

public class Main {
    public static void main(String[] args) {
        List<Integer> li = new ArrayList<>();

        // add items
        li.add(20);
        li.add(40);
        li.add(10);
        li.add(70);
        li.add(30);

        // print console
        System.out.println(li); // Output: [20, 40, 10, 70, 30]

        // insert elements
        li.add(2, 100);
        System.out.println(li); // Output: [20, 40, 100, 10, 70, 30]

        // access elements
        int get = li.get(4);
        System.out.println(get); // Output: 70

        // change elements
        li.set(4, 25);
        System.out.println(li); // Output: [20, 40, 100, 10, 25, 30]

        // check elements
        boolean contain = li.contains(100);
        System.out.println(contain); // Output: true

        // remove elements
        li.remove(1);
        System.out.println(li); // Output: [20, 100, 10, 25, 30]

        // List elements size
        System.out.println(li.size()); // Output: 5

        // Loop through a List using for-loop
        for (int i = 0; i < li.size(); i++) {
            System.out.println(li.get(i)); // Outputs: 20, 100, 10, 25, 30
        }

        // Loop through a List using for-each loop
        for (int i : li) {
            System.out.println(i); // Outputs: 20, 100, 10, 25, 30
        }

        // sort List
        Collections.sort(li);
        System.out.println(li); // Output: [10, 20, 25, 30, 100]

        // clear elements in List 
        li.clear();
        System.out.println(li); // Output: []
    }
}
```

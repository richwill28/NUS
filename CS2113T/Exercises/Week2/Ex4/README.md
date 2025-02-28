## \[Key Exercise\] `getMultipleGradeCaps` Method

Add the following method to the class given below.

- `public static double[] getMultipleGradeCaps(String[] grades)`: Returns the 
CAP values of the given `grades`. e.g., if the input was the array 
`["A+", "B"]`, the method returns `[5.0, 3.5]`. The mapping from grades to CAP 
is given below.

| A+   | A    | A-   | B+   | B    | B-   | C    | Else |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| 5.0  | 5.0  | 4.5  | 4.0  | 3.5  | 3.0  | 2.5  | 0.0  |

<mark>Do not change the code of the <code>main</code> method!</mark>

```java
public class Main {
    // ADD YOUR CODE HERE

    public static double getGradeCap(String grade) {
        double cap = 0;
        switch (grade) {
        case "A+":
        case "A":
            cap = 5.0;
            break;
        case "A-":
            cap = 4.5;
            break;
        case "B+":
            cap = 4.0;
            break;
        case "B":
            cap = 3.5;
            break;
        case "B-":
            cap = 3.0;
            break;
        case "C":
            cap = 2.5;
            break;
        default:
        }
        return cap;
    }

    public static void main(String[] args) {
        String[] grades = new String[]{"A+", "A", "A-"};
        double[] caps = getMultipleGradeCaps(grades);
        for (int i = 0; i < grades.length; i++) {
            System.out.println(grades[i] + ":" + caps[i]);
        }
    }
}
```

⬇️

```console
A+:5.0
A:5.0
A-:4.5
```

<details>
  <summary>Hint</summary>

  Partial solution:
  
  ```java
  public static double[] getMultipleGradeCaps(String[] grades) {
      double[] caps = new double[grades.length];
      for (int i = 0; i < grades.length; i++) {
          // ...
      }
      return caps;
  }
  ```
</details>

Website: https://nus-cs2113-ay2122s1.github.io/website/schedule/week2/topics.html#key-exercise-getmultiplegradecaps-method

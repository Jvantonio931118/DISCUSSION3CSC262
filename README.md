import java.util.ArrayList;

public class Main {

    public static void main(String[] args) {

        // ===== Example 1: Array =====
        // Arrays have a FIXED SIZE decided at creation.
        int[] examScoresArray = new int[3];
        examScoresArray[0] = 85;
        examScoresArray[1] = 90;
        examScoresArray[2] = 95;

        System.out.println("Array contents:");
        for (int i = 0; i < examScoresArray.length; i++) {
            System.out.println("Index " + i + ": " + examScoresArray[i]);
        }

        // If we want to "add" another score, we CANNOT resize the array.
        // We would need to create a new, larger array and copy the values.
        // This shows that arrays are not convenient when the size changes often.


        // ===== Example 2: ArrayList =====
        // ArrayList is a RESIZABLE collection backed by an internal array.
        // It can only store objects, so we use Integer instead of int.
        ArrayList<Integer> examScoresList = new ArrayList<>();

        // We can add elements without worrying about capacity.
        examScoresList.add(85);
        examScoresList.add(90);
        examScoresList.add(95);

        // Adding another element is simple; ArrayList resizes itself.
        examScoresList.add(100);

        System.out.println("\nArrayList contents:");
        for (int i = 0; i < examScoresList.size(); i++) {
            System.out.println("Index " + i + ": " + examScoresList.get(i));
        }

        // We can also remove elements by index, which shifts the remaining items.
        examScoresList.remove(1); // removes the value 90
        System.out.println("\nArrayList after removing index 1:");
        for (int i = 0; i < examScoresList.size(); i++) {
            System.out.println("Index " + i + ": " + examScoresList.get(i));
        }

        // ===== Key Differences Highlighted in Code =====
        // 1. Array: fixed length, can store primitives, no built-in add/remove methods.
        // 2. ArrayList: dynamic size, stores objects (Integer), has helpful methods like add(), remove(), size().
        // 3. Syntax: array uses [], ArrayList uses methods and generics.
    }
}

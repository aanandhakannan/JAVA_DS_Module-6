# Ex2 Count how many times a number appears in an array recursively.
## DATE: 17.09.2026
## AIM:
To write a Java program to Count how many times a number appears in an array recursively.

## Algorithm
1. Start
   
2.Read the number of elements (e.g., number of heartbeat readings).

3.Store all readings in an array.

4.Call a recursive function findMin(arr, index)
If index == arr.length - 1, return arr[index]
Else return min(arr[index], findMin(arr, index + 1))

5.Print the minimum value returned by the recursive function.

6.End   

## Program:
```
/*
Program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.
Developed by: YASHWANTH K
RegisterNumber: 212224040369
*/
import java.util.*;

public class Main {
    static int getMin(int[] arr, int i, int n) {
        if (i == n - 1) {
            return arr[i];
        }

    
        int minRest = getMin(arr, i + 1, n);
       
        return Math.min(arr[i], minRest);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }
        System.out.println(getMin(arr, 0, n));
    }
}
```

## Output:

<img width="649" height="254" alt="image" src="https://github.com/user-attachments/assets/e2c774aa-cc92-40f6-acb8-778042dd4078" />

## Result:
Thus, the Java program to Count how many times a number appears in an array recursively is implemented successfully.

# EX 1 You’re creating a health monitoring device which stores several sensor readings in an array. To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.
## DATE: 17.09.2026
## AIM:
To write a JAVA program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.

## Algorithm
1. Start
 
2.Read the number of elements (e.g., number of heartbeat readings).

3.Store all readings in an array.

4.Call a recursive function findMin(arr, index) If index == arr.length - 1, return arr[index] Else return min(arr[index], findMin(arr, index + 1))

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

<img width="617" height="290" alt="image" src="https://github.com/user-attachments/assets/868e66b2-af96-46f6-9443-f5ed467f667a" />


## Result:
Thus the JAVA prograM ti find the minimum value (e.g., lowest heartbeat), implement a recursive method has implemented successfully

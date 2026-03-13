# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Maintain two int variables a and b, read their initial values from user. Use synchronized block to swap them and print swapped values.

# Input:
- Two lines: a and b values
# Output:
- a = <swapped_a>
- b = <swapped_b>

## AIM:
To write a Java program that demonstrates the use of the synchronized block by swapping two numbers safely using a lock object.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'.
3.	Read two integer values from the user.
4.	Create a lock object to control synchronization.
5.	Use a synchronized block with the lock object.
6.	nside the synchronized block, swap the values of the two variables using a temporary variable.
7.	After swapping, display the updated values of both variables.
8.	End the program.





## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: VESHWANTH.
RegisterNumber:  212224230300
*/
```

## SOURCE CODE:
    
    import java.util.Scanner;
    
    public class SwapUsingSync {
        public static void main(String[] args) {
            Scanner sc = new Scanner(System.in);
    
            int a = sc.nextInt();
            int b = sc.nextInt();
    
            Object lock = new Object();
    
            synchronized (lock) {
                int temp = a;
                a = b;
                b = temp;
            }
    
            System.out.println("a = " + a);
            System.out.println("b = " + b);
        }
    }
    




## OUTPUT:
<img width="1269" height="322" alt="image" src="https://github.com/user-attachments/assets/a83486ec-77c8-4a20-b9c4-776de095d1f8" />



## RESULT:
The program successfully demonstrates synchronization by swapping two numbers within a synchronized block, ensuring thread-safe execution even though only one thread is used.

# Ex.No:2(B) METHODS

## QUESTION:
Write a Java program with instance method calculateSum() that sums elements of an integer array. Class name is ArrayOps. Return type is int.

## AIM:
To write a Java program with instance method calculateSum() that sums elements of an integer array. Class name is ArrayOps. Return type is int.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the number of elements n from the user.
4.	Create an array arr of size n.
5.	Read n elements from the user and store them in the array.
6.	Call the function calculateSum(arr) to add all elements of the array.
7.	Print the sum of the array elements and stop the program.





## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: VESHWANTH.
RegisterNumber:  212224230300
*/
```

## SOURCE CODE:

    import java.util.*;
    public class ArrayOps {
    
        public static int calculateSum(int [] arr) {
            int sum=0;
            for(int i=0;i<arr.length;i++){
                sum+=arr[i];
            }
            return sum;
        }
    
        public static void main(String[] args) {
            Scanner sc=new Scanner(System.in);
            int n=sc.nextInt();
            int arr[]=new int[n];
            for(int i=0;i<n;i++){
                arr[i]=sc.nextInt();
            }
            int result=calculateSum(arr);
            System.out.println(result);
        }
    }
    




## OUTPUT:

<img width="1285" height="279" alt="image" src="https://github.com/user-attachments/assets/4ed064e3-ce2e-4d15-aea7-e74cb94f20b8" />


## RESULT:
Thus, the Java program successfully reads n elements from the user, calculates the sum of all array elements using a method, and displays the total sum as the output.

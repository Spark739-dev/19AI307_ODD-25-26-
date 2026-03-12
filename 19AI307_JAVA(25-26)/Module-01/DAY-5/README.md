# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a Java program to calculate the power of a given number.

## AIM:
To write a Java program to calculate the power of a given number.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Import the Scanner class and create a Scanner object to read input.
4.	Read the values of base and exponent from the user.
5.	Use the Math.pow(base, exp) function to calculate the power.
6.	Store the result in a variable called result.
7.	Display the result and end the program.





## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by: VESHWANTH.
RegisterNumber:  212224230300
*/
```

## SOURCE CODE:

    import java.util.Scanner;
    
    public class Main {
        public static void main(String[] args) {
            Scanner sc = new Scanner(System.in);
    
            double base = sc.nextDouble();
            double exp = sc.nextDouble();
    
            double result = Math.pow(base, exp);
    
            System.out.println(base + " raised to the power of " + exp + " is: " + result);
        }
    }






## OUTPUT:
<img width="1291" height="342" alt="image" src="https://github.com/user-attachments/assets/1a98322d-b7d0-47f2-bdba-37044f267f1e" />



## RESULT:
Therefore the program successfully reads a number and calculates the power of a given number.

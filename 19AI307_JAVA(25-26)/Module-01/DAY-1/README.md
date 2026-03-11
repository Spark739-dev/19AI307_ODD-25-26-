# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
Lovely has mastered printing in Java, and now she wants to learn how arithmetic operators work. She’s curious about how Java can add, subtract, multiply, divide, and find remainders of two numbers.

Write a Java program that:

Accepts two integer numbers from the user.

Demonstrates all 5 arithmetic operations:

Addition (+)

Subtraction (-)

Multiplication (*)

Division (/)

Modulus (%)

Displays the result of each operation in a separate line with a clear message.

## AIM:
To write a Java program that reads two integer numbers from the user and performs basic arithmetic operations such as addition, subtraction, multiplication, division, and modulus, and displays the results.

## ALGORITHM :
1.	Start the program.
2.	Create an object of the Scanner class to take input from the user.
3. Read the first integer input from the user and store it in variable num1.
4. Read the second integer input from the user and store it in variable num2.
5. Calculate the sum of num1 and num2, and display the result.
6. Calculate the difference (num1 - num2), and display the result.
7. Calculate the product of num1 and num2, and display the result.
8. Calculate the quotient of num1 divided by num2, and display the result.
9. Calculate the remainder of num1 divided by num2, and display the result.
10. End the program.



## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: VESHWANTH.
RegisterNumber:  212224230300
*/
```

## Sourcecode.java:

    import java.util.*;
        public class helloworld{
            public static void main(String[] args){
                Scanner scan = new Scanner(System.in);
                int num1 = scan.nextInt();
                int num2 = scan.nextInt();
                int sum = num1 + num2;
                int diff = num1 - num2;
                int prod = num1*num2;
                int quotient = num1/num2;
                int rem = num1 % num2;
                System.out.println("Sum = "+ sum);
                System.out.println("Difference = "+ diff);
                System.out.println("Product = "+ prod);
                System.out.println("Quotient = "+ quotient);
                System.out.printf("Remainder = %d",rem );
            }
        }





## OUTPUT:
<img width="1297" height="271" alt="image" src="https://github.com/user-attachments/assets/4732aced-72f1-4be4-a20d-7806c1629802" />



## RESULT:
Thus,The given java program to write simple arithmetic calculator is successfully executed.


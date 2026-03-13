# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to reverse a number using the Integer wrapper class and compare it with the original number.

## AIM:
To write a Java program to reverse a number using the Integer wrapper class and compare it with the original number.

## ALGORITHM :
1.	Start the program.
2.	Import the java.util package to use the Scanner class for user input.
3.	Create the main class and define the main() method.
4.	Create a Scanner object to read an integer from the user.
5.	Read the input number and store it in variable num.
6.	Assign the value of num to Integer a and copy it to a temporary variable temp.
7.	Initialize variables remainder and reversed = 0.
8.	Use a while loop to reverse the number by extracting digits using temp % 10 and building the reversed number.
9.	Compare the original number a with the reversed number reversed.
10.	If both are equal, print that the number is a palindrome; otherwise print that it is not a palindrome and display the reversed number.





## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: VESHWANTH.
RegisterNumber:  212224230300
*/
```

## SOURCE CODE:
     import java.util.*;
     public class main{
         public static void main(String[] args){
             Scanner sc=new Scanner(System.in);
             int num=sc.nextInt();
             Integer a=num;
             int remainder;
             int reversed=0;
             int temp=a;
             while(temp>0){
                 remainder=temp%10;
                 reversed=reversed*10+remainder;
                 temp/=10;
             }
             if(a==reversed){
                 System.out.println(a+" is a palindrome number.");
             } else{
                 System.out.println(a+" is not a palindrome number."); 
                 System.out.println("Reversed Number: "+reversed);
             }
         }
     }
     





## OUTPUT:
<img width="1242" height="406" alt="image" src="https://github.com/user-attachments/assets/ffe062d6-3616-4d6f-b145-1b6847ad2f8d" />



## RESULT:
The program was executed successfully. It accepts an integer from the user, reverses the digits of the number, and checks whether the number is a palindrome. If the original number and the reversed number are the same, it prints that the number is a palindrome; otherwise, it prints that it is not a palindrome and displays the reversed number.

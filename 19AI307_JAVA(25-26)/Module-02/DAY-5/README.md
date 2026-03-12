# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Calculator with: One non-static method add(int a, int b) that returns the sum, One static method info() that says "Calculator is ready".

## AIM:
To create a class Calculator with: One non-static method add(int a, int b) that returns the sum, One static method info() that says "Calculator is ready".

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class Calculator with a method calc(int num1, int num2) to return the sum of two numbers.
4.	Define a static method info() that returns the message "Calculator is ready".
5.	Create the main class prog containing the main method.
6.	Create a Scanner object to read two integers num1 and num2 from the user.
7.	Create an object c of the Calculator class.
8.	Call info() method to display the ready message and call calc(num1, num2) to compute the sum.Call info() method to display the ready message and call calc(num1, num2) to compute the sum.
9.	Display the result (sum of the two numbers) and stop the program.





## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: VESHWANTH.
RegisterNumber:  212224230300
*/
```

## SOURCE CODE:

    import java.util.Scanner;
    
    class Calculator {
       
       public int calc(int num1,int num2){
           return num1+num2;
       }
       
       public static String info(){
           return "Calculator is ready";
       }
    }
    
    class prog {
        public static void main(String[] args) {
            Scanner sc=new Scanner(System.in);
            int num1=sc.nextInt();
            int num2=sc.nextInt();
            Calculator c=new Calculator();
            System.out.println(c.info());
            System.out.println("Sum: "+ c.calc(num1,num2));
        }
    }





## OUTPUT:

<img width="1292" height="413" alt="image" src="https://github.com/user-attachments/assets/43bc1b46-e7a1-4a0b-ada7-46c3f1a2dec5" />


## RESULT:
Thus, the program successfully reads two numbers from the user, displays a message indicating the calculator is ready, and calculates and prints the sum of the two numbers using the calc() method.

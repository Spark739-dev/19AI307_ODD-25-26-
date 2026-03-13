# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
You have a program that reads an integer from the user. The program must reject any negative number by throwing a special error.How would you design a custom exception to handle this? What message would you display if the user enters a negative number?



## AIM:
To develop a Java program that creates and uses a custom exception to validate user input and reject negative numbers, displaying an appropriate error message when a negative number is entered.

## ALGORITHM :
1.	Start the program.
2.	Import the java.util package and create a Scanner object to read input from the user.
3. Use a try block to read an integer value from the user.
4. Check if the entered number is less than 0.
5. If the number is negative, throw an IllegalArgumentException.
6. Catch the exception in the catch block and display the message "Negative numbers are not allowed"; otherwise print "Valid input: number".
	





## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: VESHWANTH.
RegisterNumber:  212224230300
*/
```

## SOURCE CODE:
    import java.util.*;
    public class main{
        public static void main(String[] args){
            Scanner sc=new Scanner(System.in);
            try{
                int num=sc.nextInt();
                if(num<0){
                    throw new IllegalArgumentException();
                }
                System.out.println("Valid input: "+num);
            }
            catch(IllegalArgumentException e){
                System.out.println("Negative numbers are not allowed");
            }
        }
    }
    





## OUTPUT:
<img width="1296" height="433" alt="image" src="https://github.com/user-attachments/assets/31ccb911-592a-47ba-82f7-8da2ea32cbb7" />



## RESULT:
The program was executed successfully. It reads an integer from the user and checks whether the number is negative. If the user enters a negative number, the program throws an exception and displays the message "Negative numbers are not allowed". If the number is positive, the program prints "Valid input" along with the entered number.

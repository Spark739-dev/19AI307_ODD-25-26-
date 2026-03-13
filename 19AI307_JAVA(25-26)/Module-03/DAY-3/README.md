# Ex.No:3(C) ABSTRACTION

## QUESTION:
Create abstract class BankAccount with method calculateInterest(). Extend it in SavingsAccount and FixedDepositAccount.

Input Format:

First line: 1 for SavingsAccount, 2 for FixedDepositAccount
- If 1: next line → balance (double)
- If 2: next line → amount (double) and years (int)

Output Format:

- A single line showing interest earned rounded to 2 decimal places.

## AIM:
To create abstract class BankAccount with method calculateInterest(). Extend it in SavingsAccount and FixedDepositAccount.

## ALGORITHM :
1.	Start the program.
2.	Import the java.util package to use the Scanner class for input.
3.	Create an abstract class BankAccount with an abstract method calculateInterest().
4.	Create a class SavingsAccount that extends BankAccount.
5.	Declare a variable balance in SavingsAccount and create a constructor to initialize it.
6.	Override the calculateInterest() method in SavingsAccount to return balance * 0.04.
7.	Create another class FixedDepositAccount that extends BankAccount.
8.	Declare variables amount and years, and create a constructor to initialize them.
9.	Override the calculateInterest() method in FixedDepositAccount to return amount * 0.07 * years.
10.	In the main method, create a Scanner object to read user input.
11.	Read the user’s choice and create either a SavingsAccount object or a FixedDepositAccount object based on the input values.
12.	Call calculateInterest() using the BankAccount reference, display the result using System.out.printf, and end the program.




## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: VESHWANTH.
RegisterNumber:  212224230300
*/
```

## SOURCE CODE:
    import java.util.*;
    
    abstract class BankAccount {
        abstract double calculateInterest();
    }
    
    class SavingsAccount extends BankAccount {
        double balance;
    
        SavingsAccount(double balance) {
            this.balance = balance;
        }
    
        @Override
        double calculateInterest() {
            return balance * 0.04;   
        }
    }
    
    class FixedDepositAccount extends BankAccount {
        double amount;
        int years;
    
        FixedDepositAccount(double amount, int years) {
            this.amount = amount;
            this.years = years;
        }
    
        @Override
        double calculateInterest() {
            return amount * 0.07 * years;   
        }
    }
    
    class prog {
        public static void main(String[] args) {
            Scanner sc = new Scanner(System.in);
    
            int choice = sc.nextInt();
            BankAccount account;
    
            if (choice == 1) {
                double balance = sc.nextDouble();
                account = new SavingsAccount(balance);
            } else {
                double amount = sc.nextDouble();
                int years = sc.nextInt();
                account = new FixedDepositAccount(amount, years);
            }
    
            double interest = account.calculateInterest();
            System.out.printf("%.2f", interest);
        }
    }
    






## OUTPUT:
<img width="1296" height="457" alt="image" src="https://github.com/user-attachments/assets/52c77002-07eb-4d7e-b2da-aba0c356ea15" />



## RESULT:
The program was executed successfully. It reads the user’s choice and account details, creates the appropriate account object (SavingsAccount or FixedDepositAccount), calculates the interest using the overridden calculateInterest() method, and displays the calculated interest formatted to two decimal places.


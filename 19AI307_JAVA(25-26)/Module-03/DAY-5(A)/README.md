# Ex.No:3(E) ENUM

## QUESTION:
Write a Java program to define an enum named GameLevel with three constants: EASY, MEDIUM, and HARD.

## AIM:
To write a Java program that defines an enum named GameLevel with constants EASY, MEDIUM, and HARD, and allows the user to select a game level.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'.
3.	Define an enum GameLevel with constants: EASY, MEDIUM, HARD.
4.	Read user input as a string and convert it to uppercase.
5.	Use GameLevel.valueOf() to match the input with an enum constant.
6.	If the value matches, print the selected game level.
7.	If no match is found, catch IllegalArgumentException and show an error message.
8.	Close the scanner in the finally block.









## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: VESHWANTH.
RegisterNumber:  212224230300
*/
```

## SOURCE CODE:
    import java.util.Scanner;
    
    enum GameLevel {
        EASY, MEDIUM, HARD;
    }
    
    public class Game {
        public static void main(String[] args) {
            Scanner scanner = new Scanner(System.in);
            String userInput = scanner.nextLine().toUpperCase();
    
            try {
                GameLevel level = GameLevel.valueOf(userInput);
                System.out.println("You selected game level: " + level);
            } catch (IllegalArgumentException e) {
                System.out.println("Invalid game level entered.");
            } finally {
                scanner.close();
            }
        }
    }
    
           
       
        
    




## OUTPUT:
<img width="1241" height="335" alt="image" src="https://github.com/user-attachments/assets/67e9b5da-4aff-4ab7-9718-c4c27facc046" />




## RESULT:
Therefore the program successfully reads a game level from the user and maps it to the corresponding enum constant.

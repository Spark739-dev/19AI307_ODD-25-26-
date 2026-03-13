# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Ask the user for name, age, and email address. Write the collected data into a file called userdata.txt in a structured format.

## AIM:
To ask the user for name, age, and email address. Write the collected data into a file called userdata.txt in a structured format.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util' and 'java.io*'.
3. Create a Scanner object to read user input.
4. Create a file object named "userdata.txt" to store user information.
5. Read user details such as name, age, and email from the user.
6. Create a FileWriter object and write the entered name, age, and email into the file.
7. Display the entered user information (name, age, and email) on the console.
8. Handle possible IOException using a try-catch block and end the program.	





## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: VESHWANTH.
RegisterNumber:  212224230300
*/
```

## SOURCE CODE:

    import java.util.*;
    import java.io.*;
    public class main{
        public static void main(String[] args){
            Scanner sc=new Scanner(System.in);
            try{
                File n = new File("userdata.txt");
                String s=sc.nextLine();
                int age=sc.nextInt();
                sc.nextLine();
                String add=sc.nextLine(); 
                FileWriter writer = new FileWriter(n);
                writer.write(s);
                writer.write(age); 
                writer.write(add); 
                System.out.println("User Information");
                System.out.println("================");
                System.out.println("Name  : "+s);
                System.out.println("Age   : "+age); 
                System.out.println("Email : "+add); 
            }
            catch(IOException e){
                e.printStackTrace();
            }
            
        }
    }
    




## OUTPUT:
<img width="1234" height="388" alt="image" src="https://github.com/user-attachments/assets/99a6b512-8d8b-4cc7-a045-65d678bd590d" />



## RESULT:
The program successfully reads user information (Name, Age, and Email) from the user, writes the data into the file userdata.txt, and displays the entered details on the console. The file operation is handled using FileWriter, and any file-related errors are managed using a try-catch block for IOException.

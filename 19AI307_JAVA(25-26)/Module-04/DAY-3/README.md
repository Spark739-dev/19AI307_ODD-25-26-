# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
A Department contains Professor objects, but professors can exist independently. If no inputs gets passed, print "No professors assigned."

## AIM:
To write a Java program demonstrating aggregation, where a Department contains multiple Professor objects, but professors can exist independently. If no professors are assigned, the program should display "No professors assigned.".

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Professor class with a name attribute and a constructor to initialize it.
4.	Create a Department class with a department name,an array of Professor objects,a counter to track assigned professors.
5.	Implement addProfessor() to store a professor in the array.
6.	Implement showProfessors() which prints the department name,checks whether any professors are assigned, prints "No professors assigned." if the count is zero, otherwise prints the list of professors.
7.	Read the number of professors.
8.	Create professor objects only if input is provided.
9.	Read department name (with fallback default).
10.	Create a Department object and add professor objects into it.
11.	Call showProfessors() to display the results.





## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: VESHWANTH.
RegisterNumber:  212224230300
*/
```

## SOURCE CODE:
     import java.util.*;
     
     class Professor {
         String name;
         Professor(String name) {
             this.name = name;
         }
     }
     
     class Department {
         String name;
         Professor[] professors;
         int count = 0;
     
         Department(String name, int n) {
             this.name = name;
             professors = new Professor[n];
         }
     
         void addProfessor(Professor p) {
             professors[count++] = p;
         }
     
         void showProfessors() {
             System.out.println("Department: " + name);
             if (count == 0) {
                 System.out.println("No professors assigned.");
             } else {
                 for (int i = 0; i < count; i++) {
                     System.out.println("- " + professors[i].name);
                 }
             }
         }
     }
     
     public class Main {
         public static void main(String[] args) {
             Scanner sc = new Scanner(System.in);
             int n = sc.nextInt();
             sc.nextLine(); 
     
             Professor[] profs = new Professor[n];
             for (int i = 0; i < n; i++) {
                 if (sc.hasNextLine()) {
                     profs[i] = new Professor(sc.nextLine());
                 }
             }
     
             String deptName = "Computer Science";
             if (sc.hasNextLine()) {
                 deptName = sc.nextLine().replace("Department: ", "");
             }
     
             Department dept = new Department(deptName, n);
             for (Professor p : profs) {
                 dept.addProfessor(p);
             }
     
             dept.showProfessors();
             sc.close();
         }
     }
     
     




## OUTPUT:
<img width="1032" height="361" alt="image" src="https://github.com/user-attachments/assets/31ee66b2-1762-42e3-b224-73dac803348e" />



## RESULT:
Therefore the program successfully demonstrates aggregation by associating independent Professor objects with a Department.



# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a class that uses a constructor to initialize variables and overrides toString() method.

## AIM:
To write a class that uses a constructor to initialize variables and overrides toString() method.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define a class student with attributes name (String) and id (int).
4.	Create a constructor student(String name, int id) to initialize the student’s name and id using this keyword.
5.	Override the toString() method to return the student details in string format.
6.	Create the main class bunk containing the main method.
7.	Create a Scanner object to read the student name and id from the user.
8.	Create a student object s1 by passing the name and id to the constructor.
9.	Print the student object s1, which automatically calls the toString() method.
10.	Stop the program.
    





## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: VESHWANTH. 
RegisterNumber:  212224230300
*/
```

## SOURCE CODE:
    import java.util.*;
    class student{
        String name;
        int id;
    
        student(String name,int id){
            this.name=name;
            this.id=id;
        } 
        public String toString(){
           return "Student{name='" + name + "', age=" + id + "}";
        }
    }
    public class bunk{
        public static void main(String[] args){
            Scanner sc=new Scanner(System.in);
            String name=sc.nextLine();
            int id=sc.nextInt();
            student s1=new student(name,id);
            System.out.println(s1);
        }
    }






## OUTPUT:
<img width="1286" height="420" alt="image" src="https://github.com/user-attachments/assets/e4979cb3-d475-49b7-884f-7e3fc298284c" />



## RESULT:
Thus, the program successfully creates a student object using a constructor, reads the name and id from the user, and displays the student details using the overridden toString() method.

# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class Car with attributes brand, model, year. Create 2 objects and print their details.

## AIM:
To create a class Car with attributes brand, model, year. Create 2 objects and print their details.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class Car with attributes brand, model, and year.
4.	In the main method, create the first object car1 of class Car and assign values to its attributes.
5.	Create another object car2 of class Car and assign values to its attributes.
6.	Display the details of car1 and car2 using System.out.println().
7.	End the program.





## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: VESHWANTH.
RegisterNumber: 212224230300
*/
```

## SOURCE CODE:
    import java.util.*;
    class Car{
        String brand;
        String model;
        int year;
    }
    public class main {
        public static void main(String[] args) {
            Car car1 = new Car();
            car1.brand = "Toyota";
            car1.model = "Innova";
            car1.year = 2022;
    
            Car car2 = new Car();
            car2.brand = "Hyundai";
            car2.model = "i20";
            car2.year = 2021;
    
            System.out.println("Car 1: " + car1.brand + " " + car1.model + " " + car1.year);
            System.out.println("Car 2: " + car2.brand + " " + car2.model + " " + car2.year);
        }
    }
    
    





## OUTPUT:
<img width="1267" height="276" alt="image" src="https://github.com/user-attachments/assets/7ef9a9d1-458a-4a70-b4ae-594a9ac4a02c" />



## RESULT:
Therefore,The program successfully creates two Car objects and assigns values to their attributes (brand, model, and year). It then displays the details of both cars on the screen.

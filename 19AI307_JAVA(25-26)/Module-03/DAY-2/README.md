# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program that calculates the area of different shapes using method overloading. Create a class AreaCalculator with:
- area(int side) for square
- area(int length, int breadth) for rectangle
- area(double radius) for circle
## AIM:
To write a Java program that calculates the area of different shapes using method overloading. Create a class AreaCalculator.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'.
3.	Create a Scanner object to read input values from the user.
4.	Read the side of the square, create an object of the calculator class, and calculate the area of the square using the area() method.
5.	Read the length and breadth of the rectangle and calculate the area of the rectangle using the rectangle() method.
6.	Read the radius of the circle and calculate the area of the circle using the area1() method.
7.	Display all calculated areas (square, rectangle, and circle) and end the program.





## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: VESHWANTH.
RegisterNumber:  212224230300
*/
```

## SOURCE CODE:

    import java.util.*;
    class calculator{
        
        public int area(int side){
            return side*side;
        }
        
        public int rectangle(int length,int breadth){
            return length*breadth;
        }
        
        public double area1(double radius){
            return Math.PI*radius*radius;
        }
    }
    class prog{
        public static void main(String[] args){
            Scanner sc=new Scanner(System.in);
            int square=sc.nextInt();
            calculator c=new calculator();
            System.out.println("Area of square: " + c.area(square));
            int len=sc.nextInt();
            int breadth=sc.nextInt();
            System.out.println("Area of rectangle: " + c.rectangle(len, breadth));
            double radical=sc.nextDouble();
            System.out.println("Area of circle: " + c.area1(radical));
        }
    }
    
    
    


## OUTPUT:

<img width="1290" height="503" alt="image" src="https://github.com/user-attachments/assets/fc197efa-d15d-4704-b654-3ea054e9a445" />


## RESULT:
Thus,the given program for simple calculation using polymorphism method is successfully implemented.

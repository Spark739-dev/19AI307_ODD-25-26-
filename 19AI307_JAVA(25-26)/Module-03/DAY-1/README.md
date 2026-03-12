# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
Create a Super class Vehicle with fields brand (String) and speed (int). Create a subclass Car that inherits from Vehicle and adds a field fuelType (String).

Implement a method in Car called displayInfo() that prints the vehicle's brand, speed, and fuel type.

Write a program that:

- Takes input for brand, speed, and fuel type using Scanner.
- Creates a Car object.
- Calls displayInfo() to print the details.

## AIM:
To Create a Super class Vehicle with fields brand (String) and speed (int). Create a subclass Car that inherits from Vehicle and adds a field fuelType (String) and to implement a method in Car called displayInfo() that prints the vehicle's brand, speed, and fuel type.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a base class vehicle with attributes brand (String) and speed (int).
4.	Create a subclass car that extends the vehicle class.
5.	Add an attribute fueltype in the car class.
6.	Define a method display() in the car class to print the vehicle details.
7.	Use the super keyword to access the inherited variables brand and speed.
8.	Create the main class main containing the main() method.
9.	Create a Scanner object to read input from the user.
10.	Create an object c of the car class.
11.	Read the brand, speed, and fuel type from the user and store them in the object.
12.	Call the display() method to print the brand, speed, and fuel type.
13.	End the program.





## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: VESHWANTH.
RegisterNumber:  212224230300
*/
```

## SOURCE CODE:

    import java.util.*;
    class vehicle{
        String brand;
        int speed;
        
    }
    
    class car extends vehicle{
        String fueltype;
        
        void display(){
            System.out.println("Brand: "+super.brand);
            System.out.println("Speed: "+super.speed+" km/h");
            System.out.println("Fuel Type: "+fueltype);
        }
    }
    public class main{
        public static void main(String[] args){
            Scanner sc=new Scanner(System.in);
            car c=new car();
            c.brand=sc.nextLine();
            c.speed=sc.nextInt();
            sc.nextLine();
            c.fueltype=sc.nextLine();
            c.display();
        }
    }
    
    



## OUTPUT:
<img width="1291" height="483" alt="image" src="https://github.com/user-attachments/assets/a5be5482-c041-4a7a-b464-7cdfdcd40c20" />



## RESULT:
Thus, the program successfully demonstrates inheritance in Java, where the car class inherits properties from the vehicle class and displays the brand, speed, and fuel type entered by the user.

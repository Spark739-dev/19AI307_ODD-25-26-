# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called Smartphone with private instance variables brand, model, and storageCapacity. Provide public getter and setter methods to access and modify these variables. Add a method called increaseStorage() that takes an integer value and increases the storageCapacity by that value.

## AIM:
To write a Java program to create a class called Smartphone with private instance variables brand, model, and storageCapacity. Provide public getter and setter methods to access and modify these variables. Add a method called increaseStorage() that takes an integer value and increases the storageCapacity by that value.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class Smartphone with private attributes: brand, model, and storageCapacity.
4.	Define getter methods to return the values of brand, model, and storageCapacity.
5.	Define setter methods to assign values to brand, model, and storageCapacity.
6.	Create a method increaseStorage(value) to increase the storage capacity if the given value is greater than 0.
7.	Create a method display() to print the smartphone details (brand, model, and updated storage capacity).
8.	In the main method, create a Scanner object to read user input.
9.	Create an object phone of the Smartphone class.
10.	Read the brand, model, storage capacity, and additional storage value, then set them using setter methods and call increaseStorage(value).
11.	Call the display() method to print the updated smartphone details and stop the program.





## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: VESHWANTH.
RegisterNumber: 212224230300 
*/
```

## SOURCE CODE:
    import java.util.Scanner;
    
    class Smartphone {
        private String brand;
        private String model;
        private int storageCapacity;
    
        
        public String getBrand() {
            return brand;
        }
    
        public String getModel() {
            return model;
        }
    
        public int getStorageCapacity() {
            return storageCapacity;
        }
    
        
        public void setBrand(String brand) {
            this.brand = brand;
        }
    
        public void setModel(String model) {
            this.model = model;
        }
    
        public void setStorageCapacity(int storageCapacity) {
            this.storageCapacity = storageCapacity;
        }
    
       
        public void increaseStorage(int value) {
            if (value > 0) {
                this.storageCapacity += value;
            }
        }
    
        
        public void display() {
            System.out.println("Brand: " + brand);
            System.out.println("Model: " + model);
            System.out.println("Updated Storage Capacity: " + storageCapacity + " GB");
            System.out.println("------------------------------");
        }
    }
    public class main{
        public static void main(String[] args){
            Scanner sc=new Scanner(System.in);
            Smartphone phone=new Smartphone();
            String brand=sc.nextLine();
            String model=sc.nextLine();
            int storage=sc.nextInt();
            int value=sc.nextInt();
            phone.setBrand(brand);
            phone.setModel(model);
            phone.setStorageCapacity(storage);
            phone.increaseStorage(value);
            phone.display();
        }
    }
    
       
    





## OUTPUT:

<img width="1264" height="553" alt="image" src="https://github.com/user-attachments/assets/003b630f-130f-4202-aa9f-f4e65dd9674c" />


## RESULT:
Thus, the program successfully creates a Smartphone object, reads the brand, model, and storage capacity, increases the storage using a method, and displays the updated smartphone details.

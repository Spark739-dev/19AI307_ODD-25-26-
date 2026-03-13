# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Design a program where a Product model stores item info, and the view displays it. Implement a controller to update product price and refresh the view automatically.



## AIM:
To Design a program where a Product model stores item info, and the view displays it. Implement a controller to update product price and refresh the view automatically.


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'.
3.	Create a Product class (Model) with attributes: name, price, and code.
4.	Define a constructor in the Product class to initialize the product details.
5.	Create getter methods (getName(), getPrice(), getCode()) to access product information.
6.	Create a setter method setPrice() to update the product price.
7.	Create a ProductView class (View) to display product details on the screen.
8.	Create a ProductController class (Controller) that connects the Product and ProductView.
9.	In the main method, read product name, price, code, and new price from the user using Scanner.
10.	Create objects for Product, ProductView, and ProductController, and display the original product details using updateView().
11.	Update the product price using updatePrice(newPrice) and display the updated product details, then end the program.





## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: VESHWANTH.
RegisterNumber:  212224230300
*/
```

## SOURCE CODE:

    import java.util.Scanner;
    
    public class ProductManagementSystem {
    
        // ===== Model =====
        static class Product {
            private String name;
            private double price;
            private String code;
    
            // Constructor
            public Product(String name, double price, String code) {
                this.name = name;
                this.price = price;
                this.code = code;
            }
    
            // Getter for name
            public String getName() {
                return name;
            }
    
            // Getter for price
            public double getPrice() {
                return price;
            }
    
            // Getter for code
            public String getCode() {
                return code;
            }
    
            // Setter for price
            public void setPrice(double price) {
                this.price = price;
            }
        }
    
        // ===== View =====
        static class ProductView {
            public void displayProduct(String name, double price, String code) {
                System.out.println("--- Product Details ---");
                System.out.println("Name : " + name);
                System.out.println("Price: " + price);
                System.out.println("Code : " + code);
            }
        }
    
        // ===== Controller =====
        static class ProductController {
            private Product product;
            private ProductView view;
    
            // Constructor
            public ProductController(Product product, ProductView view) {
                this.product = product;
                this.view = view;
            }
    
            // Update view
            public void updateView() {
                view.displayProduct(
                    product.getName(),
                    product.getPrice(),
                    product.getCode()
                );
            }
    
            // Update price and refresh view
            public void updatePrice(double newPrice) {
                product.setPrice(newPrice);
                updateView();
            }
        }
    
        // ===== Main Method =====
        public static void main(String[] args) {
            Scanner sc = new Scanner(System.in);
    
            // Input
            String name = sc.nextLine();
            double price = sc.nextDouble();
            sc.nextLine(); // consume newline
            String code = sc.nextLine();
            double newPrice = sc.nextDouble();
    
            // Create objects
            Product product = new Product(name, price, code);
            ProductView view = new ProductView();
            ProductController controller = new ProductController(product, view);
    
            // Display original details
            controller.updateView();
    
            // Update price and display again
            controller.updatePrice(newPrice);
    
            sc.close();
        }
    }






## OUTPUT:
<img width="1290" height="426" alt="image" src="https://github.com/user-attachments/assets/7cb4fe72-99bd-46b3-b7b8-2be97738a799" />



## RESULT:
The program successfully implemented a behavioral design pattern using MVC, where the controller updates product price and automatically refreshes the view.

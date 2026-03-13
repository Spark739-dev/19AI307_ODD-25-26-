# Ex.No:3(D)    INTERFACE 

## QUESTION:
Two types of traffic controllers decide whether a vehicle can pass based on signal color. The decision logic varies by controller.

AggressiveController: Allows only if "GREEN".

DefensiveController: Allows for "GREEN" or "YELLOW".

 Input Format:

signalColor
controllerType
signalColor: A string indicating the signal color (GREEN, YELLOW, RED)

controllerType: An integer (1 for AggressiveController, 2 for DefensiveController)

 Output Format:

Print "GO"       → if vehicle is allowed to move  
Print "STOP"     → if vehicle must stop

## AIM:
To develop a Java program using abstraction and method overriding to simulate two types of traffic controllers (AggressiveController and DefensiveController) that determine whether a vehicle can move or stop based on the given signal color and controller type, and display the result as "GO" or "STOP".

## ALGORITHM :
1.	Start the program.
2.	Import the java.util package to use the Scanner class for input.
3. Create an interface TrafficController with a method decide(String signalColor).
4. Create a class AggressiveController that implements TrafficController.
5. In AggressiveController, implement the decide() method to print "GO" if the signal color is GREEN, otherwise print "STOP".
6. Create another class DefensiveController that implements TrafficController.
7. In DefensiveController, implement the decide() method to print "GO" if the signal color is GREEN or YELLOW, otherwise print "STOP".
8. In the main method, create a Scanner object and read the input containing signal color and controller type.
9. Based on the controller type, create either an AggressiveController or DefensiveController object using the TrafficController reference.
10. Call the decide() method with the signal color to display "GO" or "STOP", then end the program.
	





## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: VESHWANTH.
RegisterNumber:  212224230300
*/
```

## SOURCE CODE:
    import java.util.*;
    
    interface TrafficController {
        void decide(String signalColor);
    }
    
    class AggressiveController implements TrafficController {
        public void decide(String signalColor) {
            if (signalColor.equalsIgnoreCase("GREEN")) {
                System.out.println("GO");
            } else {
                System.out.println("STOP");
            }
        }
    }
    
    class DefensiveController implements TrafficController {
        public void decide(String signalColor) {
            if (signalColor.equalsIgnoreCase("GREEN") || signalColor.equalsIgnoreCase("YELLOW")) {
                System.out.println("GO");
            } else {
                System.out.println("STOP");
            }
        }
    }
    
    public class Main {
        public static void main(String[] args) {
            Scanner sc = new Scanner(System.in);
    
           
            String line = sc.nextLine().trim();
            String[] parts = line.split("\\s+");
    
            String signalColor = parts[0];
            int controllerType = Integer.parseInt(parts[1]);
    
            TrafficController controller;
    
            if (controllerType == 1) {
                controller = new AggressiveController();
            } else {
                controller = new DefensiveController();
            }
    
            controller.decide(signalColor);
        }
    }
    
    





## OUTPUT:
<img width="1301" height="304" alt="image" src="https://github.com/user-attachments/assets/eeba5290-2fcd-4a1a-bdd6-d22e6e0433d9" />



## RESULT:
The program was executed successfully. It reads the signal color and controller type, creates the appropriate controller (AggressiveController or DefensiveController), evaluates the signal condition, and displays "GO" if the vehicle is allowed to move or "STOP" if the vehicle must stop.

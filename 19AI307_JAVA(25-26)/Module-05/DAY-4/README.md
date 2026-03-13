# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for set the priority and name of the current thread.

Note : Read the threadname from the User

Set the Priority as 2.

## AIM:
To write a Java program to set the name and priority of the current thread, where the thread name is read from the user and the priority is set to 2.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'.
3.	Create a class mythread that extends the Thread class.
4.	Define a constructor that accepts the thread name and priority, sets the thread name using super(name), and sets the priority using setPriority(p).
5.	Override the run() method to display the thread priority, thread name, and the current thread details.
6.	In the main method, create a Scanner object to read the thread name from the user.
7.	Create an object of mythread with the entered thread name and set the priority as 2, then start the thread using start().
8.	xecute the thread, print the thread information, and end the program.





## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: VESHWANTH.
RegisterNumber:  212224230300
*/
```

## SOURCE CODE:
    import java.util.*;
    class mythread extends Thread{
        mythread(String name,int p){
            super(name);
            setPriority(p);
        }
        public void run(){
            System.out.println("Priority of Thread: "+getPriority());
            System.out.println("Name of Thread: "+getName());
            System.out.println(Thread.currentThread());
        }
    }
    
    class prog{
        public static void main(String[] args){
            Scanner sc=new Scanner(System.in);
            String s=sc.nextLine();
            mythread t=new mythread(s,2);
            t.start();
            
        }
    }
    





## OUTPUT:

<img width="1289" height="343" alt="image" src="https://github.com/user-attachments/assets/5b008077-d52b-4830-9cb7-1b5a970b4012" />


## RESULT:
The program successfully reads the thread name from the user, creates a thread with the given name, sets its priority to 2, and displays the thread name, priority, and current thread details on the console.

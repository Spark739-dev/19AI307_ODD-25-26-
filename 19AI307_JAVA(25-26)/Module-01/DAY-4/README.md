# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java program to find the index of a given element in an array

## AIM:
To write a Java program that reads an array of integers and finds the index of a given element within the array.

## ALGORITHM :
1.	Start the program and read the size of the array n.
2.	Read n integer elements and store them in the array a[ ].
3.	Read the element x whose index needs to be found.
4.	Traverse the array from index 0 to n-1:
   
              If a[i] == x, print the index i and terminate the program.
5. .If the loop finishes without a match, print "Element not found".
6. End the program.




## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: VESHWANTH.
RegisterNumber: 212224230300
*/
```

## SOURCE CODE:

    import java.util.*;
    public class main{
        public static void main(String[] args){
            Scanner sc=new Scanner(System.in);
            int num = sc.nextInt();
            int arr[]=new int[num];
            for(int i=0;i<num;i++){
                arr[i]=sc.nextInt();
            }
            int key=sc.nextInt();
            int index=-1;
            for(int i=0;i<num;i++){
                if(arr[i]==key){
                    index=i;
                    break;
                }
            }
            if(index==-1){
                System.out.println("Element not found");
            } else{
                System.out.println(index); 
            }
        }
    }





## OUTPUT:
<img width="1237" height="613" alt="image" src="https://github.com/user-attachments/assets/a275f852-4e8b-4690-822f-7304ffeb7961" />



## RESULT:
Therefore the program successfully searches the array for the given element.

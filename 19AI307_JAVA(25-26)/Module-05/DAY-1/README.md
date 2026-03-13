# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a Java program to write characters to a file using FileWriter.

## AIM:
o write character data into a file using the FileWriter class in Java.

## ALGORITHM :
1.	Start the program.
2. Import java.io.FileWriter and java.io.IOException.
3. Take user input using Scanner.
4. Create a FileWriter object with the desired file name.
5. Use write() method to write text into the file.
6. Close the FileWriter and handle exceptions using try-catch.
	





## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: VESHWANTH.
RegisterNumber:  212224230300
*/
```

## SOURCE CODE:
    import java.io.*;
    
    public class FileWriteExample {
        public static void main(String[] args) {
            try {
                BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
                String filename = br.readLine();
                String content = br.readLine();
    
                FileWriter fw = new FileWriter(filename);
                fw.write(content);
                fw.close();
    
                System.out.println("File written successfully.");
            } catch (IOException e) {
                System.out.println("An error occurred.");
            }
        }
    }
    




## OUTPUT:
<img width="1259" height="399" alt="image" src="https://github.com/user-attachments/assets/99882ab3-d427-4991-9633-ee4ffc3faab1" />



## RESULT:
The program successfully writes the entered text into output.txt using FileWriter.

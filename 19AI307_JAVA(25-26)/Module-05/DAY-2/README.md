# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a Java program to serialize a collection of objects (like ArrayList<Student>) into a file.

## AIM:
To write a Java program that demonstrates object serialization and deserialization, where multiple Student objects entered by the user are stored in a file and later retrieved and displayed.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3. Create a Student class that implements Serializable with attributes id, name, and marks.
4. Define a constructor in the Student class to initialize the student details.
5. Override the toString() method to display student information in a readable format.
6. Create the method serializeStudents() to write the list of student objects into a file using ObjectOutputStream.
7. Create the method deserializeStudents() to read the list of student objects from the file using ObjectInputStream.
8. In the main method, create a Scanner object and an empty ArrayList to store student objects.
9. Read the number of students n, then input each student’s id, name, and marks, and add them to the list.
10. Serialize the student list into the file "students.dat" and then deserialize the data from the same file.
11. Display the deserialized student details using a loop and end the program.	





## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: VESHWANTH.
RegisterNumber:  212224230300
*/
```

## SOURCE CODE:
    import java.io.*;
    import java.util.*;
    
    // Student class must implement Serializable
    class Student implements Serializable {
        private static final long serialVersionUID = 1L;
    
        private int id;
        private String name;
        private double marks;
    
        public Student(int id, String name, double marks) {
            this.id = id;
            this.name = name;
            this.marks = marks;
        }
    
        @Override
        public String toString() {
            return "Student{id=" + id + ", name='" + name + "', marks=" + marks + "}";
        }
    }
    
    public class StudentSerializationUserInput {
    
        // Serialize list of students
        public static void serializeStudents(List<Student> students, String fileName) {
            try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream(fileName))) {
                oos.writeObject(students);
                System.out.println("Students serialized successfully into: " + fileName);
            } catch (IOException e) {
                System.out.println("Error during serialization: " + e.getMessage());
            }
        }
    
        // Deserialize list of students
        @SuppressWarnings("unchecked")
        public static List<Student> deserializeStudents(String fileName) {
            List<Student> students = null;
            try (ObjectInputStream ois = new ObjectInputStream(new FileInputStream(fileName))) {
                students = (List<Student>) ois.readObject();
                System.out.println("Students deserialized successfully from: " + fileName);
            } catch (IOException | ClassNotFoundException e) {
                System.out.println("Error during deserialization: " + e.getMessage());
            }
            return students;
        }
    
        public static void main(String[] args) {
            Scanner scanner = new Scanner(System.in);
            List<Student> students = new ArrayList<>();
    
            int n = scanner.nextInt();
            scanner.nextLine(); // consume newline
            String f="students.dat";
            for(int i=0;i<n;i++){
                int id=scanner.nextInt();
                scanner.nextLine();
                String name=scanner.nextLine();
                double marks =scanner.nextDouble();
                students.add(new Student(id,name,marks));
            }
            serializeStudents(students,f);
            
            List<Student> deserializedStudents = deserializeStudents(f);
            
            
    
            // Display deserialized data
            if (deserializedStudents != null) {
                System.out.println("\nDeserialized Students:");
                for (Student s : deserializedStudents) {
                    System.out.println(s);
                }
            }
    
            scanner.close();
        }
    }
    
    





## OUTPUT:
<img width="1225" height="907" alt="image" src="https://github.com/user-attachments/assets/f245767f-375f-42bf-9ff3-1fa2888453fa" />



## RESULT:
The program successfully serializes a list of Student objects into a file named students.dat and then deserializes the data back into a list. It correctly displays all the retrieved student information, proving that object serialization and deserialization work as expected.

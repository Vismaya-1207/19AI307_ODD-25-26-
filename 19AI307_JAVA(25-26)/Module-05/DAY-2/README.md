# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a Java program to serialize a collection of objects (like ArrayList<Student>) into a file.

## AIM:
To serialize a collection of objects (e.g., ArrayList<Student>) into a file using Java object serialization.

## ALGORITHM :
1.Start the program.

2.Create a Student class that implements Serializable.

3.Create an ArrayList to store multiple Student objects.

4.Add student objects to the list.

5.Create a FileOutputStream to connect to a file.

6.Wrap it with ObjectOutputStream.

7.Write the ArrayList object into the file using writeObject().

8.Close the stream.

9.Display success message.

10.End the program.




## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: VISMAYA V
RegisterNumber: 212224060310 
*/
```

## SOURCE CODE:
```
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
        // Write your code here
        for(int i=0;i<n;i++)
        {
            int id=scanner.nextInt();
            scanner.nextLine();
            String name=scanner.nextLine();
            double marks=scanner.nextDouble();
            scanner.nextLine();
            students.add(new Student(id,name,marks));
        }
        String fileName="students.dat";
        serializeStudents(students,fileName);
        List<Student>deserializedStudents=deserializeStudents(fileName);

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

```
## OUTPUT:
<img width="1294" height="550" alt="image" src="https://github.com/user-attachments/assets/fb184cbd-6f86-40d6-9f29-639737f6908d" />



## RESULT:
Therefore,the program was executed successfully.

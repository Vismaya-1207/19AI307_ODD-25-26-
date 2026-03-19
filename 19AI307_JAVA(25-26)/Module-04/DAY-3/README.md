# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
A student can enroll in multiple courses. The relationship is many-to-many via association.
If No Courses were assigned, print "No courses enrolled." 

## AIM:
To demonstrate association (many-to-many relationship) between Student and Course classes and display enrolled courses.

## ALGORITHM :
1.Start the program.

2.Create class Course with course name.

3.Create class Student with a list of courses.

4.Read student name from user.

5.Read number of courses.

6.For each course:

Create a Course object.

Enroll the student in the course.

7.Display student’s courses:

If no courses, print "No courses enrolled."

8.Else, print all course names.

9.Stop the program.




## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by:VISMAYA.V 
RegisterNumber: 212224060310 
*/
```

## SOURCE CODE:
```
import java.util.*;

public class AssociationExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String studentName = sc.nextLine();
        Student student = new Student(studentName);

        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String course = sc.nextLine();
            student.enroll(new Course(course));
        }

        student.showCourses();
        sc.close();
    }
}


class Course {
    private String name;

    public Course(String name) {
        this.name = name;
    }

    public String getCourseName() {
        return name;
    }
}

class Student {

    private List<Course> ob=new ArrayList<>();
    String name;
    public Student(String name) {
        this.name=name;
    }

    public void enroll(Course c) {
        
        ob.add(c);
    }

    public void showCourses() {
        System.out.println(name+"'s enrolled courses:");
        if(ob.isEmpty())
        {
           System.out.print("No courses enrolled." );
           return;
        }
        
        for(Course x:ob)
        {
            System.out.println("- "+x.getCourseName());
        }
        
    }
}

```






## OUTPUT:
<img width="1272" height="396" alt="image" src="https://github.com/user-attachments/assets/c389a134-b9f2-41d7-9afd-64c548ab56da" />



## RESULT:
Therefore,the program was executed successfully.

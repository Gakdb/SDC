# 📘 Java JDBC CRUD Operations — experiment5

This project showcases basic Java JDBC operations (Insert, Display, Update, Delete) on a `student` table using MySQL. Each file below includes line-by-line explanations in comments to help beginners understand the logic clearly.

---
---downloading jar file ![Alt Text](images/your-screenshot.png)



## 🛠 Prerequisites

- MySQL installed with database: `mydb` and table: `student(s_id INT, s_name VARCHAR, s_address VARCHAR)`
- Java JDK
- JDBC driver configured
- IDE or terminal

---

## 📂 Files and Code Explanations

---

### 🔹 InsertData.java — Add a new student

```java
import java.sql.*;
import java.util.Scanner;

public class InsertData {
    public static void main(String[] args) {
        try (
            // Step 1: Connect to the database
            Connection con = DriverManager.getConnection("jdbc:mysql://localhost/mydb", "root", "ace123101");
            // Step 2: Create a statement object
            Statement t = con.createStatement()
        ) {
            // Step 3: Read input from user
            Scanner sc = new Scanner(System.in);
            System.out.println("Inserting Data into student table:");
            System.out.println("________________________________________");

            System.out.print("Enter student id: ");
            int sid = sc.nextInt();

            System.out.print("Enter student name: ");
            String sname = sc.next();

            System.out.print("Enter student address: ");
            String saddr = sc.next();

            // Step 4: Prepare SQL query string
            String insertQuery = "INSERT INTO student VALUES(" + sid + ",'" + sname + "','" + saddr + "')";

            // Step 5: Execute insert query
            t.executeUpdate(insertQuery);

            System.out.println("Data inserted successfully into student table");

        } catch (SQLException err) {
            // Exception handling for SQL errors
            System.out.println("ERROR: " + err);
        }
    }
}

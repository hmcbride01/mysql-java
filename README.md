
# MySQL-Java Project

## Project Description
This project demonstrates the integration of MySQL and Java to design and manage relational databases. It showcases best practices for creating and maintaining tables, defining relationships, and ensuring data integrity within a Java application. The project includes features such as table creation, foreign keys, indexing, and handling complex relationships (e.g., one-to-many, many-to-many). By leveraging Java's JDBC (Java Database Connectivity), the project offers hands-on examples of database design principles in action, facilitating smoother application development and data management.

### Key Features:
- Creation of robust tables and relationships directly integrated into Java applications.
- Implementation of data constraints to ensure data validity and consistency.
- Execution of complex queries through Java for meaningful data retrieval.
- Database optimization using indexing techniques.
- Real-world examples of many-to-many relationships implemented programmatically via join tables.

## Technologies Used
- **Database Management System**: MySQL  
- **Programming Language**: Java  
- **Libraries/Tools**: JDBC, MySQL Workbench, ERD tools for database design.  

## Highlighted Features
1. **Complex Relationships Management**  
   This project handles many-to-many relationships using join tables within a Java application, ensuring data integrity and seamless querying.  
   _Challenge:_ Understanding and implementing join tables programmatically for scalable solutions.  
   _Solution:_ Use of Java's JDBC API to dynamically manage relationships and enforce constraints.  

2. **Data Validation with Constraints**  
   Key constraints (e.g., primary keys, foreign keys) and validation rules are applied to maintain data consistency.  
   _Challenge:_ Aligning constraints with both database and application requirements.  
   _Solution:_ Rigorous testing through Java-driven database interactions.

## Code Snippets
### Example: Creating a Many-to-Many Relationship in Java
```java
// Establishing connection to MySQL
Connection connection = DriverManager.getConnection("jdbc:mysql://localhost:3306/your_database", "username", "password");

// Creating Students table
String createStudentsTable = "CREATE TABLE Students (" +
    "student_id INT AUTO_INCREMENT PRIMARY KEY," +
    "name VARCHAR(100) NOT NULL)";
connection.createStatement().execute(createStudentsTable);

// Creating Courses table
String createCoursesTable = "CREATE TABLE Courses (" +
    "course_id INT AUTO_INCREMENT PRIMARY KEY," +
    "title VARCHAR(100) NOT NULL)";
connection.createStatement().execute(createCoursesTable);

// Creating Join table for Student-Courses
String createJoinTable = "CREATE TABLE StudentCourses (" +
    "student_id INT," +
    "course_id INT," +
    "PRIMARY KEY (student_id, course_id)," +
    "FOREIGN KEY (student_id) REFERENCES Students(student_id)," +
    "FOREIGN KEY (course_id) REFERENCES Courses(course_id))";
connection.createStatement().execute(createJoinTable);
```

## Installation & Usage Instructions
 **Prerequisites**:
   - Install MySQL and MySQL Workbench.
   - Install Java Development Kit (JDK) and set up your development environment (e.g., IntelliJ IDEA, Eclipse).
   - Add the MySQL Connector/J library to your project.


## Contact Information
For collaboration or questions, feel free to reach out:  
- **Email**: [h.mcbride6979@gmail.com](mailto:h.mcbride6979@gmail.com)  
- **GitHub**: [hmcbride01](https://github.com/hmcbride01)  
- **LinkedIn**: [Heather McBride](https://www.linkedin.com/in/heather-mcbride-323ab725/)


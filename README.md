# Data-Modelling-Assignment
Github repository for Data modelling assignment  


### Question 1: Design a data model for a simple e-commerce system (duration: 1.5-2 hours).  
Instructions:  
Identify the entities in an e-commerce system, including products, categories, customers, and orders.  
Determine the attributes for each entity, such as product name, price, customer name, order date, etc.  
Identify the relationships between entities, such as a product can belong to multiple categories and a customer can place multiple orders.  
Determine the primary keys for each entity, such as product ID for products, customer ID for customers, etc.  
Create an ER diagram to visually represent the data model.  
Write a brief description of the data model, including its purpose, entities, relationships, and any assumptions or constraints.  

### Solution:  

### ER Diagram:  
![image](https://user-images.githubusercontent.com/122514456/224827939-a8fcc449-c2e4-4713-a8c5-80714ae70af0.png)


### Description:  

This data model represents a simple e-commerce system that sells products to customers. The system contains four entities: products, categories,   customers, and orders. Products have attributes such as product id, name, description, price, and image. Categories have attributes such as name and   category id. Customers have attributes such as customer id, name, email, phone number, and address. Orders have attributes such as order id, order date,   total price, quantity.  

### Purpose:  

The purpose of the above ER model is to provide a data model for a simple e-commerce system. The model describes the various entities, attributes, and   relationships that exist within the system. The entities in the model include products, categories, customers, and orders.  

Overall, the purpose of the ER model is to provide a clear and structured representation of the data that is required to build and operate an  
e-commerce system. It serves as a blueprint for the design and development of the system, ensuring that all necessary data is captured and stored   appropriately.   

### Entities:  

Products: A product that can be sold on the e-commerce system.   
Categories: A category that a product can belong to.  
Customers: A customer who can place orders on the e-commerce system.  

Orders: A record of an order placed by a customer that contains information about the products, quantities, and total price.  

### Attributes:  

Products: ID, name, description, price, image.   
Categories: ID, name.  
Customers: ID, name, email, phone number, address.   
Orders: ID, order date, total price, quantity.    
### Relationships:  

A product can belong to multiple categories and a category can have multiple products (many-to-many).    
A customer can place multiple orders, but an order can only be placed by one customer (one-to-many).    
An order can contain multiple products and a product can be in multiple orders (many-to-many).    

The ER diagram visually represents the relationships between the entities, with arrows indicating the direction of the relationships. The ‘Contains’ is a  junction that allows for a many-to-many relationship between orders and products. The ‘Belongs to’ is a junction that allows for a many-to-many   relationship between categories and products. The ‘Places’ is a junction that allows for a many-to-many relationship between orders and customers.  

### Assumptions:  

The data model assumes that each product can belong to multiple categories, each customer can place multiple orders, and each order can contain multiple   products. The primary keys for each entity are ID for products, categories, and customers, and ID for orders.  

### Constraints:  
 
### Primary Keys (Entity Integrity)    
Products: product ID   
Categories: category ID   
Customers: customer ID  
Orders: order ID  

### Foreign Keys (Referential Integrity)  

Belongs to (Intersection Table between Products and Categories): Composite Key (Product ID, Category ID)  
Contains(Intersection Table between Products and Orders): Composite Key (Product ID, Order ID)  
Places(Relationship between Customers and Orders): Foreign Key (Customer ID migrates from Customer table to Order table)   


### Question 2: Design a data model for a student enrollment system (duration: 1.5-2 hours).  
Instructions:  
Identify the entities in a student enrollment system, including students, courses, and enrollments.  
Determine the attributes for each entity, such as student name, course name, enrollment date, etc.  
Identify the relationships between entities, such as a student can enroll in multiple courses and a course can have multiple students.  
Determine the primary keys for each entity, such as student ID for students, course ID for courses, etc.  
Create an ER diagram to visually represent the data model.  
Write a brief description of the data model, including its purpose, entities, relationships, and any assumptions or constraints.   

### Solution:  
### ER Diagram:  
![image](https://user-images.githubusercontent.com/122514456/224828814-1edda297-a9b1-4d18-9560-f4cfa7d45c67.png)


### Description:  

The purpose of this data model is to represent a student enrollment system, where students can enroll in multiple courses and courses can have multiple   students. The model consists of two entities: students, courses, and a relationship named enrollments. Students and courses have their own attributes,   such as student_id, gender, name, address, dob, email, phone number and course id, name, course description, start date, end date, instructor, credits   respectively. Enrollments represent the relationship between students and courses and have attributes such as enrollment date. The primary keys are   student ID, course ID.    

### Purpose:    

The purpose of the above data model is to represent a student enrollment system. The model is designed to store and manage information related to    students, courses, and enrollments. It provides a structure for organizing and storing data related to these entities, including their attributes and   relationships. The model can be used to track which courses a student has enrolled in, which students are enrolled in a particular course, when   enrollments were made. The data model can be used by educational institutions, such as schools or universities, to manage student enrollment and course   registration processes. It can also be used to generate reports, analyze enrollment trends, and make informed decisions about course offerings and student  performance.  

### Entities:  
 
Students: This entity represents the students who enroll in courses. Its attributes include student ID, name, email, address, gender, dob and phone   number.  

Courses: This entity represents the courses that students can enroll in. Its attributes may include course ID, name, description, instructor, start date,  end date and credits.  

### Attributes:  
Students: student ID, name, email, address, gender, dob and phone number  

Courses: course ID, name, description, instructor, start end, end date and credit  

### Relationships:  

A student can enroll in multiple courses. A course can have multiple students.  
The ER diagram visually represents the relationships between the entities, with arrows indicating the direction of the relationships. The ‘Enrollments’ is  a junction that allows for a many-to-many relationship between students and courses.    

### Assumptions:  

This data model assumes that a student can enroll in multiple courses and a course can have multiple students. It also assumes that each enrollment is   unique and can be identiﬁed by a composite key referencing student id and course id.  

### Constraints:  

### Primary Keys (Entity Integrity)  

Student: student ID  
Course: course ID  

### Foreign Keys (Referential Integrity)  

Enrollments(Intersection Table between Students and Courses): Composite Key (student ID, course ID)   

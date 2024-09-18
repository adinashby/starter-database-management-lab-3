# Database Management - Lab 3

This template repository is the starter project for Database Management Lab 3. Written in Access.

### Question(s)

### Microsoft Access Lab: Relationship Between Tables

#### Objective:
By the end of this lab, students will understand how to create relationships between tables, the importance of relationships in relational databases, and how to enforce referential integrity.

---

### Part 1: Understanding Table Relationships

In a relational database, tables are connected through relationships. These relationships allow data to be linked across tables, ensuring consistency and minimizing redundancy. The types of relationships are:
- **One-to-One**
- **One-to-Many**
- **Many-to-Many**

For this lab, we will focus on a **One-to-Many** relationship between two tables: **Students** and **Courses**.

---

### Part 2: Preparing the Tables

#### Step 1: Create a New Table for Courses
1. Open your **StudentRecords.accdb** database.
2. Go to **Create** > **Table** to create a new table called **Courses**.
3. In **Design View**, add the following fields:
   - **CourseID** (AutoNumber) – Primary Key
   - **CourseName** (Short Text)
   - **Credits** (Number)
   
4. Save the table as **Courses**.

#### Step 2: Modify the Students Table
1. Open the **Students** table in **Design View**.
2. Add a new field:
   - **CourseID** (Number) – This field will create the link between **Students** and **Courses**.
   
3. Save the **Students** table.

#### Questions:
1. Why do we need to include the **CourseID** field in the **Students** table?
2. What data type should be used for **CourseID** in both tables, and why?

---

### Part 3: Creating a Relationship

#### Step 1: Open the Relationships Window
1. Go to the **Database Tools** tab and click on **Relationships**.
2. In the **Show Table** dialog box, add both the **Students** and **Courses** tables to the window.

#### Step 2: Create a One-to-Many Relationship
1. Click and drag the **CourseID** field from the **Courses** table to the **CourseID** field in the **Students** table.
2. In the **Edit Relationships** dialog, check **Enforce Referential Integrity**.
3. Click **Create** to establish the relationship. You will see a line representing the **One-to-Many** relationship between **Courses** and **Students**.

#### Questions:
1. What is the purpose of enforcing referential integrity in a relationship?
2. What does a **One-to-Many** relationship mean in this context?

---

### Part 4: Testing the Relationship

#### Step 1: Enter Data into Both Tables
1. In **Datasheet View**, enter at least 3 records into the **Courses** table, such as:
   - CourseID: Auto-generated
   - CourseName: Database Design
   - Credits: 3
   - (Add two more courses)

2. Enter data into the **Students** table, ensuring that each student has a valid **CourseID** corresponding to a record in the **Courses** table.

#### Step 2: Run a Query to See Related Data
1. Create a new **Query**.
2. Add both the **Students** and **Courses** tables to the query.
3. Select fields such as **FirstName**, **LastName**, **CourseName**, and **Credits**.
4. Run the query to display the students and their enrolled courses.

#### Questions:
1. What happens if you try to enter a **CourseID** in the **Students** table that doesn't exist in the **Courses** table?
2. How does the query show the relationship between the two tables?

---

### Part 5: Conclusion
- **Discussion**: Summarize how relationships between tables help reduce redundancy and maintain data integrity. Discuss the role of referential integrity and its importance in preventing orphan records and ensuring data consistency across related tables.
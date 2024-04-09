# Dahel_Techies_Online_Clothing_Store_Analysis_Internship
Dahel Consultant and Techies: Sales Analysis; A deep dive into Online Clothing Store Sales data, aimed at extracting valuable  insights to enhance strategic decision-making. I have been hired as a data  analyst for an online clothing store.
(*The picture below is gotten from Robosize Website*). 






![image](https://github.com/RemedyData/Dahel_Techies_Online_Clothing_Store_Analysis_Internship/assets/137626163/820e28f3-7b1d-46c2-97fd-84e7edb51eed)








***Disclaimer:*** This is not a real company as we know this is a dataset compiled by Dahel Consultant Techies for Internship purposes. 


## Introduction

This is an online clothing store performance analysis . It is done by analyzing data from challenge table which was redesigned into three tables namely Customer, Sales and Date tables. 
I used SQL to analyse the entire dataset throughout the project. 



## Problem Statement:

- THE COMPANY IS EXPECTED TO UNDERGO A RAPID EXPANSION IN THE COMING MONTHS AND THEY
 ARE NOT SURE IF THEIR DATABASE CAN HANDLE THE AMOUNT OF TRANSACTIONS THAT WILL COME WITH THE INCREASED NUMBER OF CUSTOMERS.


The goal of this analysis is to:

- YOU HAVE BEEN TASKED TO INVESTIGATE THE CURRENT
 DESIGN OF THE DATABASE. 

- IF THE DESIGN IS FOUND TO BE INEFFICIENT FOR ONLINE TRANSACTION PROCESSING, THEN THE NEED TO REDESIGN THE DATABASE.


## Skills and Concepts Demonstrated:

Data Retrieval:
- SQL queries to retrieve data from one or more database tables based on specified criteria.
- Use of the SELECT statement and its various clauses such as WHERE, ORDER BY, and LIMIT.

Data Filtering and Sorting:
- Filtering data based on specific conditions using the WHERE clause.
- Sorting data using the ORDER BY clause to organize results in ascending or descending order based on specified columns.

Data Aggregation:
- Proficiency in using SQL aggregate functions (e.g., SUM, AVG, COUNT, MAX, MIN) to perform calculations on groups of data.
- Knowledge of the GROUP BY clause to group rows with similar characteristics together for aggregate function calculations.

Data Transformation:
- Ability to manipulate and transform data using SQL functions such as DATE functions, string functions, and mathematical functions.
- Understanding of how to convert data types and format data for analysis.


Subquerying and CTEs:
- Proficiency in using subqueries (nested queries) to filter or aggregate data based on the results of another query.
- Understanding of Common Table Expressions (CTEs) to create temporary result sets for use within a larger query.

Window Functions:
- Ability to utilize window functions to perform calculations across a set of rows related to the current row.
- Skills in ranking data, calculating moving averages, and computing cumulative sums using window functions.

Data Analysis and Interpretation:
- Competency in analyzing SQL query results to derive insights and make data-driven decisions.
- Interpretation of query results in the context of business requirements and objectives.

Optimization and Performance Tuning:
- Knowledge of SQL query optimization techniques to improve query performance, such as indexing, query restructuring, and using appropriate join strategies.

Error Handling and Debugging:
- Skill in identifying and resolving errors in SQL queries, including syntax errors, logic errors, and data-related issues.



   ---





  ## Data Source:
  
The dataset for the work is gotten from Dahel Consultant Techies. It consists of Challenge 1(online  clothing store) table which was redesigned into three tables namely Customer, Sales and Date tables. I studied the dataset well to gain proper insight into the dataset. You can find a link to download the Challenge 1(online  clothing store) dataset [here:](https://docs.google.com/spreadsheets/d/1YAIgqS9nS3RDiX00aoRuEMGXiTw6x8D0QZpmcZJ-Pho/edit?usp=drive_link) 


   

   

   ---





## Data Transformation and Analysis:

   ## Redesign Method: 

   Database Normalization

   To address the inefficiencies of the initial denormalized database, a normalization approach was employed, resulting in the creation of three distinct tables:
   - Customers Table:
    Columns: CustomerID (Primary Key), Name, Surname, transactionid.
   - Sales Table:
    Columns: Transaction ID (Primary Key), CustomerID (Foreign Key), Shipping-State, item, description, retail-price, loyalty-discount.
   - Dates Table:
    Columns: transaction id (Primary Key), Timestamp, Time, Customerid.



  - Furthermore, Several structured queries were written to get the right tables and then saved as views in the Database on PostgreSQL.
    The tables and views are:


   
   Table before splitting
   ![image](https://github.com/RemedyData/Dahel_Techies_Online_Clothing_Store_Analysis_Internship/assets/137626163/2b6cdec7-53af-4e4b-a4bd-a9f235b935f1)

   
   
   
   
   The customer table
   ![image](https://github.com/RemedyData/Dahel_Techies_Online_Clothing_Store_Analysis_Internship/assets/137626163/39bc4956-4ce9-42ba-9860-81715ad51de1)

   
   
   
   
   
   The date table
   ![image](https://github.com/RemedyData/Dahel_Techies_Online_Clothing_Store_Analysis_Internship/assets/137626163/834fa9f2-8b77-4999-b050-0552c1eea3d1)

   
   
   
   
   
   The sales table
   ![image](https://github.com/RemedyData/Dahel_Techies_Online_Clothing_Store_Analysis_Internship/assets/137626163/62c1857b-2664-469e-a17f-7584bb46e04c)






    



---




## Data Model:









## Data Analysis:

Consideration for Normalizing the Online Clothing Store Database:

- The current database design poses challenges with data redundancy, integrity, and scalability.
- Transitioning from a denormalized to a normalized structure is crucial for several reasons:

Data Efficiency:

- Normalization eliminates redundancy, ensuring streamlined data storage and reducing the risk of
inconsistencies.

Enhanced Integrity:
- Establishing relationships between tables improves data integrity, minimizing update, insertion, and
deletion anomalies.

Optimized Query Performance:
- A normalized structure facilitates efficient querying, enhancing overall system performance, crucial for
anticipated growth.

Scalability and Adaptability:
- Normalization provides a scalable framework, accommodating increased data volumes and
adapting to evolving business needs.

Simplified Maintenance:
- Updates and modifications become more straightforward, reducing the risk of errors and ensuring
agility in response to changes.

Best Practice Alignment:
- Adhering to normalization aligns with industry standards, ensuring the database is developed with best
practices in mind.





## Recommendation

The database provided was investigated. Below are the findings:

- From the datasets, it is observed that the database provided had only one table consisting of 10
columns( TransactionID, Timestamp, CustomerID, Name, Surname, Shipping-State, Item, Description,
Retail-Price, and Loyalty-Discount).
- The database design is denormalized because all information as regards the clothing data is placed
on just one table with different columns.


The denormalized data as a result can lead :

- Difficulty in Ensuring Data Integrity.
- Data Redundancy i.e. same information is stored in multiple places and that can lead to
  inconsistencies and increase the chances of data errors.
- Update Anomalies: With denormalization, updating data in one place might be overlooked in other
  places, leading to inconsistencies. For example, if a customer changes their shipping address, it needs to
  be updated in every row where that customer is mentioned.
- Complex Queries: Writing complex queries to extract specific information becomes more
  challenging due to the spread of data across multiple columns. This can result in slower query
  performance.
- Limited Scalability: As the number of transactions and customers increases, the denormalized
  database may struggle to scale efficiently. This can impact system performance and responsiveness.







---

### Thank you for reading.

I am open for entry-level to mid_level data analyst role.

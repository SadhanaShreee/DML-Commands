# DML-Commands

## AIM:
 To Study and Implement DML Commands.
 ## THEORY:
 ```
 1.INSERT INTO:
 This is used to add records into a relation.
 These are three type of INSERT INTO queries which are as
 A)Inserting a single record
 Syntax:
 INSERTINTO<relation/table name> (field_1,field_2……field_n)VALUES (data_1,data_2,
 ......data_n);student(sno,sname,class,address)VALUES (1,’Ravi’,’M.Tech’,’Palakol’);
 B)Inserting all records from another relation
 Syntax:
 INSERTINTOrelation_name_1 SELECT Field_1,field_2,field_n FROM relation_name_2
 WHEREfield_x=data;
 C)Inserting multiple records
 Syntax:
 INSERTINTOrelation_name field_1,field_2,.................field_n) VALUES
 (&data_1,&data_2,....... &data_n);
 2.UPDATE-SET-WHERE:
 This is used to update the content of a record in a relation.
 Syntax:
 SQL>UPDATErelation name SET Field_name1=data,field_name2=data, WHERE
 field_name=data; Example: SQL>UPDATE student SET sname = ‘kumar’ WHEREsno=1;
 12
3.DELETE-FROM:
 This is used to delete all the records of a relation but it will retain the structure of that relation.
 A)DELETE-FROM: This is used to delete all the records of relation.
 Syntax:
 DELETEFROMrelation_name;
 b)DELETE-FROM-WHERE:Thisisused to delete a selected record from a relation.
 Syntax:
 DELETEFROMrelation_name WHERE condition;
 4.SELECT FROM:
 To display a set of fields for all records of relation
 Syntax:
 SELECT(column1,column2) FROM (Table Name)WHERE condition;
```

```
Question 1:
 Write a SQL query to find all those customers who does not have any grade. Return customer_id,
 cust_name, city, grade, salesman_id.

Answer:
 SELECT customer_id , cust_name, city, grade, salesman_id
 FROMcustomer
 WHEREgrade IS NULL;
```
 ## Output:
![Screenshot 2024-11-20 135722](https://github.com/user-attachments/assets/2de9155d-44c0-4cff-845f-f8c3162563f8)

 ```
Question 2:
 Write a SQL statement to Display names and city of salesman, who belongs to the city of London or Rome.
 13

Answer:
 SELECT name,city
 FROMsalesman
 WHEREcity='London' OR city='Rome';
```
## Output:
![Screenshot 2024-11-20 135734](https://github.com/user-attachments/assets/79cd3aa3-0206-48ac-b512-5ef77aced33a)

```
Question 3:
 Write a SQL statement to get the EmployeeID, FirstName, BirthDate, Age from employees table whose age
 is older than 50.

Answer:
 ALTERTABLEemployees
 ADDAgeinteger;
 UPDATEemployees
 SET Age =Current_Date-BirthDate;
 SELECT EmployeeID, FirstName, BirthDate, Age
 FROMemployees WHEREAge>50;
```
## Output:
![Screenshot 2024-11-20 135743](https://github.com/user-attachments/assets/9e7159df-7da4-459d-a356-302a1df3ceb4)

```
Question 4:
 Write a SQL statement to Find those salesmen with all information whose name containing the 1st character
 is 'N' and the 4th character is 'l' and rests may be any character.

Answer:
 SELECT *FROMsalesman
 WHEREnameLIKE'N__l%';
```
## Output:
![Screenshot 2024-11-20 135850](https://github.com/user-attachments/assets/f2723011-69f3-428c-ae94-95be7e8f5a3a)

```
Question 5:
 Write a SQL statement to Update the reorder level to 20 where the quantity in stock is less than 10 and
 product category is 'Snacks' in the products table.

Answer:
 UPDATEproducts
 SET reorder_lvl=20
 WHEREquantity<10 AND category='Snacks';
```
## Output:
![Screenshot 2024-11-20 135901](https://github.com/user-attachments/assets/1516245d-dc4f-4b59-b840-b42ab7091b85)

```
Question 6:
 Increase the reorder level by 30% for products from 'Food' category having quantity in stock less than 50% of
 existing reorder level in the products table
 

Answer:
 UPDATE products
 SET reorder_lvl=reorder_lvl+reorder_lvl*0.3
 WHEREcategory='Food';
```
## Output:
![Screenshot 2024-11-20 135910](https://github.com/user-attachments/assets/0332ad40-7219-463f-a4c0-a7885d69dc22)

```
Question 7:
 Write a SQL statement to Update all customers in Chennai city to grade them as platinum customer (5).

Answer:
 UPDATEcustomer
 SET grade=5
 WHEREcity='Chennai';
```
## Output:
![Screenshot 2024-11-20 135946](https://github.com/user-attachments/assets/e50c38fd-ad73-46da-aa05-881678232cdb)

```
Question 8:
 Write a SQL query to remove rows from the table 'customer' with the following condition
1. 'cust_country' must be 'India',
2. 'cus_city' must not be 'Chennai',

Answer:
 DELETEFROMcustomer
 WHEREcust_country='India' AND NOT cust_city='Chennai';
```
## Output:
![Screenshot 2024-11-20 140003](https://github.com/user-attachments/assets/39154767-b280-4d93-aec5-337dd88e8e95)

```
Question 9:
 Write a SQL query to Delete customers with 'GRADE' 3 or 'AGENT_CODE' 'A008' whose
 'OUTSTANDING_AMT' is less than 5000

Answer:
 DELETEFROMCustomer
 WHERE(grade=3 or agent_code='A008') AND outstanding_amt<5000;
```
## Output:
![Screenshot 2024-11-20 140015](https://github.com/user-attachments/assets/aa9baebb-1c6f-4228-af27-5d23d624d9f9)

```
Question 10:
 Write a SQL query to delete a doctor from Doctors table whos specialization is 'Cardiology'

Answer:
 DELETEFROMDoctors
 WHEREspecialization='Cardiology';
```
## Output:
![Screenshot 2024-11-20 140120](https://github.com/user-attachments/assets/bfce56ee-d254-4c23-9322-7bbe9d17f843)


## Result:
 Thus , the SQL queries to implement DML commands have been executed successfully.


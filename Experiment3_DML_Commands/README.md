# Experiment 3: DML Commands

## AIM
To study and implement DML (Data Manipulation Language) commands.

## THEORY

### 1. INSERT INTO
Used to add records into a relation.
These are three type of INSERT INTO queries which are as
A)Inserting a single record
**Syntax (Single Row):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES (value_1, value_2, ...);
```
**Syntax (Multiple Rows):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES
(value_1, value_2, ...),
(value_3, value_4, ...);
```
**Syntax (Insert from another table):**
```sql
INSERT INTO table_name SELECT * FROM other_table WHERE condition;
```
### 2. UPDATE
Used to modify records in a relation.
Syntax:
```sql
UPDATE table_name SET column1 = value1, column2 = value2 WHERE condition;
```
### 3. DELETE
Used to delete records from a relation.
**Syntax (All rows):**
```sql
DELETE FROM table_name;
```
**Syntax (Specific condition):**
```sql
DELETE FROM table_name WHERE condition;
```
### 4. SELECT
Used to retrieve records from a table.
**Syntax:**
```sql
SELECT column1, column2 FROM table_name WHERE condition;
```
**Question 1**
--
Write a SQL statement to change the first_name column of employees table with 'John' for those employees whose department_id is 80 and gets a commission_pct below 0.35.

```sql
update EMPLOYEES set first_name = "John" where department_id = 80 and commission_pct < .35;
```

**Output:**

![image](https://github.com/user-attachments/assets/a6eadae2-2222-4849-adcb-a23e990d15e8)

**Question 2**
---
Write a SQL statement to update the product_name as 'Grapefruit' whose product_id is 4 in the products table.

```sql
update products set product_name = "Grapefruit" where product_id = 4;
```

**Output:**

![image](https://github.com/user-attachments/assets/ed3922bd-3991-4dc6-a589-2f5413bd14f6)


**Question 3**
---
Write a SQL statement to change the EMAIL and COMMISSION_PCT column of the following EMPLOYEES table with 'not available' and 0.55 for those employees whose DEPARTMENT_ID is 110.

```sql
update employees set email = 'not available', commission_pct = 0.55 where department_id=110;
```

**Output:**

![image](https://github.com/user-attachments/assets/1f983944-b367-4b94-8fc9-77dd8e8837eb)

**Question 4**
---
Write a SQL statement to Increase the selling price by 15% in the products table where quantity in stock is less than 50 and supplier ID is 10.

```sql
update products set sell_price = sell_price*1.15 where supplier_id = 10 and quantity < 50;
```

**Output:**

![image](https://github.com/user-attachments/assets/ecc3298c-cf68-4317-a62f-04b52d19ea34)

**Question 5**
---
Write a SQL query to Delete All Doctors whose ID ranges from 2 to 4.

```sql
delete from Doctors where doctor_id between 2 and 4;
```

**Output:**

![image](https://github.com/user-attachments/assets/6fb8210b-4c95-41b9-9b69-fac7ef869185)

**Question 6**
---
Write a SQL statement to Find the salesmen with all information who gets the commission within a range of 0.12 and 0.14.

```sql
select * from salesman where commission between 0.12 and 0.14;
```

**Output:**

![image](https://github.com/user-attachments/assets/c91e1f4b-4fa3-4782-b80a-4dfbec461ddb)

**Question 7**
---
Write a SQL statement to Find those salesmen with all information whose name containing the 1st character is 'N' and the 4th character is 'l' and rests may be any character.

```sql
select * from salesman where name like 'N__l%';
```

**Output:**

![image](https://github.com/user-attachments/assets/fad695a4-5201-4b71-853c-8b69d5b3333e)

**Question 8**
---
Write a SQL query to assign a priority of 'Low', 'Medium', or 'High' to value2 based on whether it is less than 20, between 20 and 50, or greater than 50, respectively in the Calculations table.

```sql
select id,value2, 
case
    when value2 < 20 then 'Low'
    when value2 between 20 and 50 then 'Medium'
    when value2 > 50 then 'High'
    end as priority from Calculations;
```

**Output:**

![image](https://github.com/user-attachments/assets/e799c324-a870-431f-add1-16e4672c4243)

**Question 9**
---
Write a SQL query to calculate the absolute value of the value1 column from the Calculations table.

```sql
select id,value1,abs(value1) as absolute_value from Calculations;
```

**Output:**

![image](https://github.com/user-attachments/assets/07c5864f-33c8-4cec-b50d-4501f8e66f59)

**Question 10**
---
Write a SQL query to select orders between 500 and 4000 (begin and end values are included). Exclude orders amount 948.50 and 1983.43. Return ord_no, purch_amt, ord_date, customer_id, and salesman_id.

```sql
select ord_no, purch_amt, ord_date, customer_id, salesman_id from orders 
where purch_amt between 500 and 4000
and purch_amt not in (948.50, 1983.43);
```

**Output:**

![image](https://github.com/user-attachments/assets/c695dc00-535a-4376-af3c-05f18adbf911)

## RESULT
Thus, the SQL queries to implement DML commands have been executed successfully.

## PROOF
![image](https://github.com/user-attachments/assets/29eef278-b24e-4e3c-bd60-9b259f4e2f92)

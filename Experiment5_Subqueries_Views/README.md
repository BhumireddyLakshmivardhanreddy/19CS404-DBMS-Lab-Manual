# Experiment 5: Subqueries and Views

## AIM
To study and implement subqueries and views.

## THEORY

### Subqueries
A subquery is a query inside another SQL query and is embedded in:
- WHERE clause
- HAVING clause
- FROM clause

**Types:**
- **Single-row subquery**:
  Sub queries can also return more than one value. Such results should be made use along with the operators in and any.
- **Multiple-row subquery**:
  Here more than one subquery is used. These multiple sub queries are combined by means of ‘and’ & ‘or’ keywords.
- **Correlated subquery**:
  A subquery is evaluated once for the entire parent statement whereas a correlated Sub query is evaluated once per row processed by the parent statement.

**Example:**
```sql
SELECT * FROM employees
WHERE salary > (SELECT AVG(salary) FROM employees);
```
### Views
A view is a virtual table based on the result of an SQL SELECT query.
**Create View:**
```sql
CREATE VIEW view_name AS
SELECT column1, column2 FROM table_name WHERE condition;
```
**Drop View:**
```sql
DROP VIEW view_name;
```

**Question 1**
--
-- 
![image](https://github.com/user-attachments/assets/e52c50b7-ce20-49fd-9e73-3e80bbc9f0e8)

```sql
SELECT o.ord_no, o.purch_amt, o.ord_date, o.customer_id, o.salesman_id
FROM orders o
JOIN salesman s ON o.salesman_id = s.salesman_id
WHERE s.city = 'New York';

```

**Output:**
![image](https://github.com/user-attachments/assets/20a555fe-8bca-42b5-9c77-8e64b38e1457)

**Question 2**
---
-- 
![image](https://github.com/user-attachments/assets/3cba95b8-74fb-4a0e-a78b-0055f0177ac5)

```sql
SELECT *
FROM CUSTOMERS
WHERE ADDRESS = 'Delhi' AND AGE < 30;
```
**Output:**
![image](https://github.com/user-attachments/assets/1e933d71-321d-4dc2-89fa-ed1f19559e6a)

**Question 3**
**Output:**
![image](https://github.com/user-attachments/assets/f0bced16-db95-4b1b-b346-97b25a971ef2)

**Question 4**
**Output:**
![image](https://github.com/user-attachments/assets/35963a87-353e-48c6-9c0f-5559f76fcb9a)

**Question 5**
**Output:**
![image](https://github.com/user-attachments/assets/506217b5-f908-4ac5-9e00-462b44f8b969)

**Question 6**
**Output:**
![image](https://github.com/user-attachments/assets/75fb2601-c1a0-4a71-93f5-b9b6b9cfa59e)

**Question 7**
**Output:**
![image](https://github.com/user-attachments/assets/0a75abec-25f0-4e78-ab75-93bcd9733f85)

**Question 8**
**Output:**
![image](https://github.com/user-attachments/assets/77e2848e-cdb5-48d6-a800-21ba6f0b4c58)

**Question 9**
**Output:**
![image](https://github.com/user-attachments/assets/318e582f-c7b0-41f6-b944-b60710fc55df)

**Question 10**
**Output:**
![image](https://github.com/user-attachments/assets/a1e42189-e977-41b5-94eb-ef736958a6b8)

## RESULT
Thus, the SQL queries to implement subqueries and views have been executed successfully.

# indeed-sql-skill-test


Sure, here are the questions along with their answers:

---

**Head Question**

Which Statement is used to remove records from a database ?
- [ ] REMOVE
- [x] DELETE
- [ ] ELIM

**Answer:** DELETE

---

**Question 1 / 12**

You want to update the "status" column to 'Shipped' for all orders with an "order_date" before '2024-01-01'.

**What's the correct statement?**
- [x] UPDATE
- [ ] MODIFY
- [ ] ALTER
- [ ] DATE TO
- [ ] CHANGE

**Answer:** UPDATE

---

**Question 2 / 12**

DELETE FROM employees WHERE department = 'accounting';

**What role does the "WHERE" clause play in this statement?**
- [ ] It identifies the columns to be deleted in the specified table
- [x] It defines the condition that must be met for records to be deleted
- [ ] It indicates where in the table the deletion process should start
- [ ] It limits the number of records to be deleted from the table

**Answer:** It defines the condition that must be met for records to be deleted

---

**Question 3 / 12**

You want to find the latest order date for each customer.

**Which query is correct?**
- [ ] SELECT CustomerID, TOP(OrderDate) FROM Orders GROUP BY CustomerID;
- [ ] SELECT CustomerID, MAX(OrderDate) FROM Orders;
- [x] SELECT CustomerID, MAX(OrderDate) FROM Orders GROUP BY CustomerID;
- [ ] SELECT CustomerID, MIN(OrderDate) FROM Orders;
- [ ] SELECT CustomerID, LATEST(OrderDate) FROM Orders GROUP BY CustomerID;

**Answer:** SELECT CustomerID, MAX(OrderDate) FROM Orders GROUP BY CustomerID;

---

**Question 4 / 12**

You want to review the "name" and "email" columns records from a large "employees" table. You decide to examine a few records to understand the data better.

**Which query is correct?**
- [ ] SELECT * FROM employees LIMIT 25;
- [ ] SELECT name, email FROM employees MAX(25);
- [ ] SELECT * FROM employees(name, email) LIMIT 25;
- [x] SELECT name, email FROM employees LIMIT 25;
- [ ] SELECT SUM(name, email) FROM employees;

**Answer:** SELECT name, email FROM employees LIMIT 25;

---

**Question 5 / 12**

You want to find the names of employees who joined in 2022.

**Which query is correct?**
- [ ] SELECT first_name, last_name FROM employees (joining_year) = (2022);
- [x] SELECT first_name, last_name FROM employees WHERE YEAR(joining_date) = 2022;
- [ ] SELECT first_name, last_name FROM employees WHERE joining_date IN '2022%';
- [ ] SELECT first_name, last_name FROM employees WHERE joining_date > '2022-01-01';

**Answer:** SELECT first_name, last_name FROM employees WHERE YEAR(joining_date) = 2022;

---

**Question 6 / 12**

SELECT columns(1,2,3) FROM payments WHERE amount > 10;

**Why would this query not work?**
- [ ] The table name "payments" should be in double quotes
- [ ] The WHERE clause isn't allowed in a SELECT statement
- [x] The SELECT statement should specify column names instead of "columns(1,2,3)"
- [ ] The column numbers (1,2,3) and table name "payments" should be in single quotes
- [ ] The condition "> 10" is not properly formatted for comparing the "amount" column

**Answer:** The SELECT statement should specify column names instead of "columns(1,2,3)"

---

**Question 7 / 12**

SELECT customer_name, registration_date FROM customers ORDER BY registration_date DESC;

**How does the ORDER BY clause impact the performance of this query?**
- [ ] It improves performance by reducing the storage space needed for the result set
- [ ] It improves performance by reducing the number of rows
- [x] It may negatively affect performance if the dataset is large
- [ ] It has no impact on performance, regardless of dataset size
- [ ] It will degrade performance significantly, regardless of dataset size

**Answer:** It may negatively affect performance if the dataset is large

---

**Question 8 / 12**

Library members can borrow books, forming a "many-to-many" relationship between the entities "members" and "books."

**How would this affect database querying? There's _____.**
- [ ] increased simplicity in query design
- [ ] automatic consolidation of duplicate entries within the database
- [x] a need for a linking table to manage the relationship
- [ ] more direct data retrieval
- [ ] decreased need for indexing

**Answer:** a need for a linking table to manage the relationship

---

**Question 9 / 12**

Review this ineffective query:

1. SELECT category_id, AVG(price) AS avg_price
2. FROM products
3. HAVING avg_price < 50
4. GROUP BY category_id
5. ORDER BY category_id;

**Which two lines would you flip to fix it?**
- [ ] 2 and 3
- [ ] 2 and 4
- [ ] 2 and 5
- [x] 3 and 4
- [ ] 4 and 5

**Answer:** 3 and 4

---

**Question 10 / 12**

SELECT customer.name, SUM(payment.payment_amount) FROM customer JOIN payment ON customer.customer_id = payment.customer_id GROUP BY customer.name WHERE payment.payment_amount > 5000

**Why would this query not work as expected?**
- [ ] The JOIN operation is performed incorrectly
- [ ] The GROUP BY clause should come before the JOIN operation
- [ ] The query is missing an ORDER BY clause
- [x] The WHERE clause should come before the GROUP BY clause
- [ ] The SUM function won't work with the payment_amount column

**Answer:** The WHERE clause should come before the GROUP BY clause

---

**Question 11 / 12**

You want to retrieve the first and last names of customers from Columbus, OH, and Portland, ME.

**Which query is correct?**
- [ ] SELECT first_name AND last_name FROM customers WHERE state = 'OH' AND city = 'Columbus' AND state = 'ME' AND city = 'Portland';
- [ ] SELECT first_name, last_name FROM customers WHERE (state = 'OH' AND city = 'Columbus') OR (state = 'ME' AND city = 'Portland');
- [ ] SELECT first_name, last_name FROM customers WHERE (state = 'OH' AND city = 'Columbus') AND (state = 'ME' AND city = 'Portland');
- [ ] SELECT first_name, last_name FROM customers WHERE state = 'OH' AND city = 'Columbus' AND state = 'ME' AND city = 'Portland';
- [x] SELECT first_name, last_name FROM customers WHERE state = 'OH' AND city = 'Columbus' OR state = 'ME' AND city = 'Portland';

**Answer:** SELECT first_name, last_name FROM customers WHERE state = 'OH' AND city = 'Columbus' OR state = 'ME' AND city = 'Portland';

---

**Question 12 / 12**

You want to join the "orders" and "customers" tables to return order IDs along with customers' first and last names.

**Which query is correct?**
- [ ] JOIN orders, customers USING (customer_id) SELECT order_id, first_name, last_name;
- [ ] SELECT order_id, first_name, last_name FROM orders JOIN customers ON orders.order_id = customers.customer_id;
- [ ] SELECT order_id FROM orders, SELECT first_name, last_name FROM customers WHERE orders.customer_id = customers.customer_id;
- [x] SELECT order_id, first_name, last_name FROM orders JOIN customers ON orders.customer_id = customers.customer_id;

**Answer:** SELECT order_id, first_name, last_name FROM orders JOIN customers ON orders.customer_id = customers.customer_id;

---

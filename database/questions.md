# Database Excercises

#### 1 - Reterive all data from customer, branch, depositor, loan, account, borrower
```sql
SELECT * FROM branch;
SELECT * FROM customer;
SELECT * FROM depositor;
SELECT * FROM loan;
SELECT * FROM account;
SELECT * FROM borrower;
```

#### 2 - Reterive the names and cities of all borrowers
```sql
SELECT customer_name, customer_city
FROM customer
WHERE customer_name in (SELECT customer_name FROM borrower);
```


#### 3 - Reterive set of names and cities of customers who have 'Perryridge' branch

#### 4 - Reterive the number of accounts with balance between 700 and 900
```sql
SELECT count(account_number)
FROM account
WHERE balance BETWEEN 700 AND 900;
```

#### 5 - Reterive the names of customer on streets with names ending in 'hill' - string pattern matching
```sql
SELECT customer_name
FROM customer
WHERE customer_street like '%hill';
```

#### 6 - Reterive the names of customer with both account and ?? balance

3
1. Introduction
```SQL
SELECT billing_state, COUNT(*) AS num_row, AVG(total) AS avg_sale
  FROM invoice
 WHERE billing_country='USA'
 GROUP BY billing_state;
```

2. Grouping over Several Columns 
```SQL
SELECT billing_country, billing_state, COUNT(*) AS num_row, AVG(total) AS avg_sale
  FROM invoice
 GROUP BY billing_country, billing_state;
```

3. Adding Conditions on an Aggregated Column: the Correct Way
```SQL
SELECT billing_country, billing_state, COUNT(*) AS num_row, AVG(total) AS avg_sale 
  FROM invoice
 GROUP BY billing_country, billing_state
 HAVING COUNT(*) > 40;
```

4. Revisiting the Order of Execution
```SQL
SELECT 2, 3, 6;
```

5. Adding Conditions on Not-Displayed Aggregate Column
```SQL
SELECT MIN(total) AS min_sale, MAX(total) AS max_sale
  FROM invoice
 GROUP BY billing_country, billing_state
 HAVING AVG(total)<10;
```

6. Combining WHERE and HAVING Clauses
```SQL
SELECT billing_country, billing_state, MIN(total) AS min_sale, MAX(total) AS max_sale 
  FROM invoice
 WHERE NOT billing_state='None'
 GROUP BY billing_country, billing_state
HAVING AVG(total) < 10;
```

Assessment
```SQL

```

```SQL

```

```SQL

```

```SQL

```

```SQL

```

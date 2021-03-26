1. Introduction
```SQL
SELECT COUNT(*) AS num_row
  FROM invoice
 WHERE billing_country='USA';
```

2. Counting Rows by Group
```SQL
SELECT billing_country, COUNT(*) AS num_row
  FROM invoice
 GROUP BY billing_country;
```

3. Summary Statistics by Group
```SQL

```

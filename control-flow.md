1. If... Then in SQL
```SQL
SELECT invoice_id, total, 
       (CASE 
        WHEN total>10 THEN 'High' 
        ELSE 'Low' END) AS total_category
  FROM invoice;
```

2. Multiple If... Thens
```SQL

```

Assessment
```SQL
SELECT SUBSTRING(name, 1, 5) AS short_name
  FROM artist;
```

```SQL
SELECT 1;
```

```SQL
SELECT 4;
```

```SQL
SELECT track_id, name, CAST(bytes AS REAL)/1000000 AS megabytes
  FROM track
 LIMIT 5; 
```

```SQL
SELECT ROUND(CAST(bytes AS REAL)/1000000, 2) AS megabytes
  FROM track;
```

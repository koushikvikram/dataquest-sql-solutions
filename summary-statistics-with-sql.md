1. Introduction
```SQL
SELECT name, album_id, milliseconds
  FROM track
 WHERE unit_price>=1.00;
```

2. Using Several Statistics in a Column
```SQL
SELECT MIN(milliseconds) AS min_runtime, MAX(milliseconds) AS max_runtime
  FROM track;
```

3. Using Aggregate Functions with Computed Columns
```SQL
SELECT AVG((milliseconds / 1000.0 / 60)) AS avg_runtime_minutes, AVG(bytes / 1024.0 / 1024) AS avg_size_megabyte
  FROM track;
```

4. Combining Aggregate and Scalar Functions
```SQL
SELECT AVG(milliseconds/1000.0/60) AS avg_runtime_minutes, ROUND(AVG(milliseconds/1000.0/60), 2) AS avg_runtime_minutes_rounded
  FROM track;
```

5. Combining Aggregate Functions with Arithmetic Operators
```SQL
SELECT AVG(milliseconds) AS avg_runtime, SUM(milliseconds)*1.0/COUNT(milliseconds) AS another_avg_runtime
  FROM track;
```

6. 

# Develop the Python Code to:
* create the swimmers table - [Project SQL Statements](https://github.com/jctmcclain/Python-Intro/blob/main/swimmingapp/database-notes.md)
* insert data

```python
import duckdb

con = duckdb.connect('swimmingdb.db')
con.sql('')
con.close()
```

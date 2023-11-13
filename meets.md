# Develop the Python Code to:
* create the meets table
* insert data

```python
# Add your Python Code

# import DuckDB Module
import duckdb

#  Create connection
con = duckdb.connection("database.db")

#  Add SQL Statement
strSQL = 'CREATE OR REPLACE TABLE meets(m_id integer primary key, 
meet_location varchar(200), 
meet_type varchar(40),
meet_date varchar(20),
meet_time varchar(20),
landmarkconf varchar(20)
)'
#  Exectute SQL Statement
con.sql(strSQL)

#  Exectute SQL Statement2
strSQL2 = 'create sequence meetid start 100'
#  Exectute SQL Statement
con.sql(strSQL2)

strSQL3 = 'select * from meets'
con.sql(strSQL3)

# Close connection
con.close()


# print("Hello World")
# Stop your Python Code
```

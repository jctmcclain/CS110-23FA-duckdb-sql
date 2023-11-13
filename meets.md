# Develop the Python Code to:
* create the meets table
* insert data

```python
# Add your Python Code

import DuckDB
con = duckdb.connection("database.db")
strSQL = " "
con.sql(strSQL)
con.close()
CREATE OR REPLACE TABLE meets(m_id integer primary key, 
meet_location varchar(200), 
meet_type varchar(40),
meet_date varchar(20),
meet_time varchar(20),
landmarkconf varchar(20)
);
create sequence meetid start 100

print("Hello World")
# Stop your Python Code
```

# Develop the Python Code to:
- [x] create the meets table - [Project SQL Statements](https://github.com/jctmcclain/Python-Intro/blob/main/swimmingapp/database-notes.md)
- [ ] insert data
- [x] select data

```python
# Add your Python Code

# import DuckDB Module
import duckdb

#  Create connection
con = duckdb.connection("swimmingdb.db")

#  Add SQL Statement
strSQL = 'CREATE OR REPLACE TABLE meets(m_id integer primary key, meet_location varchar(200), meet_type varchar(40),meet_date varchar(20),meet_time varchar(20),landmarkconf varchar(20))'
#  Exectute SQL Statement
con.sql(strSQL)

#  Exectute SQL Statement2
strSQL2 = 'create sequence meetid start 100'
#  Exectute SQL Statement
con.sql(strSQL2)

strSQL3 = 'select * from meets'
rs = con.sql(strSQL3)
rs.show()

# Close connection
con.close()


# print("Hello World")
# Stop your Python Code
```

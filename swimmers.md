# Develop the Python Code to:
- [x] create the swimmers table - [Project SQL Statements](https://github.com/jctmcclain/Python-Intro/blob/main/swimmingapp/database-notes.md)
- [ ] insert data
- [ ] select data

```python
import duckdb

con = duckdb.connect('swimmingdb.db')
con.sql('CREATE OR REPLACE TABLE swimmers(s_id integer primary key, firstname varchar(40), lastname varchar(40),jcclass varchar(20),hometown varchar(100),school_district varchar(200),email varchar(100),roster varchar(20))')
# only run once
con.sql('create sequence swimmerid start 10')
con.close()
```


# SQL Statement for Swimmers - Not Pythonized
```sql
insert into swimmers values(nextval('swimmerid'),'Betty','Backstroker','FR','Huntingdon,PA','Huntingdon Area','betty@swim.cc','women');
```
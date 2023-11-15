# Develop the Python Code to:
- [x] create the events table - [Project SQL Statements](https://github.com/jctmcclain/Python-Intro/blob/main/swimmingapp/database-notes.md)
- [ ] insert data
- [ ] select data

```python
import duckdb

con = duckdb.connect('swimmingdb.db')
con.sql('CREATE OR REPLACE TABLE events(e_id integer primary key, event_name varchar(200), event_type varchar(40), event_order integer)')
con.sql('create sequence eventid start 1000;')
con.close()
```

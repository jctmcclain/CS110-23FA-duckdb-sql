# Develop the Python Code to:
- [x] create the swimmer stats table - [Project SQL Statements](https://github.com/jctmcclain/Python-Intro/blob/main/swimmingapp/database-notes.md)
- [ ] insert data
- [ ] select data

```python
import duckdb

con = duckdb.connect('swimmingdb.db')
con.sql('CREATE OR REPLACE TABLE swimmerstats(id integer primary key, s_id integer, m_id integer, e_id integer, tm_minutes integer, tm_seconds integer, tm_hundredth_seconds integer, meet_place varchar(20), FOREIGN KEY (s_id) references swimmers(s_id), FOREIGN KEY (m_id) references meets(m_id), FOREIGN KEY (e_id) references events(e_id))')
con.sql('create sequence sstatid start 1')
con.close()
```

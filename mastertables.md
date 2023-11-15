# Complete listing to create tables 

``python

import duckdb

con = duckdb.connect('swimmingdb.db')

# Events - 1000
# Meets - 
# Swimmers - 10

# - DEVELOPMENT STAGE do not run as TESTING or PRODUCTION

con.sql('CREATE OR REPLACE TABLE swimmers(s_id integer primary key, firstname varchar(40), lastname varchar(40),jcclass varchar(20),hometown varchar(100),school_district varchar(200),email varchar(100),roster varchar(20))')
con.sql('create or replace sequence swimmerid start 10')

con.sql('CREATE OR REPLACE TABLE events(e_id integer primary key, event_name varchar(200), event_type varchar(40), event_order integer)')
con.sql('create or replace sequence eventid start 1000;')

#  Add SQL Statement
strSQL = 'CREATE OR REPLACE TABLE meets(m_id integer primary key, meet_location varchar(200), meet_type varchar(40),meet_date varchar(20),meet_time varchar(20),landmarkconf varchar(20))'
#  Exectute SQL Statement
con.sql(strSQL)

#  Exectute SQL Statement2
strSQL2 = 'create or replace sequence meetid start 100'
#  Exectute SQL Statement
con.sql(strSQL2)


con.sql('CREATE OR REPLACE TABLE swimmerstats(id integer primary key, s_id integer, m_id integer, e_id integer, tm_minutes integer, tm_seconds integer, tm_hundredth_seconds integer, meet_place varchar(20), FOREIGN KEY (s_id) references swimmers(s_id), FOREIGN KEY (m_id) references meets(m_id), FOREIGN KEY (e_id) references events(e_id))')
con.sql('create or replace sequence sstatid start 1')

# Show table Meets 
strSQL3 = 'select * from meets'
rs = con.sql(strSQL3)
rs.show()

con.close()
```

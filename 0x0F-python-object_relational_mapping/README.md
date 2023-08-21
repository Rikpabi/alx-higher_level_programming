# 0x0F. Python - Object-relational mapping

## Learning Objectives
* Why Python programming is awesome
* How to connect to a MySQL database from a 

Python script
* How to `SELECT` rows in a MySQL table from a 

Python script
* How to `INSERT` rows in a MySQL table from a 

Python script
* What ORM means
* How to map a Python Class to a MySQL table


## Requirements
   - Install `MySQLdb` module version 2.0.x
     * For installing `MySQLdb`, you need to have 

`MySQL` installed: [How to install MySQL 8.0 in 

Ubuntu 20.04]

(https://intranet.alxswe.com/rltoken/paGukker_0Ko

G3D9FqymNQ)
     - $ sudo apt-get install python3-dev
     - $ sudo apt-get install libmysqlclient-dev
     - $ sudo apt-get install zlib1g-dev
     - $ sudo pip3 install mysqlclient
     - ...
     - $ python3
     - >>> import MySQLdb
     - >>> MySQLdb.version_info 
     - (2, 0, 3, 'final', 0)
   - Install `SQLAlchemy` module version `1.4.x`
     - $ sudo pip3 install SQLAlchemy
     - ...
     - $ python3
     - >>> import sqlalchemy
     - >>> sqlalchemy.__version__ 
     - '1.4.22'
   * Also, you can have this warning message:
     - 

/usr/local/lib/python3.4/distpackages/sqlalchemy/

engine/default.py:552: Warning: (1681, 

"'@@SESSION.GTID_EXECUTED' is deprecated and will 

be re
moved in a future release.")                      

     - cursor.execute(statement, parameters)  

   * You can ignore it.

---

### [0. Get all states](./0-select_states.py)
* A script that lists all `states` from the 

database `hbtn_0e_0_usa`. The script should take 

3 arguments: `mysql username`, `mysql password` 

and `database name` (no argument validation 

needed), Using the module `MySQLdb` (`import 

MySQLdb`), The script should connect to a MySQL 

server running on `localhost` at port `3306`, 

Results must be sorted in ascending order by 

`states.id`. Code should not be executed when 

imported.


### [1. Filter states](./1-filter_states.py)
* A script that lists all `states` with a `name` 

starting with `N` (upper N) from the database 

`hbtn_0e_0_usa`. The script should take 3 

arguments: `mysql username`, `mysql password` and 

`database name` (no argument validation needed), 

Using the module `MySQLdb` (`import MySQLdb`), 

The script should connect to a MySQL server 

running on `localhost` at port `3306`, Results 

must be sorted in ascending order by `states.id`. 

Code should not be executed when imported.

### [2. Filter states by user input](./2-

my_filter_states.py)
* A script that takes in an argument and displays 

all values in the `states` table of 

`hbtn_0e_0_usa` where `name` matches the 

argument. The script should take 4 arguments: 

`mysql username`, `mysql password`, `database 

name`, and `state name searched`(no argument 

validation needed), Using the module `MySQLdb` 

(`import MySQLdb`), The script should connect to 

a MySQL server running on `localhost` at port 

`3306`, Using `format` to create the SQL query 

with the user input, Results must be sorted in 

ascending order by `states.id`. Code should not 

be executed when imported.

### [3. SQL Injection...](./3-

my_safe_filter_states.py)
* Did you test `"Arizona'; TRUNCATE TABLE states 

; SELECT * FROM states WHERE name = '"` as an 

input? Empty? Yes, it’s an SQL injection to 

delete all records of a table…
* A script that takes in arguments and displays 

all values in the `states` table of 

`hbtn_0e_0_usa` where `name` matches the 

argument. But this time, it is safe from MySQL 

injections!. The script should take 4 arguments: 

`mysql username`, `mysql password`, `database 

name`, and `state name searched`(no argument 

validation needed), Using the module `MySQLdb` 

(`import MySQLdb`), The script should connect to 

a MySQL server running on `localhost` at port 

`3306`, Results must be sorted in ascending order 

by `states.id`. Code should not be executed when 

imported.

### [4. Cities by states](./4-cities_by_state.py)
* A script should take 3 arguments: `mysql 

username`, `mysql password` and `database name`, 

Using the module `MySQLdb` (`import MySQLdb`), 

The script should connect to a MySQL server 

running on `localhost` at port `3306`, Results 

must be sorted in ascending order by `cities.id`,
Using only `execute()` once. Code should not be 

executed when imported.

### [5. All cities by state](./5-

filter_cities.py)
* A script that takes in the name of a state as 

an argument and lists all `cities` of that state, 

using the database `hbtn_0e_4_usa`. The script 

should take 4 arguments: `mysql username`, `mysql 

password`, `database name` and `state name` (SQL 

injection free!), Using the module `MySQLdb` 

(`import MySQLdb`), The script should connect to 

a MySQL server running on `localhost` at port 

`3306`, Results must be sorted in ascending order 

by `cities.id`,
Using only `execute()` once. Code should not be 

executed when imported.

### [6. First state model](./model_state.py)
* A python file that contains the class 

definition of a `State` and an instance `Base = 

declarative_base()`. `State` class:
  - inherits from `Base` [Tips]

(https://intranet.alxswe.com/rltoken/SFKIwNZ3IG6_

4TL6dEsIuA)
  - links to the MySQL table `states`.
  - class attribute `id` that represents a column 

of an auto-generated, unique integer, can’t be 

null and is a primary key
  - class attribute `name` that represents a 

column of a string with maximum 128 characters 

and can’t be null.
* Using the module `SQLAlchemy`, The script 

should connect to a MySQL server running on 

`localhost` at port `3306`.
* WARNING: all classes who inherit from `Base` 

must be imported before calling 

`Base.metadata.create_all(engine)`.

### [7. All states via SQLAlchemy](./7-

model_state_fetch_all.py)
* A script that lists all `State` objects from 

the database `hbtn_0e_6_usa`. This script should 

take 3 arguments: `mysql username`, `mysql 

password` and `database name`. Using the module 

`SQLAlchemy`, import `State` and `Base` from 

`model_state` - `from model_state import Base, 

State`. The script should connect to a MySQL 

server running on `localhost` at port `3306`, 

Results must be sorted in ascending order by 

`states.id`, Code should not be executed when 

imported.

### [8. First state](./8-

model_state_fetch_first.py)
* A script that prints the first `State` object 

from the database `hbtn_0e_6_usa`. This script 

should take 3 arguments: `mysql username`, `mysql 

password` and `database name`. Using the module 

`SQLAlchemy`, import `State` and `Base` from 

`model_state` - `from model_state import Base, 

State`. The script should connect to a MySQL 

server running on `localhost` at port `3306`, 

Results must be sorted in ascending order by 

`states.id`, If the table `states` is empty, 

print `Nothing` followed by a new line. Code 

should not be executed when imported.

### [9. Contains `a`](./9-

model_state_filter_a.py)
* A script that lists all `State` objects that 

contain the letter `a` from the database 

`hbtn_0e_6_usa`. This script should take 3 

arguments: `mysql username`, `mysql password` and 

`database name`. Using the module `SQLAlchemy`, 

import `State` and `Base` from `model_state` - 

`from model_state import Base, State`. The script 

should connect to a MySQL server running on 

`localhost` at port `3306`, Results must be 

sorted in ascending order by `states.id`, Code 

should not be executed when imported.

### [10. Get a state](./10-model_state_my_get.py)
* A script that prints the State object with the 

name passed as argument from the database 

hbtn_0e_6_usa`. This script takes 4 arguments: 

`mysql username`, `mysql password`, `database 

name` and `state name to search` (SQL injection 

free). Using the module `SQLAlchemy`, import 

`State` and `Base` from `model_state - from 

model_state import Base, State`. This script 

connects to a MySQL server running on localhost 

at port `3306`. Assume you have one record with 

the state name to search. Results must display 

the `states.id`. If no state has the name you 

searched for, display `Not found`. Code should 

not be executed when imported.

### [11. Add a new state](./11-

model_state_insert.py)
* A  script that adds the `State` object 

“Louisiana” to the database `hbtn_0e_6_usa`. This 

script takes 3 arguments: `mysql username`, 

`mysql password` and `database name`. Using the 

module `SQLAlchemy`. Import `State` and `Base` 

from `model_state` - `from model_state import 

Base, State`. This script connects to a MySQL 

server running on `localhost` at port `3306`. 

Print the new `states.id` after creation. Code 

should not be executed when imported.

### [12. Update a state](./11-

model_state_insert.py)
* A script that changes the name of a `State` 

object from the database `hbtn_0e_6_usa`. This 

script takes 3 arguments: `mysql username`, 

`mysql password` and `database name`. Using the 

module `SQLAlchemy`. Import `State` and `Base` 

from `model_state` - `from model_state import 

Base, State`. This script connects to a MySQL 

server running on `localhost` at port `3306`. 

Change the name of the State where id = 2 to New 

Mexico. Code should not be executed when 

imported.

### [13. Delete states](./13-

model_state_delete_a.py)
* A script that deletes all `State` objects with 

`a` name containing the letter a from the 

database `hbtn_0e_6_usa`. This script takes 3 

arguments: `mysql username`, `mysql password` and 

`database name`. Using the module `SQLAlchemy`. 

Import `State` and `Base` from `model_state` - 

`from model_state import Base, State`. This 

script connects to a MySQL server running on 

`localhost` at port `3306`. Code should not be 

executed when imported.


### [14. Cities in state]([./model_city.py, ' '] 

[./14-model_city_fetch_by_state.py])
* A Python file similar to `model_state.py` named 

`model_city.py` that contains the class 

definition of a `City`.
  - `City` class:
    - inherits from `Base` (imported from 

`model_state`)
    - links to the MySQL table `cities`.
    - class attribute `id` that represents a 

column of an auto-generated, unique integer, 

can’t be null and is a primary key.
    - class attribute `name` that represents a 

column of a string of 128 characters and can’t be 

null.
    - class attribute `state_id` that represents 

a column of an integer, can’t be null and is a 

foreign key to `states.id`. Using the module 

`SQLAlchemy`.
* Next, A script `14-

model_city_fetch_by_state.py` that prints all 

`City` objects from the `database 

hbtn_0e_14_usa`. This script should take 3 

arguments: `mysql username`, `mysql password` and 

`database name`. Using the module `SQLAlchemy`. 

Import `State` and `Base` from `model_state` - 

`from model_state import Base, State`. This 

script connects to a MySQL server running on 

`localhost` at port `3306`. Results must be 

sorted in ascending order by `cities.id`.  <city 

name>). Code should not be executed when 

imported.

### [15. City relationship]

([./relationship_city.py, ' '] 

[./relationship_state.py, ' '] [./100-

relationship_states_cities.py])
* Improve the files `model_city.py` and 

`model_state.py`, and save them as 

`relationship_city.py` and 

`relationship_state.py`:
  - `City` class:
    - No change
  - `State` class:
    - In addition to previous requirements, the 

class attribute `cities` must represent a 

relationship with the class `City`. If the 

`State` object is deleted, all linked `City` 

objects must be automatically deleted. Also, the 

reference from a `City` object to his `State` 

should be named `state`. Using the module 

`SQLAlchemy`.
* Next, a script that creates the `State` 

“California” with the `City` “San Francisco” from 

the `database hbtn_0e_100_usa`: (`100-

relationship_states_cities.py`). This script 

takes 3 arguments: `mysql username`, `mysql 

password` and `database name`. Using the module 

`SQLAlchemy`. This script connects to a MySQL 

server running on `localhost` at port `3306`. 

Using the `cities` relationship for all `State` 

objects. Code should not be executed when 

imported.

### [16. List relationship](./101-

relationship_states_cities_list.py)
* A script that lists all `State` objects, and 

corresponding `City` objects, contained in the 

database `hbtn_0e_101_usa`. This script takes 3 

arguments: `mysql username`, `mysql password` and 

`database name`. Using the module `SQLAlchemy`.
This script connects to a MySQL server running on 

`localhost` at port `3306`. Only one query to the 

database. Using the `cities` relationship for all 

`State` objects. Results must be sorted in 

ascending order by `states.id` and `cities.id`. 

Code should not be executed when imported.

### [17. From city](./102-

relationship_cities_states_list.py)
* A script that lists all `City` objects from the 

database `hbtn_0e_101_usa`. This script takes 3 

arguments: `mysql username`, `mysql password` and 

`database name`. Using the module `SQLAlchemy`.
This script connects to a MySQL server running on 

`localhost` at port `3306`. Only one query to the 

database. Using the `state` relationship for all 

`State` objects linked to `City` object. Results 

must be sorted in ascending order by `states.id` 

and `cities.id`. Code should not be executed when 

imported.

---

## Author
* **Richard Akpabio** - [Rikpabi]

(http://github.com/Rikpabi)

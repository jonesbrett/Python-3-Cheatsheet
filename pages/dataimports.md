- [Return to Table of Contents](/../../)  

### Files

You can read data from a txt file with ' with open ('filename.txt') as 'text_file', the read the file and cache it as 'cache_file'.

```python
with open ('filename.txt') as text_file:
    cache_file = text_file.read()
    print(cache_file)
```
The above example will read the complete file and cache it as 'cache_file.

We can also read the file line by line.

```python
with open ('filename.txt') as text_file:
    first_line = text_file.readline()
    second_line = text_file.readline()
    print(second_line)
```
If we need to write to the file we can use the 'w' argument, the deafult argument is 'r' for read only.

```python
with open ('filename.txt' 'w') as text_file:
    text_file.write("Hello World")
```
> __Note__ 
The above example will overwrite the file.

We can append to the file using the 'a' argument.

```python
with open ('filename.txt' 'a') as text_file:
    text_file.write("Hello World")
```

### SQL

You can use the Pandas module to import data from a CSV file into a SQLite db:


```python
# Import sqlite3 module
import sqlite3
# Import pandas module into
import pandas

# Create a connection object,
# Make a new db if not exist already 
# and connect it, if exist then connect.
connection = sqlite3.connect("sp500.sqlite")
curs = connection.cursor()

# Creates the  table called "TradeData" with the following columns, id, date, open, high, low, close, volume, adj_close
curs.execute(
    """CREATE TABLE IF NOT EXISTS TradeData (id INTEGER, date text, open INTEGER, high INTEGER, low INTEGER, 
    close INTEGER, volume INTEGER, adj_close INTEGER)"""
)

# Load CSV into Pandas DataFrame
data = pandas.read_csv("sp500.csv")

# Write data to SQLite db table "TradeData"
data.to_sql("TradeData", connection, if_exists="replace", index=False)

# Prompts user if they want to view the imported data
prompt = input("Would you like to view the table: yes or no? ")
if prompt == "yes":
    curs.execute("select * from TradeData")
    trades = curs.fetchall()
    for row in trades:
        print(row)

print("closing connection")
connection.close()
```

- [Return to Table of Contents](/../../)  

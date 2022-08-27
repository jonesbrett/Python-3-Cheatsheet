
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
    """CREATE TABLE IF NOT EXISTS TradeData (id INTEGER, date text, open INTEGER, high INTEGER, low INTEGER, close INTEGER, volume INTEGER, adj_close INTEGER)"""
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

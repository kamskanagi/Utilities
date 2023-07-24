# Tutorial: Working with MySQL in Python

In this tutorial, we will cover the basics of working with MySQL in Python using the `mysql.connector` library. We will learn how to connect to a MySQL database, create tables, insert data, perform queries, and modify tables. By the end of this tutorial, you should have a good understanding of how to interact with a MySQL database in Python.

### Prerequisites:
- MySQL Server installed and running on your local machine.
- Python and `mysql.connector` library installed.

### Step 1: Install `mysql.connector`
If you haven't installed the `mysql.connector` library, you can do so using `pip`:

```bash
pip install mysql-connector-python
```

### Step 2: Import Libraries
Let's start by importing the required libraries:

```python
import mysql.connector
import datetime
```

### Step 3: Connect to the MySQL Database
Replace the host, user, and password with your MySQL server credentials:

```python
db = mysql.connector.connect(
    host="localhost",
    user="root",
    passwd="root",
    database="testdatabase"  # Add the name of the database you want to use
)
```

### Step 4: Create and Insert Data into a Table
We will create two tables, `Users` and `Scores`, and insert data into them:

```python
users = [("kevin", "tecth"),
         ("peter", "pet"),
         ("sul", "sulBoy")]

user_scores = [
    (45, 100),
    (30, 200),
    (20, 124)
]

Q1 = "CREATE TABLE Users (id int PRIMARY KEY AUTO_INCREMENT, name VARCHAR(50), passwd VARCHAR(50))"
Q2 = "CREATE TABLE Scores (userId int PRIMARY KEY, FOREIGN KEY(userId) REFERENCES Users(id), game1 int DEFAULT 0, game2 int DEFAULT 0)"

for x, user in enumerate(users):
    mycursor.execute("INSERT INTO Users (name, passwd) VALUES (%s, %s)", user)
    last_id = mycursor.lastrowid
    mycursor.execute("INSERT INTO Scores (userId, game1, game2) VALUES (%s, %s, %s)", (last_id,)+user_scores[x])

db.commit()
```

### Step 5: Perform Queries
Now, let's perform some queries to retrieve data from the `Users` and `Scores` tables:

```python
mycursor.execute("SELECT * FROM Users")

for x in mycursor:
    print(x)

mycursor.execute("SELECT * FROM Scores")

for x in mycursor:
    print(x)
```

### Step 6: Modify a Table
Finally, let's see how to modify a table. Below are some examples of table modifications:

```python
# Add a new column 'food' to the 'Users' table
mycursor.execute("ALTER TABLE Users ADD COLUMN food VARCHAR(50) NOT NULL")

# Remove the 'food' column from the 'Users' table
mycursor.execute("ALTER TABLE Users DROP food")

# Rename the 'name' column to 'first_name' in the 'Users' table
mycursor.execute("ALTER TABLE Users CHANGE name first_name VARCHAR(50)")
```

### Conclusion
In this tutorial, we learned the basics of connecting to a MySQL database in Python using the `mysql.connector` library. We explored creating tables, inserting data, performing queries, and modifying tables. With this knowledge, you can start building more complex applications that interact with MySQL databases using Python.

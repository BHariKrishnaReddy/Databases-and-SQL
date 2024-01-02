## Introduction to SQL Statements:
   * SQL statements are commands used to interact with tables in relational databases.
   * There are two main categories of SQL statements<br>
           * Data Definition Language (**DDL**) - used to define, modify, or delete database objects like tables.<br> 
           * Data Manipulation Language (**DML**) - used to read or modify data in tables, often called CRUD operations.

<h2 align = 'center'> DDL </h2>
 

#### CREATE TABLE statement syntax

        CREATE TABLE <table_name> (
            column_1 data_type_1,
            column_x data_type_x,
            column_z data_type_z,
            ...
        );

#### ALTER TABLE statement syntax
  * Purpose: Modify the structure of an existing table
  * Functionality: Add or remove columns, keys, and constraints. Modify the data type of columns

        #Adding a column
        ALTER TABLE <table_name>
        ADD COLUMN new_column data_type;

        #Dropping a column
        ALTER TABLE <table_name>
        DROP COLUMN column_to_drop;

        #Changing the DataType of the column
        ALTER TABLE table_name
        ALTER COLUMN column_name SET DATA TYPE new_data_type;

#### TRUNCATE TABLE statement syntax
  * Purpose: Delete all rows of data in a table
  * Functionality: Removes all data but retains the table structure.Immediate execution, irreversible

        TRUNCATE TABLE <table_name>;

#### DROP TABLE statement syntax
  * Purpose: Delete an existing table.
  * Functionality: Deletes both the table and its data by default 

        DROP TABLE <table_name>

<h2 align = 'center'> DML </h2>

#### SELECT statement syntax
  * Purpose: Retrieve data from a table.
  * Functionality: Reads one or more columns or all columns. Supports filtering and sorting

        `Select * from <table_name>`  # returns full table
        Select column_1,column_x,column_z from <table_name>  # returns full data, but only of the columns mentioned after the SELECT keyword.


#### INSERT - DML statement
  * Purpose: Add new data to a table
  * Functionality: Inserts one or multiple rows of data

        #### Entering one row at a time
        INSERT INTO <table_name> (column_1,column_x,column_z) VALUES (value_of_col1,value_of_colx,value_of_colz)
        
        #### Entering multiple rows at a time 
        INSERT INTO <table_name> (column_1,column_x,column_z) 
        VALUES  (value1_of_col1,value1_of_colx,value1_of_colz),
                (value2_of_col1,value2_of_colx,value2_of_colz),
                ..
                ..
                (valueN_of_col1,valueN_of_colx,valueN_of_colz)
        
#### UPDATE - DML statement, we use this to alter the table info/data
  * Purpose: Modify existing data in a table.
  * Functionality: Edits values in specified columns based on a condition
    
        UPDATE <table_name> SET [[column_x] = [value_of_colx]] < WHERE [CONDITION] # If there is no WHERE clause it will UPDATE the whole table!

#### DELETE  statement
  * Purpose: Remove data from a table
  * Functionality: Deletes rows based on a specified condition

        DELETE FROM  <table_name> WHERE [CONDITION] # If there is no WHERE clause it will DELETE the whole table!

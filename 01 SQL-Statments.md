### SELECT statement syntax
Select * from <table_name>  # returns full table
Select column_1,column_x,column_z from <table_name>  # returns full data, but only of the colmuns mentioned after select key word.


## INSERT - DML(Data Manipulation Lang) statment

# entering one row at a time
INSERT INTO <table_name> (column_1,column_x,column_z) VALUES (value_of_col1,value_of_colx,value_of_colz)

# entering multiple rows at a timw 
INSERT INTO <table_name> (column_1,column_x,column_z) 
VALUES  (value1_of_col1,value1_of_colx,value1_of_colz),
        (value2_of_col1,value2_of_colx,value2_of_colz),
        ..
        ..
        (valueN_of_col1,valueN_of_colx,valueN_of_colz)

## UPDATE - DML statement , we use this to alter the table info/data
UPDATE <table_name> SET [[column_x] = [value_of_colx]] < WHERE [CONDITION] # If there is no where clause it will UPDATE the whole table !

## DELETE  statement
DELETE FROM  <table_name> WHERE [CONDITION] # If there is no where clause it will DELETE the whole table !

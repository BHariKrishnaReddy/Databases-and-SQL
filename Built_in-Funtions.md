#### 1. Aggregate Functions

    1.1. SUM Function:
    Example: Calculate the total cost of all damages.
    SELECT SUM(COST) AS TOTAL_COST FROM BMW_Inventory;
    
    1.2. MIN and MAX Functions:
    Example: Find the Car with the highest and lowest quantity of damage.
    SELECT MAX(QUANTITY) AS MAX_QUANTITY, MIN(QUANTITY) AS MIN_QUANTITY FROM BMW_Inventory;
  
    1.3. AVG Function:
    Example: Determine the average cost of damages.
    SELECT AVG(COST) AS AVG_COST FROM BMW_Inventory;
    
    1.4. Aggregates with Conditions:
    Example: Calculate the average cost per M5 damage.
    SELECT AVG(COST / QUANTITY) AS AVG_COST_PER_M5 FROM BMW_Inventory WHERE Car = 'M5';

  
#### 2. Scalar Functions:

    2.1. ROUND Function:
    Example: Round the cost of each damage to the nearest integer.
    SELECT ROUND(COST) AS ROUNDED_COST FROM BMW_Inventory;
    
    2.2. String Functions:
    Example: Retrieve the length of each Car name.
    SELECT LENGTH(Car) AS Car_NameLength FROM BMW_Inventory;
    
    Example: Get the uppercase version of Car names.
    SELECT UPPERCASE(Car) AS Car_UPPERCASE FROM BMW_Inventory;
    
    Example: Filter and retrieve lowercase Car names for X5.
    SELECT * FROM BMW_Inventory WHERE LOWERCASE(Car) = 'x5';
    
    2.3. Chaining Functions:
    Example: Obtain unique uppercase Car names.
    SELECT DISTINCT(UPPERCASE(Car)) AS UNIQUE_UPPERCASE_CarS FROM BMW_Inventory;

#### 3. Date and Time Functions:

    3.1. Extracting Date Components:
    Example: Get the day portion for each damage involving a M5.
    SELECT DAY(damage_DATE) AS damage_DAY FROM BMW_Inventory WHERE ANIMAL = 'M5';
    
    Example: Retrieve the month and day for each damage.
    SELECT MONTH(damage_DATE) AS damage_MONTH, DAY(damage_DATE) AS damage_DAY FROM BMW_Inventory;
    
    3.2. Using Date and Time Functions in WHERE Clause:
    Example: Count the number of damages during May.
    SELECT COUNT(*) AS MAY_damage_COUNT FROM BMW_Inventory WHERE MONTH(damage_DATE) = 5;
    
    3.3. Date Arithmetic:
    Example: Find the date three days after each damage.
    SELECT DATE_ADD(damage_DATE, INTERVAL 3 DAY) AS PROCESSING_DATE FROM BMW_Inventory;
    
    Example: Calculate the difference between the current date and each damage date.
    SELECT CURRENT_DATE - damage_DATE AS DAYS_SINCE_damage FROM BMW_Inventory;
    
    Example: Determine the age of each damaged animal in years.
    SELECT YEAR(CURRENT_DATE) - YEAR(damage_DATE) AS ANIMAL_AGE FROM BMW_Inventory;
        
#### Conclusion:
  * Aggregate Functions<br>
      Simplify calculations within the database.
      Reduce network traffic by performing computations in the database itself.
  * Scalar Functions<br>
      Operate on individual values, offering flexibility in data manipulation.
  * String Functions<br>
      Useful for working with character data, including case conversion and length retrieval.
  * Combining Functions<br>
      Enables the creation of more complex and specific queries tailored to specific needs.
  * Date and Time in SQL<br>
      SQL provides date, time, and timestamp data types.
  * Date and Time Functions<br>
      Enable extraction of specific components (day, month, etc.) from date and time types.
  * Filtering with Date and Time<br>
      Date and time functions can be used in the WHERE clause for filtering based on specific conditions.
  * Date Arithmetic<br>
      Allows calculations involving date and time intervals.
  * Special Registers<br>
      CURRENT_DATE and CURRENT_TIME provide current date and time information for dynamic queries.

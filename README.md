<b>Data Types </b> <br/>
INT: Numeric variable without decimals <br/>
FLOAT: Numeric variable with decimals <br/>
TEXT: String variable <br/>
<br/>
Tuples are rows <br/>
<b>Comments </b> <br/>
Shortcut: Ctrl + / <br/>
Syntax: /* Comments */ <br/>
Other: -- also works for single line comments <br/>
<br/>
<b>Where</b><br/>
Equals (case-sensitive)                                    :               =                          where id = 20; // where id = "20"; <br/>
Does not equal                                             :               != or <>                   where id <> 20; // where id /= 20; <br/>
Equals non case-sensitive string                           :               LIKE                       where name LIKE "sarah thompson"; <br/>
In a list                                                  :               IN ("ITEM 1", "ITEM 2")    where name IN ("Sarah Thompson", "Kathy Smith"); // WHERE id IN (20, 51, 73); <br/>
Includes specific bit of string                            :               %                          where name LIKE "%sarah%; <br/>
Matches string with mystery character (only used with LIKE):               _                          where id like ("2_");
<br/>
To only return rows where a value is divisible by 2        :                                          where year % 2 = 0;

<b>Filtering</b> <br/>
Select distinct <br/>
Order by .... asc/desc <br/>
<br/>
Limit the number of rows returned                          :               LIMIT                      LIMIT 3; <br/>
Return rows after the nth row                              :               OFFSET                     LIMIT 3 OFFSET 1; <br/>

<b>Aggregation:</b> <br/>
SUM, AVG, MIN, MAX, COUNT

WHERE cannot be used if there is a GROUP BY statement.
In this situation HAVING is used instead.

<b>Order of Execution</b>

1: From and join <br/>
2: Where <br/>
3: Group by <br/>
4: Having <br/>
5: Select <br/>
6: Distinct <br/>
7: Order by <br/>
8: Limit/offset <br/>

If there is a UNION/INTERSECT/EXCLUDE this happens before ORDER BY

<b>Editing existing table:</b>

<b>Inserting a new row</b>

INSERT INTO tablename (column1, column2, column3)</br>
VALUES (value1, 'value2', value3);</br>

<b>Correcting existing row</b>

UPDATE tablename
SET column1 = value1,
    column2 = value2
WHERE column1 = "exampleerror";

Deleting a row
DELETE FROM tablename
WHERE condition;

<b>Create a blank table with columns</b>

CREATE TABLE table1 
(column1 TEXT,
column2 INT);

<b>Adding or removing a column:</b>

ALTER TABLE table1
ADD column1 INT;

You can specify if there is a default value:

ALTER TABLE table1
ADD column1 TEXT
DEFAULT 'N/A';

<b>Removing a column</b>

ALTER TABLE table1
DROP column1;

<b>Renaming a table</b>

ALTER TABLE table1
RENAME TO table_1;

<b>Delete a table:</b>

DROP TABLE table1;

<b>Joining tables vertically</b>

UNION: removes duplicate rows and vertically joins all elements without an order of operation
UNION ALL: joins all rows regardless of duplicates

INTERSECT: returns rows from the first table that are present in the second table
EXCEPT: returns rows from the first table that are not present in the second table

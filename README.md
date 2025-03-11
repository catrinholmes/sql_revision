Comments

Shortcut: Ctrl + /
Syntax: /* Comments */
Other: -- also works for single line comments

Where

Equals (case-sensitive)                                    :               =                          where id = 20; // where id = "20";
Does not equal                                             :               != or <>                   where id <> 20; // where id /= 20; 
Equals non case-sensitive string                           :               LIKE                       where name LIKE "sarah thompson";
In a list                                                  :               IN ("ITEM 1", "ITEM 2")    where name IN ("Sarah Thompson", "Kathy Smith"); // WHERE id IN (20, 51, 73);
Includes specific bit of string                            :               %                          where name LIKE "%sarah%;
Matches string with mystery character (only used with LIKE):               _                          where id like ("2_");

To only return rows where a value is divisible by 2        :                                          where year % 2 = 0;

Filtering

Select distinct 
Order by .... asc/desc

Limit the number of rows returned                          :               LIMIT                      LIMIT 3;
Return rows after the nth row                              :               OFFSET                     LIMIT 3 OFFSET 1;

Aggregation:
SUM, AVG, MIN, MAX,

WHERE filters rows before the GROUP BY statement
HAVING filters rows after the GROUP BY statement

Order of Execution

1: From and join
2: Where
3: Group by
4: Having
5: Select
6: Distinct
7: Order by
8: Limit/offset

About The Repository
===========
Topic | Description
--- | ---
Goal | The goal of this repository is to help us get familiarized with medium-to-advanced level SQL queries suitable for a Postgres Database. 

List of Contents
===========
- Query clause order
- Create Temp Table
- Date Syntax
- Syntax for SQL keyword ```not```



Knowledge-base
==========

SQL keyword | Usage | Example
--- | ---- | ----
```order by``` | This keyword is used to rearrange data in a specific order | (a) show employee names in order of their age, (b) how many customer are there from each country
```min``` function | How to find lowest value in a column | find the first order from the product table


#### Important Concepts in SQL
 - What is the difference in *like* vs *ilike*
 - What is the difference in *union* and *union all*
 - how to extract info from ```datetime```
 


#### Basic Syntax

Query clause order
```
SELECT
FROM
WHERE
GROUP BY
HAVING
ORDER BY

```


Create a Temp Table
```
drop table if exists table_name
;


create temp table table_name
(
  id int,
  name varchar(25),
  dob Date

)
;

```


Create a temp table from a given table
```
create temp table top_ten_salary as
(
  select emp_salary
  from employee_table 
  order by emp_salary desc
  limit 10
)
;

```

Date Syntax
```
start_time::timestamptz AT TIME ZONE 'America/New_York' 
  BETWEEN '2017-12-25' 
  AND '2017-12-26'

```


#### SQL Keywords
Let's take a quick look at the common SQL keywords.

```not```
<br>
This keyword is used in the following queries
 - find the products that didnot catch fire
 - find the parcels that didnot lose
 
General Syntax
```
select
 a
 , b
 , c
 
from
 table1

where 
 b not in
  (
    select 
     m
    from 
     table2
  )

``` 
 
Examples
 - [not_had_fire.sql]() 




```order by```
<br>
This keyword is used to rearrange data in a specific order. Such as
 - show employee names in order of their age
 - how many customer are there from each country


```min``` function
 - How to find lowest value in a column 
 

Examples
 - find the first order from the product table


Queries in Repo
=========

The following queries are available within ```sql_queries``` directory

File Name | Description
--- | ---
wb_export.sql | sql query to export result in a csv file
case_statement.sql | example of case syntax
case_statement_2.sql | example of case syntax
group_by.sql | a table with group by syntax
inner_join.sql | basic inner join syntax
join_three_tables.sql | join three tables together
join_groupby_orderby.sql | a table with join and group by and order by

The following queries are available within ```sql_query_syntax``` directory


File Name | Description
--- | ---
substring_regex.sql | xxx
dedup_count.sql | xxx               
find_max_number.sql | xxx       
date_syntax.sql | xxx
find_gradation.sql | xxx
union.sql | xxx
ilike_similar.sql | xxx         
extract_function.sql | xxx
exists.sql | xxx                   
create_tables_inser_data.sql  | xxx
inner_join.sql | xxx           
changing_dates_to_epochs.sql  | xxx




Run & Test The Queries
===========
We can run and test any query using the following online tool
```
http://rextester.com/l/postgresql_online_compiler
```
No need to install any dependency on a local machine. Just copy any query from the 
query collection and paste it in the workpad of this tool.




Support & Disclaimer
===
#### Support
Found a bug?? Here are the options
  - Please file an issue with detailed description.
  - If you know a possible solution, please create a new brnach, update the code and then submit pull request.
  - If you would  like to reach out to me directly with any question, email me at ariful.haque.uc@gmail.com


#### General Disclaimer
This is my personal repo and not an official product of any company. If you would like to use this code, please keep it in your mind that, although I have tried to make it as error-free as possible, there's no warranty of a 100% bug free application. 


References
=========
Others
  - https://aws.amazon.com/documentation/redshift/
  - https://docs.aws.amazon.com/redshift/latest/dg/c_SQL_commands.html
  - https://docs.aws.amazon.com/redshift/latest/dg/welcome.html
  - https://aws.amazon.com/documentation/redshift/

String functions and operations
 - https://www.postgresql.org/docs/9.1/static/functions-string.html

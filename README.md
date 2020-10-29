# SQL Practices On HackerRank
This file includes my solutions to HackerRank SQL questions in MySQL

## Question List
### Basic Select - Easy
[Revising the Select Query I](#revising-the-select-query-i) | [Revising the Select Query II](#revising-the-select-query-ii) | [Select All](#select-all) | [Select By ID](#select-by-id) | [Japanese Cities' Attributes](#japanese-cities-attributes) | [Japanese Cities' Names](#japanese-cities-names) | [Weather Observation Station 1](#weather-observation-station-1) | [Weather Observation Station 3](#weather-observation-station-3) | [Weather Observation Station 4](#weather-observation-station-4) | [Weather Observation Station 5](#weather-observation-station-5) | [Weather Observation Station 6](#weather-observation-station-6) | [Weather Observation Station 7](#weather-observation-station-7) | [Weather Observation Station 8](#weather-observation-station-8) | [Weather Observation Station 9](#weather-observation-station-9) | [Weather Observation Station 10](#weather-observation-station-10) | [Weather Observation Station 11](#weather-observation-station-11) | [Weather Observation Station 12](#weather-observation-station-12) | [Higher Than 75 Marks](#higher-than-75-marks) | [Employee Names](#employee-names) | [Employee Salaries](#employee-salaries)
### Advanced Select - Easy
[Type of Triangle](#type-of-triangle)
### Advanced Select - Medium
[The PADS](#the-pads) | [Occupations](#occupations) | [Binary Tree Nodes](#binatry-tree-nodes) | [New Companies](#new-companies)
### Basic Join - Easy
Asian Population | Agfrican Cities | Average Population of Each Continent
### Basic Join - Medium
The Report | Top Competitors | Ollivander's inventory | Challenges | Contest Leaderboard
### Advanced Join - Medium
SQL Project Planning | Placements | Symmetric Pairs
### Advanced Join - Hard
Interviews | 15 Days of Learning SQL
### Aggregation - Easy
Revising Aggregation - The Count Function | Revising Aggregation - The Sum Function | Revising Aggregations - Averages | Average Population | Japan Population | Population Density Difference | The Blunder | Top Earners | Weather Observation 2 | Weather Observation Station 13 | Weather Observation Station 14 | Weather Observation Station 15 | Weather Observation Station 16 | Weather Observation Station 17
### Aggregation - Medium
Weather Observation Station 18 | Weather Observation Station 19 | Weather Observation Station 20
### Alternative Queries - Easy
Draw The Triangle 1 | Draw The Triangle 2
### Alternative Queries - Medium
Print Prime Numbers

## Solutions
#### [**Revising the Select Query I**][Revising-the-Select-Query-I]
```sql
SELECT * FROM CITY WHERE population > 100000 AND CountryCode = 'USA'
```
##### [**Back to Question List**](#question-list)
[Revising-the-Select-Query-I]:
https://www.hackerrank.com/challenges/revising-the-select-query/problem

#### [**Revising the Select Query II**][Revising-the-Select-Query-II]
```sql
SELECT name FROM CITY WHERE population > 120000 AND CountryCode = 'USA'
```
##### [**Back to Question List**](#question-list)
[Revising-the-Select-Query-II]:
https://www.hackerrank.com/challenges/revising-the-select-query-2/problem

#### [**Select All**][Select-All]
```sql
SELECT * FROM CITY
```
##### [**Back to Question List**](#question-list)
[Select-All]:
https://www.hackerrank.com/challenges/select-all-sql/problem

#### [**Select By ID**][Select-By-ID]
```sql
SELECT * FROM CITY WHERE ID = 1661
```
##### [**Back to Question List**](#question-list)
[Select-By-ID]:
https://www.hackerrank.com/challenges/select-by-id/problem

#### [**Japanese Cities' Attributes**][Japanese-Cities-Attributes]
```sql
SELECT * FROM CITY WHERE CountryCode = 'JPN'
```
##### [**Back to Question List**](#question-list)
[Japanese-Cities-Attributes]:
https://www.hackerrank.com/challenges/japanese-cities-attributes/problem

#### [**Japanese Cities' Names**][Japanese-Cities-Names]
```sql
SELECT NAME FROM CITY WHERE COUNTRYCODE = 'JPN'
```
##### [**Back to Question List**](#question-list)
[Japanese-Cities-Names]:
https://www.hackerrank.com/challenges/japanese-cities-name/problem

#### [**Weather Observation Station 1**][Weather-Observation-Station-1]
```sql
SELECT CITY, STATE FROM STATION
```
##### [**Back to Question List**](#question-list)
[Weather-Observation-Station-1]:
https://www.hackerrank.com/challenges/weather-observation-station-1/problem

#### [**Weather Observation Station 3**][Weather-Observation-Station-3]
```sql
SELECT DISTINCT CITY FROM STATION WHERE ID%2=0
```
##### [**Back to Question List**](#question-list)
[Weather-Observation-Station-3]:
https://www.hackerrank.com/challenges/weather-observation-station-3/problem

#### [**Weather Observation Station 4**][Weather-Observation-Station-4]
```sql
SELECT COUNT(CITY) - COUNT(DISTINCT CITY) FROM STATION
```
##### [**Back to Question List**](#question-list)
[Weather-Observation-Station-4]:
https://www.hackerrank.com/challenges/weather-observation-station-4/problem

#### [**Weather Observation Station 5**][Weather-Observation-Station-5]
```sql
SELECT CITY, LENGTH(CITY)
FROM STATION ORDER BY LENGTH(CITY), CITY LIMIT 1;
SELECT CITY, LENGTH(CITY)
FROM STATION ORDER BY LENGTH(CITY) DESC, CITY LIMIT 1;
```
##### [**Back to Question List**](#question-list)
[Weather-Observation-Station-5]:
https://www.hackerrank.com/challenges/weather-observation-station-5/problem

#### [**Weather Observation Station 6**][Weather-Observation-Station-6]
```sql
SELECT DISTINCT CITY FROM STATION 
WHERE CITY LIKE 'A%' OR CITY LIKE 'E%' OR 
      CITY LIKE 'I%' OR CITY LIKE 'O%' OR CITY LIKE 'U%'
```
##### [**Back to Question List**](#question-list)
[Weather-Observation-Station-6]:
https://www.hackerrank.com/challenges/weather-observation-station-6/problem

#### [**Weather Observation Station 7**][Weather-Observation-Station-7]
```sql
SELECT DISTINCT CITY
FROM STATION
WHERE CITY LIKE '%A' OR CITY LIKE '%E' OR CITY LIKE '%I' OR CITY LIKE '%O' OR CITY LIKE '%U'
```
##### [**Back to Question List**](#question-list)
[Weather-Observation-Station-7]:
https://www.hackerrank.com/challenges/weather-observation-station-7/problem

#### [**Weather Observation Station 8**][Weather-Observation-Station-8]
```sql
SELECT CITY
FROM STATION
WHERE LEFT(CITY,1) IN ('A','E','I','O','U') AND RIGHT(CITY,1) IN ('A','E','I','O','U')
```
##### [**Back to Question List**](#question-list)
[Weather-Observation-Station-8]:
https://www.hackerrank.com/challenges/weather-observation-station-8/problem

#### [**Weather Observation Station 9**][Weather-Observation-Station-9]
```sql
SELECT DISTINCT CITY FROM STATION
WHERE LEFT(CITY,1) NOT IN ('A','E','I','O','U')
```
##### [**Back to Question List**](#question-list)
[Weather-Observation-Station-9]:
https://www.hackerrank.com/challenges/weather-observation-station-9/problem

#### [**Weather Observation Station 10**][Weather-Observation-Station-10]
```sql
SELECT DISTINCT CITY FROM STATION
WHERE RIGHT(CITY,1) NOT IN ('A','E','I','O','U')
```
##### [**Back to Question List**](#question-list)
[Weather-Observation-Station-10]:
https://www.hackerrank.com/challenges/weather-observation-station-10/problem

#### [**Weather Observation Station 11**][Weather-Observation-Station-11]
```sql
SELECT DISTINCT CITY FROM STATION
WHERE LEFT(CITY,1) NOT IN ('A','E','I','O','U') OR
      RIGHT(CITY,1) NOT IN ('A','E','I','O','U')
```
##### [**Back to Question List**](#question-list)
[Weather-Observation-Station-11]:
https://www.hackerrank.com/challenges/weather-observation-station-11/problem

#### [**Weather Observation Station 12**][Weather-Observation-Station-12]
```sql
SELECT DISTINCT CITY FROM STATION
WHERE LEFT(CITY,1) NOT IN ('A','E','I','O','U') AND 
      RIGHT(CITY,1) NOT IN ('A','E','I','O','U')
```
##### [**Back to Question List**](#question-list)
[Weather-Observation-Station-12]:
https://www.hackerrank.com/challenges/weather-observation-station-12/problem

#### [**Higher Than 75 Marks**][Higher-Than-75-Marks]
```sql
SELECT NAME
FROM STUDENTS WHERE MARKS > 75
ORDER BY RIGHT(NAME,3), ID
```
##### [**Back to Question List**](#question-list)
[Higher-Than-75-Marks]:
https://www.hackerrank.com/challenges/more-than-75-marks/problem

#### [**Employee Names**][Employee-Names]
```sql
SELECT NAME FROM EMPLOYEE ORDER BY NAME
```
##### [**Back to Question List**](#question-list)
[Employee-Names]:
https://www.hackerrank.com/challenges/name-of-employees/problem

#### [**Employee Salaries**][Employee-Salaries]
```sql
SELECT NAME FROM EMPLOYEE
WHERE SALARY > 2000 AND MONTHS < 10 
ORDER BY EMPLOYEE_ID
```
##### [**Back to Question List**](#question-list)
[Employee-Salaries]:
https://www.hackerrank.com/challenges/salary-of-employees/problem

#### [**Type of Triangle**][Type-of-Triangle]
```sql
SELECT CASE
       WHEN A+B <= C OR A+C <= B OR B+C <= A THEN 'Not A Triangle'
       WHEN A=B AND B=C THEN 'Equilateral'
       WHEN A=B OR B=C OR A=C THEN 'Isosceles'
       ELSE 'Scalene' END AS KIND
FROM TRIANGLES
```
##### [**Back to Question List**](#question-list)
[Type-of-Triangle]:
https://www.hackerrank.com/challenges/what-type-of-triangle/problem

#### [**The PADS**][The-PADS]
```sql
SELECT CONCAT(NAME,'(',LEFT(OCCUPATION,1),')')
FROM OCCUPATIONS
ORDER BY NAME, OCCUPATION;
SELECT CONCAT('There are a total of ', COUNT(NAME),' ', LOWER(OCCUPATION),'s.')
FROM OCCUPATIONS
GROUP BY OCCUPATION
ORDER BY COUNT(NAME),OCCUPATION
```
##### [**Back to Question List**](#question-list)
[The-PADS]:
https://www.hackerrank.com/challenges/the-pads/problem

#### [**Binary Tree Nodes**][Binary-Tree-Nodes]
```sql
SELECT N, CASE WHEN P IS NULL THEN 'Root'
               WHEN N IN (SELECT P FROM BST) THEN 'Inner'
               ELSE 'Leaf' END AS node_type
FROM BST ORDER BY N
```
##### [**Back to Question List**](#question-list)
[Binary-Tree-Nodes]:
https://www.hackerrank.com/challenges/binary-search-tree-1/problem

#### [**New Companies**][New-Companies]
```sql
SELECT Company.company_code, founder, COALESCE(lead_manager_cnt,0), COALESCE(sr_manager_cnt,0), COALESCE(manager_cnt,0), COALESCE(employee_cnt,0)

FROM    Company,
        
        (SELECT company_code, COUNT(DISTINCT employee_code) AS employee_cnt
         FROM Employee GROUP BY company_code) AS employee_cnt, 
         
        (SELECT company_code, COUNT(DISTINCT manager_code) AS manager_cnt
         FROM Manager GROUP BY company_code) AS manager_cnt, 
         
        (SELECT company_code, COUNT(DISTINCT senior_manager_code) AS sr_manager_cnt
         FROM Senior_Manager GROUP BY company_code) AS sr_manager_cnt,
         
        (SELECT company_code, COUNT(DISTINCT lead_manager_code) AS lead_manager_cnt
         FROM Lead_Manager GROUP BY company_code) AS lead_manager_cnt
         
WHERE Company.company_code = lead_manager_cnt.company_code 
    AND Company.company_code = sr_manager_cnt.company_code
    AND Company.company_code = manager_cnt.company_code
    AND Company.company_code = employee_cnt.company_code
ORDER BY Company.company_code
```
##### [**Back to Question List**](#question-list)
[New-Companies]:
https://www.hackerrank.com/challenges/the-company/problem

#### [**Binary Tree Nodes**][Binary-Tree-Nodes]
```sql
SELECT N, CASE WHEN P IS NULL THEN 'Root'
               WHEN N IN (SELECT P FROM BST) THEN 'Inner'
               ELSE 'Leaf' END AS node_type
FROM BST ORDER BY N
```
##### [**Back to Question List**](#question-list)
[Binary-Tree-Nodes]:
https://www.hackerrank.com/challenges/binary-search-tree-1/problem

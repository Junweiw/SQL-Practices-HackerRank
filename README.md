# SQL Practices On HackerRank
This file includes my solutions to HackerRank SQL questions in MySQL or noted otherwise.

## Question List
### Basic Select - Easy
[Revising the Select Query I](#revising-the-select-query-i) | [Revising the Select Query II](#revising-the-select-query-ii) | [Select All](#select-all) | [Select By ID](#select-by-id) | [Japanese Cities' Attributes](#japanese-cities-attributes) | [Japanese Cities' Names](#japanese-cities-names) | [Weather Observation Station 1](#weather-observation-station-1) | [Weather Observation Station 3](#weather-observation-station-3) | [Weather Observation Station 4](#weather-observation-station-4) | [Weather Observation Station 5](#weather-observation-station-5) | [Weather Observation Station 6](#weather-observation-station-6) | [Weather Observation Station 7](#weather-observation-station-7) | [Weather Observation Station 8](#weather-observation-station-8) | [Weather Observation Station 9](#weather-observation-station-9) | [Weather Observation Station 10](#weather-observation-station-10) | [Weather Observation Station 11](#weather-observation-station-11) | [Weather Observation Station 12](#weather-observation-station-12) | [Higher Than 75 Marks](#higher-than-75-marks) | [Employee Names](#employee-names) | [Employee Salaries](#employee-salaries)
### Advanced Select - Easy
[Type of Triangle](#type-of-triangle)
### Advanced Select - Medium
[The PADS](#the-pads) | [Occupations](#occupations) | [Binary Tree Nodes](#binary-tree-nodes) | [New Companies](#new-companies)
### Basic Join - Easy
[Asian Population](#asian-population) | [African Cities](#african-cities) | [Average Population of Each Continent](#average-population-of-each-continent)
### Basic Join - Medium
[The Report](#the-report) | [Top Competitors](#top-competitors) | [Ollivander's inventory](#ollivanders-inventory) | [Challenges](#challenges) | [Contest Leaderboard](#contest-leaderboard)
### Advanced Join - Medium
[SQL Project Planning](#sql-project-planning) | [Placements](#placements) | [Symmetric Pairs](#symmetric-pairs)
### Advanced Join - Hard
[Interviews](#interviews) | [15 Days of Learning SQL](#15-days-of-learning-sql)
### Aggregation - Easy
[Revising Aggregations - The Count Function](#revising-aggregations---the-count-function) | [Revising Aggregations - The Sum Function](#revising-aggregations---the-sum-function) | [Revising Aggregations - Averages](#revising-aggregations---Averages) | [Average Population](#average-population) | [Japan Population](#japan-population) | [Population Density Difference](#population-density-difference) | [The Blunder](#the-blunder) | [Top Earners](#top-earners) | [Weather Observation Station 2](#weather-observation-station-2) | [Weather Observation Station 13](#weather-observation-station-13) | [Weather Observation Station 14](#weather-observation-station-14) | [Weather Observation Station 15](#weather-observation-station-15) | [Weather Observation Station 16](#weather-observation-station-16) | [Weather Observation Station 17](#weather-observation-station-17)
### Aggregation - Medium
[Weather Observation Station 18](#weather-observation-station-18) | [Weather Observation Station 19](#weather-observation-station-19) | [Weather Observation Station 20](#weather-observation-station-20)
### Alternative Queries - Easy
[Draw The Triangle 1](#draw-the-triangle-1) | [Draw The Triangle 2](#draw-the-triangle-2)

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

##### [**Back to Question List**](#question-list)
[Type-of-Triangle]:
https://www.hackerrank.com/challenges/what-type-of-triangle/problem

#### [**Occupations**][Occupations]
```sql
WITH Rows_Table AS(
SELECT DISTINCT Row_Num
FROM 
    (SELECT ROW_NUMBER() OVER(PARTITION BY Occupation ORDER BY Name) AS Row_Num FROM Occupations)T1),

Doctor AS(
SELECT ROW_NUMBER() OVER (PARTITION BY NULL ORDER BY Name) AS Row_Num, Name
FROM Occupations WHERE Occupation = 'Doctor'),

Professor AS(
SELECT ROW_NUMBER() OVER (PARTITION BY NULL ORDER BY Name) AS Row_Num, Name
FROM Occupations WHERE Occupation = 'Professor'),

Singer AS(
SELECT ROW_NUMBER() OVER (PARTITION BY NULL ORDER BY Name) AS Row_Num, Name
FROM Occupations WHERE Occupation = 'Singer'),

Actor AS(
SELECT ROW_NUMBER() OVER (PARTITION BY NULL ORDER BY Name) AS Row_Num, Name
FROM Occupations WHERE Occupation = 'Actor')

SELECT Doctor.Name, Professor.Name, Singer.Name, Actor.Name
FROM Rows_Table LEFT JOIN Doctor ON Rows_Table.Row_Num = Doctor.Row_Num
                LEFT JOIN Professor ON Rows_Table.Row_Num = Professor.Row_Num
                LEFT JOIN Singer ON Rows_Table.Row_Num = Singer.Row_Num
                LEFT JOIN Actor ON Rows_Table.Row_Num = Actor.Row_Num
```
##### [**Back to Question List**](#question-list)
[Occupations]:
https://www.hackerrank.com/challenges/occupations/problem

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

#### [**Asian Population**][Asian-Population]
```sql
# Solution 1
SELECT SUM(City.population)
FROM City, Country
WHERE City.Countrycode = Country.Code AND Country.Continent = 'Asia'
```

```sql
# Solution 2
SELECT SUM(City.population)
FROM City LEFT JOIN Country
ON City.Countrycode = Country.Code
WHERE Country.Continent = 'Asia'
```
##### [**Back to Question List**](#question-list)
[Asian-Population]:
https://www.hackerrank.com/challenges/asian-population/problem

#### [**African Cities**][African-Cities]
```sql
# Solution 1
SELECT City.Name
FROM City, Country
WHERE City.CountryCode = Country.Code AND Country.Continent = 'Africa'
```

```sql
# Solution 2
SELECT City.Name
FROM City LEFT JOIN Country
ON City.CountryCode = Country.Code
WHERE Country.Continent = 'Africa'
```
##### [**Back to Question List**](#question-list)
[African-Cities]:
https://www.hackerrank.com/challenges/african-cities/problem

#### [**Average Population of Each Continent**][Average-Population-of-Each-Continent]
```sql
# Solution 1
SELECT Country.Continent, FLOOR(SUM(City.population)/COUNT(City.name))
FROM City, Country
WHERE City.CountryCode = Country.Code
GROUP BY Country.Continent
```

```sql
# Solution 2
SELECT Country.Continent, FLOOR(SUM(City.Population)/Count(City.Name))
FROM City INNER JOIN Country
ON City.CountryCode = Country.Code
GROUP BY Country.Continent
```
##### [**Back to Question List**](#question-list)
[Average-Population-of-Each-Continent]:
https://www.hackerrank.com/challenges/average-population-of-each-continent/problem

#### [**The Report**][The-Report]
```sql
# Solution 1
SELECT CASE WHEN grades >= 8 THEN name ELSE NULL END AS name, grades, marks
FROM
    (SELECT id, name, marks, CASE WHEN marks < 100 THEN CEIL((marks+1)/10) ELSE 10 END AS grades
     FROM Students)T1
ORDER BY grades DESC, name, marks
```

```sql
# Solution 2
SELECT CASE WHEN Grades.grade >= 8 THEN Students.name ELSE NULL END AS name, Grades.grade, Students.marks
FROM Students, Grades
WHERE Students.Marks BETWEEN Min_Mark AND Max_Mark
ORDER BY Grades.grade DESC, name, Students.marks
```
##### [**Back to Question List**](#question-list)
[The-Report]:
https://www.hackerrank.com/challenges/the-report/problem

#### [**Top Competitors**][Top-Competitors]
```sql
SELECT T2.hacker_id, Hackers.name
FROM 
   (SELECT T1.hacker_id, COUNT(DISTINCT T1.challenge_id) AS challenge_count
    FROM
        (SELECT Submissions.hacker_id, Submissions.challenge_id
         FROM Submissions LEFT JOIN
             (SELECT Difficulty.score AS full_score, challenges.Challenge_id
              FROM Challenges LEFT JOIN Difficulty
              ON Challenges.difficulty_level = Difficulty.difficulty_level) Challenge_score
         ON Submissions.challenge_id = Challenge_score.challenge_id 
         WHERE Submissions.score = Challenge_score.full_score)T1
    GROUP BY T1.hacker_id     
    HAVING COUNT(DISTINCT challenge_id) > 1)T2
    LEFT JOIN Hackers ON T2.hacker_id = Hackers.hacker_id
ORDER BY T2.challenge_count DESC, T2.hacker_id
```
##### [**Back to Question List**](#question-list)
[Top-Competitors]:
https://www.hackerrank.com/challenges/full-score/problem

#### [**Ollivander's Inventory**][Ollivander's-Inventory]
```sql
# Solution 1
SELECT Wands.id, T1.age, T1.min_coins, T1.power
FROM 
   (SELECT MIN(coins_needed) AS min_coins, Wands_Property.age, Wands.power, Wands_Property.code
    FROM Wands LEFT JOIN Wands_Property
    ON Wands.code = Wands_Property.code
    WHERE Wands_Property.is_evil = 0
    GROUP BY Wands_Property.age, Wands.power, Wands_Property.code)T1
LEFT JOIN Wands
ON Wands.coins_needed = T1.min_coins AND Wands.power = T1.power AND Wands.code = T1.code
ORDER BY Wands.power DESC, T1.age DESC
```

```sql
# Solution 2
SELECT id, age, min_coins, power
FROM
    (SELECT Wands.id, MIN(Wands.coins_needed) OVER(PARTITION BY Wands_Property.age, Wands.power) AS min_coins, Wands.coins_needed, Wands_Property.age, Wands.power
     FROM Wands LEFT JOIN Wands_Property
     ON Wands.code = Wands_Property.code
     WHERE Wands_Property.is_evil = 0)T1
WHERE min_coins = coins_needed
ORDER BY power DESC, age DESC
```
##### [**Back to Question List**](#question-list)
[Ollivander's-Inventory]:
https://www.hackerrank.com/challenges/harry-potter-and-wands/problem

#### [**Challenges**][Challenges]
```sql
# Using MS SQL
WITH Challenge_counts AS(
SELECT Hackers.hacker_id, name, COALESCE(challenge_cnt,0) AS challenge_cnt
FROM Hackers LEFT JOIN
    (SELECT hacker_id, COUNT(challenge_id) AS challenge_cnt
     FROM Challenges
     GROUP BY hacker_id)T1
ON Hackers.hacker_id = T1.hacker_id),

Challenge_counts_max AS(
SELECT hacker_id, name, challenge_cnt, MAX(challenge_cnt) OVER (PARTITION BY NULL) AS max_challenge, COUNT(hacker_id) OVER (PARTITION BY challenge_cnt) AS hacker_per_challenge
FROM Challenge_counts)

SELECT hacker_id, name, challenge_cnt
FROM Challenge_counts_max
WHERE challenge_cnt = max_challenge OR hacker_per_challenge = 1
ORDER BY challenge_cnt DESC, hacker_id
```
##### [**Back to Question List**](#question-list)
[Challenges]:
https://www.hackerrank.com/challenges/challenges/problem

#### [**Contest Leaderboard**][Contest-Leaderboard]
```sql
SELECT Hackers.hacker_id, name, tot_scores
FROM Hackers LEFT JOIN
   (SELECT hacker_id, SUM(max_scores) AS tot_scores
    FROM
        (SELECT hacker_id, challenge_id, MAX(score) AS max_scores
         FROM Submissions
         GROUP BY hacker_id, challenge_id)T1
    GROUP BY hacker_id)T2
ON Hackers.hacker_id = T2.hacker_id
WHERE tot_scores >0
ORDER BY tot_scores DESC, Hackers.hacker_id
```
##### [**Back to Question List**](#question-list)
[Contest-Leaderboard]:
https://www.hackerrank.com/challenges/contest-leaderboard/problem

#### [**SQL Project Planning**][SQL-Project-Planning]
```sql
# Solution 1 in MS SQL
WITH Project_Dates AS(
    SELECT Task_Date, ROW_NUMBER()OVER(PARTITION BY NULL ORDER BY Task_Date) AS Row_Number
    FROM  (SELECT Task_Date
           FROM
            (SELECT DISTINCT Start_Date AS Task_Date
             FROM Projects
             UNION ALL
             SELECT DISTINCT End_Date AS Task_date
             FROM Projects)T1
           GROUP BY Task_Date
           HAVING COUNT(Task_Date) =1)T2),
    
    Start_End_Dates AS(
    SELECT Start_Date, End_Date, DATEDIFF(day,Start_Date, End_Date) AS Completion_Days
    FROM 
        (SELECT Task_Date AS Start_Date, Row_Number
         FROM Project_Dates
         WHERE Row_Number % 2 = 1)Start_D,
        (SELECT Task_Date AS End_Date, Row_Number
         FROM Project_Dates
         WHERE Row_number % 2 = 0)End_D
    WHERE Start_D.Row_Number = End_D.Row_number - 1)
    
SELECT Start_Date, End_Date
FROM Start_End_Dates
ORDER BY Completion_Days, Start_Date
```

```sql
# Solution 2 in MySQL
SELECT start_date, MIN(end_date)
FROM 
    (SELECT start_date FROM projects WHERE start_date NOT IN (SELECT end_date FROM projects)) Start_D,
    (SELECT end_date FROM projects WHERE end_date NOT IN (SELECT start_date FROM projects)) End_D
WHERE Start_D.start_date < End_D.end_date
GROUP BY Start_D.start_date
ORDER BY DATEDIFF(MIN(end_date), start_date), start_date
```
##### [**Back to Question List**](#question-list)
[SQL-Project-Planning]:
https://www.hackerrank.com/challenges/sql-projects/problem

#### [**Placements**][Placements]
```sql
SELECT Students.Name
FROM
    (SELECT Friends.ID, Packages.Salary AS Salary
     FROM Friends LEFT JOIN Packages
     ON Friends.ID = Packages.ID)T1
    LEFT JOIN
    (SELECT Friends.ID, Packages.Salary AS Friends_Salary
     FROM Friends LEFT JOIN Packages
     ON Friends.Friend_ID = Packages.ID)T2
    ON T1.ID = T2.ID
    LEFT JOIN Students
    ON T1.ID = Students.ID
WHERE T1.Salary < T2.Friends_Salary
ORDER BY T2.Friends_Salary
```
##### [**Back to Question List**](#question-list)
[Placements]:
https://www.hackerrank.com/challenges/placements/problem

#### [**Symmetric Pairs**][Symmetric-Pairs]
```sql
SELECT T1.X, T1.Y
FROM Functions AS T1, Functions AS T2
WHERE T1.X = T2.Y AND T1.Y = T2.X
GROUP BY T1.X, T1.Y
HAVING COUNT(*)>1 OR T1.X < T1.Y
ORDER BY T1.X, T1.Y
```
##### [**Back to Question List**](#question-list)
[Symmetric-Pairs]:
https://www.hackerrank.com/challenges/symmetric-pairs/problem

#### [**Interviews**][Interviews]
```sql
# Solution 1 in MySQL
SELECT Contests.contest_id, Contests.hacker_id, Contests.name,
       contest_level.sum_sub, contest_level.sum_acc_sub, contest_level.sum_views,
       contest_level.sum_uni_views
FROM Contests LEFT JOIN
    (SELECT contest_id, SUM(tot_sub) AS sum_sub, SUM(tot_acc_sub) AS sum_acc_sub, 
            SUM(tot_views) AS sum_views, SUM(tot_uni_views) AS sum_uni_views
     FROM Colleges
     LEFT JOIN 
        (SELECT College_id, SUM(submission_challenge_level.total_submissions) AS tot_sub,
                SUM(submission_challenge_level.total_accepted_submissions) AS tot_acc_sub,
                SUM(view_challenge_level.total_views) AS tot_views, 
                SUM(view_challenge_level.total_unique_views) AS tot_uni_views
         FROM Challenges
            LEFT JOIN (SELECT challenge_id, 
                              SUM(total_views) AS total_views,
                              SUM(total_unique_views) AS total_unique_views 
                       FROM View_Stats
                       GROUP BY challenge_id) AS view_challenge_level
            ON Challenges.challenge_id = view_challenge_level.challenge_id 
            LEFT JOIN (SELECT challenge_id, 
                              SUM(total_submissions) AS total_submissions,
                              SUM(total_accepted_submissions) AS total_accepted_submissions
                       FROM Submission_stats
                       GROUP BY challenge_id) AS submission_challenge_level
            ON Challenges.challenge_id = submission_challenge_level.challenge_id
         GROUP BY College_id) college_level
     ON Colleges.college_id = college_level.college_id
     GROUP BY contest_id) contest_level
ON Contests.contest_id = contest_level.contest_id
WHERE contest_level.sum_sub +
      contest_level.sum_acc_sub +
      contest_level.sum_views +
      contest_level.sum_uni_views > 0
ORDER BY contest_id
```

```sql
#Solution 2 in MS SQL
WITH sum_views AS(
SELECT challenge_id, SUM(COALESCE(total_views,0)) AS total_views, 
       SUM(COALESCE(total_unique_views, 0)) AS tot_unique_views
FROM View_Stats GROUP BY challenge_id),

sum_submission AS(
SELECT challenge_id, SUM(COALESCE(total_submissions,0)) AS tott_submissions, SUM(COALESCE(total_accepted_submissions,0)) AS tot_accepted_submissions
FROM Submission_Stats GROUP BY challenge_id),

sum_contests AS(
SELECT contest_id, SUM(total_views) AS sum_views, 
       SUM(tot_unique_views) AS sum_tot_unique_views, 
       SUM(tott_submissions) AS sum_tot_submissions, 
       SUM(tot_accepted_submissions) AS sum_tot_accepted_submissions
FROM challenges LEFT JOIN sum_views ON challenges.challenge_id = sum_views.challenge_id
                LEFT JOIN sum_submission ON challenges.challenge_id = sum_submission.challenge_id
                LEFT JOIN colleges ON challenges.college_id = colleges.college_id
GROUP BY contest_id)
                
SELECT Contests.contest_id, hacker_id, name, sum_tot_submissions, sum_tot_accepted_submissions, sum_views, sum_tot_unique_views
FROM Contests LEFT JOIN sum_contests ON Contests.contest_id = sum_contests.contest_id
WHERE sum_tot_submissions + sum_tot_accepted_submissions + sum_views + sum_tot_unique_views > 0
```
##### [**Back to Question List**](#question-list)
[Interviews]:
https://www.hackerrank.com/challenges/interviews/problem

#### [**15 Days of Learning SQL**][15 Days of Learning SQL]
```sql
WITH fifteen_days AS(
    SELECT hacker_id, submission_date, daily_submissions, 
           MAX(daily_submissions) OVER(PARTITION BY submission_date) AS max_daily_submission,
           DENSE_RANK()OVER(ORDER BY submission_date) AS submission_order_date,
           ROW_NUMBER()OVER(PARTITION BY hacker_id ORDER BY submission_date) AS submission_order_hacker
    FROM
          (SELECT hacker_id, submission_date, COUNT(submission_id) AS daily_submissions
           FROM Submissions
           GROUP BY hacker_id, submission_date)T1)

SELECT uni_hackers.submission_date, uni_hackers.hacker_per_date, max_submissions.min_hacker_id, Hackers.name
FROM
    (SELECT COUNT(hacker_id) AS hacker_per_date, submission_date
     FROM fifteen_days
     WHERE submission_order_date = submission_order_hacker
     GROUP BY submission_date) uni_hackers
LEFT JOIN 
    (SELECT MIN(hacker_id) AS min_hacker_id, submission_date
     FROM fifteen_days
     WHERE daily_submissions = max_daily_submission
     GROUP BY submission_date) max_submissions
ON uni_hackers.submission_date = max_submissions.submission_date
LEFT JOIN Hackers
ON max_submissions.min_hacker_id = Hackers.hacker_id
ORDER BY uni_hackers.submission_date
```
##### [**Back to Question List**](#question-list)
[15 Days of Learning SQL]:
https://www.hackerrank.com/challenges/15-days-of-learning-sql/problem

#### [**Revising Aggregations - The Count Function**][Revising Aggregations - The Count Function]
```sql
SELECT COUNT(ID)
FROM CITY
WHERE POPULATION > 100000
```
##### [**Back to Question List**](#question-list)
[Revising Aggregations - The Count Function]:
https://www.hackerrank.com/challenges/revising-aggregations-the-count-function/problem

#### [**Revising Aggregations - The Sum Function**][Revising Aggregations - The Sum Function]
```sql
SELECT SUM(POPULATION)
FROM CITY WHERE DISTRICT = 'California'
```
##### [**Back to Question List**](#question-list)
[Revising Aggregations - The Sum Function]:
https://www.hackerrank.com/challenges/revising-aggregations-the-sum-function/problem

#### [**Revising Aggregations - Averages**][Revising Aggregations - Averages]
```sql
SELECT AVG(POPULATION)
FROM CITY WHERE DISTRICT = 'California'
```
##### [**Back to Question List**](#question-list)
[Revising Aggregations - Averages]:
https://www.hackerrank.com/challenges/revising-aggregations-the-average-function/problem

#### [**Average Population**][Average Population]
```sql
SELECT ROUND(AVG(POPULATION),0) FROM CITY
```
##### [**Back to Question List**](#question-list)
[Average Population]:
https://www.hackerrank.com/challenges/average-population/problem

#### [**Japan Population**][Japan Population]
```sql
SELECT SUM(POPULATION) FROM CITY WHERE COUNTRYCODE = 'JPN'
```
##### [**Back to Question List**](#question-list)
[Japan Population]:
https://www.hackerrank.com/challenges/japan-population/problem

#### [**Population Density Difference**][Population Density Difference]
```sql
SELECT MAX(POPULATION) - MIN(POPULATION) FROM CITY
```
##### [**Back to Question List**](#question-list)
[Population Density Difference]:
https://www.hackerrank.com/challenges/population-density-difference/problem

#### [**The Blunder**][The Blunder]
```sql
SELECT CEIL(AVG(Salary) - AVG(REPLACE(Salary,0,''))) FROM Employees
```
##### [**Back to Question List**](#question-list)
[The Blunder]:
https://www.hackerrank.com/challenges/the-blunder/problem

#### [**Top Earners**][Top Earners]
```sql
# Solution 1
SELECT months * salary, COUNT(employee_id)
FROM Employee
GROUP BY months * salary ORDER BY months * salary DESC LIMIT 1
```

```sql
# Solution 2
SELECT MIN(max_earning), SUM(CASE max_earning WHEN months * salary THEN 1 ELSE 0 END)
FROM Employee, 
    (SELECT MAX(months * salary) AS max_earning FROM Employee) AS T1
```
##### [**Back to Question List**](#question-list)
[Top Earners]:
https://www.hackerrank.com/challenges/earnings-of-employees/problem

#### [**Weather Observation Station 2**][Weather Observation Station 2]
```sql
SELECT ROUND(SUM(LAT_N),2) AS lat, ROUND(SUM(LONG_W),2) AS lon FROM STATION
```
##### [**Back to Question List**](#question-list)
[Weather Observation Station 2]:
https://www.hackerrank.com/challenges/weather-observation-station-2/problem

#### [**Weather Observation Station 13**][Weather Observation Station 13]
```sql
SELECT TRUNCATE(SUM(LAT_N),4)
FROM STATION WHERE LAT_N > 38.788 AND LAT_N < 137.2345
```
##### [**Back to Question List**](#question-list)
[Weather Observation Station 13]:
https://www.hackerrank.com/challenges/weather-observation-station-13/problem

#### [**Weather Observation Station 14**][Weather Observation Station 14]
```sql
SELECT TRUNCATE(MAX(LAT_N),4) FROM STATION WHERE LAT_N < 137.2345
```
##### [**Back to Question List**](#question-list)
[Weather Observation Station 14]:
https://www.hackerrank.com/challenges/weather-observation-station-14/problem

#### [**Weather Observation Station 15**][Weather Observation Station 15]
```sql
SELECT ROUND(LONG_W,4) FROM STATION WHERE LAT_N < 137.2345 ORDER BY LAT_N DESC LIMIT 1
```
##### [**Back to Question List**](#question-list)
[Weather Observation Station 15]:
https://www.hackerrank.com/challenges/weather-observation-station-15/problem

#### [**Weather Observation Station 16**][Weather Observation Station 16]
```sql
SELECT ROUND(MIN(LAT_N),4) FROM STATION WHERE LAT_N > 38.7780
```
##### [**Back to Question List**](#question-list)
[Weather Observation Station 16]:
https://www.hackerrank.com/challenges/weather-observation-station-16/problem

#### [**Weather Observation Station 17**][Weather Observation Station 17]
```sql
SELECT ROUND(LONG_W, 4) FROM STATION WHERE LAT_N > 38.7780 ORDER BY LAT_N LIMIT 1
```
##### [**Back to Question List**](#question-list)
[Weather Observation Station 17]:
https://www.hackerrank.com/challenges/weather-observation-station-17/problem

#### [**Weather Observation Station 18**][Weather Observation Station 18]
```sql
SELECT ROUND(MAX(LAT_N)-MIN(LAT_N) + MAX(LONG_W)-MIN(LONG_W),4) FROM STATION
```
##### [**Back to Question List**](#question-list)
[Weather Observation Station 18]:
https://www.hackerrank.com/challenges/weather-observation-station-18/problem

#### [**Weather Observation Station 19**][Weather Observation Station 19]
```sql
SELECT ROUND(
             SQRT(POWER(MAX(LAT_N)-MIN(LAT_N), 2)
            +POWER(MAX(LONG_W)-MIN(LONG_W), 2))
            ,4)
FROM STATION
```
##### [**Back to Question List**](#question-list)
[Weather Observation Station 19]:
https://www.hackerrank.com/challenges/weather-observation-station-19/problem

#### [**Weather Observation Station 20**][Weather Observation Station 20]
```sql
SELECT ROUND(AVG(LAT_N), 4)
FROM (SELECT ROW_NUMBER() OVER(PARTITION BY NULL ORDER BY LAT_N DESC) AS ROW_NUM, 
      COUNT(LAT_N) OVER(PARTITION BY NULL) AS TOT_ROWS, LAT_N
      FROM STATION ORDER BY LAT_N) T1
WHERE ROW_NUM = CASE WHEN TOT_ROWS%2=0 THEN TOT_ROWS/2 ELSE CEIL(TOT_ROWS/2) END OR
      ROW_NUM = CASE WHEN TOT_ROWS%2=0 THEN TOT_ROWS/2 + 1 ELSE CEIL(TOT_ROWS/2) END
```
##### [**Back to Question List**](#question-list)
[Weather Observation Station 20]:
https://www.hackerrank.com/challenges/weather-observation-station-20/problem

#### [**Draw The Triangle 1**][Draw The Triangle 1]
```sql
SET @i = 21;
SELECT REPEAT('* ', @i := @i - 1) FROM 
    (SELECT 1 UNION SELECT 2 UNION SELECT 3) a, 
    (SELECT 1 UNION SELECT 2 UNION SELECT 3) b,
    (SELECT 1 UNION SELECT 2 UNION SELECT 3) c;
```
##### [**Back to Question List**](#question-list)
[Draw The Triangle 1]:
https://www.hackerrank.com/challenges/draw-the-triangle-1/problem

#### [**Draw The Triangle 2**][Draw The Triangle 2]
```sql
SET @i = 0;
SELECT REPEAT('* ', @i := @i + 1) FROM 
    (SELECT 1 UNION SELECT 2 UNION SELECT 3) a, 
    (SELECT 1 UNION SELECT 2 UNION SELECT 3) b,
    (SELECT 1 UNION SELECT 2 UNION SELECT 3) c
LIMIT 20;
```
##### [**Back to Question List**](#question-list)
[Draw The Triangle 2]:
https://www.hackerrank.com/challenges/draw-the-triangle-2/problem

# SQLBOLT-SAMSON-ALEX
## **SQLBOLT REVIEW 1**
1. List all the Canadian cities and their populations <br/>
`SELECT CITY, POPULATION FROM north_american_cities` <br/>
`WHERE COUNTRY = "Canada";`

2. Order all the cities in the United States by their latitude from north to south <br/>
`SELECT CITY FROM north_american_cities` <br/>
`WHERE COUNTRY = "United States"` <br/>
`ORDER BY LATITUDE DESC; `

3. List all the cities west of Chicago, ordered from west to east <br/>
`SELECT CITY FROM north_american_cities` <br/>
`WHERE LONGITUDE < -87.629798` <br/>
`ORDER BY LONGITUDE ASC;` 

4. List the two largest cities in Mexico (by population) <br/>
`SELECT CITY, POPULATION FROM north_american_cities` <br/>
`WHERE COUNTRY LIKE "Mexico"` <br/>
`ORDER BY POPULATION DESC` <br/>
`LIMIT 2;`

5. List the third and fourth largest cities (by population) in the United States and their population <br/>
`SELECT CITY, POPULATION FROM north_american_cities` <br/>
`WHERE COUNTRY LIKE "United States"` <br/>
`ORDER BY POPULATION DESC` <br/>
`LIMIT 2 OFFSET 2;`



## **SQLBOLT Exercise 12**
1. Find the number of movies each director has directed <br/>
`SELECT DIRECTOR, COUNT(ID) AS Movie_Count` <br/>
`FROM MOVIES` <br/>
`GROUP BY DIRECTOR;`

2. Find the total domestic and international sales that can be attributed to each director <br/>
`SELECT DIRECTOR, SUM(DOMESTIC_SALES + INTERNATIONAL_SALES) AS Total_Sales` <br/>
`FROM MOVIES` <br/>
`    INNER JOIN BOXOFFICE` <br/>
`        ON MOVIES.ID = BOXOFFICE.MOVIE_ID` <br/>
`GROUP BY DIRECTOR;`




## **SQLPD**
1. A mailing list of an illegal online service was sent to the SQLPD hot-line. Please submit all entries' details. <br/>
`SELECT *` <br/>
`FROM mailing_list;` 

2. A mailing list of an illegal online service was sent to the SQLPD hot-line. Please submit all records' details. <br/>
`SELECT *` <br/>
`FROM mailing_list;` 

3. An illegal site's servers were seized in a recent operation. Please submit all users given names and last access times' details. <br/>
`SELECT GivenName, LastAccess` <br/>
`FROM users;`

4. An illegal site's servers were seized in a recent operation. Please submit all users number of downloads and first names' details. <br/>
`SELECT Downloads, FirstName` <br/>
`FROM users;`

5. An illegal site's servers were seized in a recent operation. Please submit all users email addresses' details. Please make sure there are no duplicates. <br/>
`SELECT DISTINCT EmailAddress` <br/>
`FROM users;`

6. White hat hacker has sent SQLPD exposed members' details of a shady site connected to various persons of interest. Please submit all members' details sorted by usernames in ascending order. <br/>
`SELECT *` <br/>
`FROM members` <br/>
`ORDER BY Username ASC;`

7. A hacked site subscribers' details have surfaced on a darknet forum. Please submit all subscribers' details sorted by mailing addresses in descending order. <br/>
`SELECT *` <br/>
`FROM subscribers` <br/>
`ORDER BY MailingAddress DESC;`

8. A mailing list of an illegal online service was sent to the SQLPD hot-line. Please submit all entries join dates, email addresses and number of kids' details sorted by email addresses in descending order. Please make sure there are no duplicates. <br/>
`SELECT DISTINCT Joined, EmailAddress, NumberOfKids` <br/>
`FROM mailing_list` <br/>
`ORDER BY EmailAddress DESC;`

9. A mailing list of an illegal online service was sent to the SQLPD hot-line. Please submit all records number of promotions sent, join dates and surnames' details sorted by number of promotions sent in descending order and then by join dates in ascending order. <br/>
`SELECT Promotions, Joined, Surname` <br/>
`FROM mailing_list` <br/>
`ORDER BY Promotions DESC, Joined ASC;`

10. White hat hacker has sent SQLPD exposed subscribers' details of a shady site connected to various persons of interest. Please submit the top 10 subscribers' details when sorted by names in ascending order and then by hashed passwords in descending order. <br/>
`SELECT *` <br/>
`FROM subscribers` <br/>
`ORDER BY Name ASC, HashedPassword DESC` <br/>
`LIMIT 10;`

11. A mailing list of an illegal online service was sent to the SQLPD hot-line. Please submit the top 5 entries first names and number of kids' details when sorted by first names in ascending order and then by number of kids in ascending order. Please make sure there are no duplicates. <br/>
`SELECT DISTINCT FirstName, NumberOfKids` <br/>
`FROM mailing_list` <br/>
`ORDER BY FirstName ASC, NumberOfKids ASC` <br/>
`LIMIT 5;`


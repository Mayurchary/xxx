Query the list of CITY names from STATION which have vowels (i.e., a, e, i, o, and u) as both their first and last characters. Your result cannot contain duplicates.

SELECT DISTINCT city FROM station WHERE REGEXP_LIKE(LOWER(city), '^[aeiou].*[aeiou]$');

Query the list of CITY names from STATION that do not start with vowels. Your result cannot contain duplicates.
SELECT DISTINCT city FROM station WHERE not REGEXP_LIKE(LOWER(city), '^[aeiou].');



Query the list of CITY names from STATION that do not end with vowels. Your result cannot contain duplicates.

SELECT DISTINCT city FROM station WHERE not REGEXP_LIKE(LOWER(city), '[aeiou]$');

Query the list of CITY names from STATION that do not start with vowels and do not end with vowels. Your result cannot contain duplicates.
SELECT DISTINCT city FROM station WHERE not REGEXP_LIKE(LOWER(city), '[aeiou]$') and not REGEXP_LIKE(LOWER(city), '^[aeiou].');


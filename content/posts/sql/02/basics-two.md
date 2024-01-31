---
title: "SQL Basics Two"
date: 2022-05-21T12:14:49+05:30
tags: ["SQL"]
categories: ["SQL"]
---

## SELECT FROM

Fetch all the records in the table, here `*` will refer to the all columns in the table

```sql
SELECT * FROM person;

```

```sql
  id  |   first_name   |   last_name    |                email                |   gender    | date_of_birth 
------+----------------+----------------+-------------------------------------+-------------+---------------
    1 | Adrianna       | Rottgers       | arottgers0@psu.edu                  | Female      | 2021-06-21
    2 | Conrade        | Chatenet       | cchatenet1@prweb.com                | Male        | 2022-02-05
    3 | Caddric        | Kynvin         | ckynvin2@tmall.com                  | Male        | 2021-05-30
    4 | Vanya          | Kitchingman    |                                     | Female      | 2021-10-10
    5 | Hamilton       | Harrild        |                                     | Male        | 2021-10-13
    6 | Chloette       | Ferruzzi       | cferruzzi5@addtoany.com             | Female      | 2022-02-21
    7 | Gardener       | Sharply        |                                     | Male        | 2021-06-07
    8 | Burlie         | Crippes        | bcrippes7@instagram.com             | Male        | 2021-08-04
    9 | Amalle         | Fudge          |                                     | Genderfluid | 2022-04-19
   10 | Misha          | Blanchflower   |                                     | Female      | 2022-02-24
   11 | Christie       | Antonik        |                                     | Female      | 2021-10-21
   12 | Kerrill        | Perren         | kperrenb@theatlantic.com            | Female      | 2021-07-25
   13 | Ashleigh       | Tregenna       | atregennac@webeden.co.uk            | Female      | 2022-01-20
   14 | Victor         | Embling        | vemblingd@canalblog.com             | Male        | 2022-05-03
   15 | Konstantine    | Penke          | kpenkee@npr.org                     | Male        | 2022-05-18
   16 | Twyla          | Hinz           | thinzf@paginegialle.it              | Female      | 2021-07-20
   17 | Tiphanie       | Loudiane       | tloudianeg@wunderground.com         | Female      | 2021-10-27
   18 | Layney         | Faherty        | lfahertyh@miitbeian.gov.cn          | Female      | 2022-02-23
   19 | Loren          | Sheldon        |                                     | Bigender    | 2021-09-20
   20 | Edgardo        | Drewett        | edrewettj@mysql.com                 | Male        | 2022-01-26
   21 | Baird          | MacDougal      | bmacdougalk@toplist.cz              | Male        | 2022-03-16

```

Fethc specific column records

```sql
SELECT first_name, last_name FROM person;

```

```sql

   first_name   |   last_name    
----------------+----------------
 Adrianna       | Rottgers
 Conrade        | Chatenet
 Caddric        | Kynvin
 Vanya          | Kitchingman
 Hamilton       | Harrild
 Chloette       | Ferruzzi
 Gardener       | Sharply
 Burlie         | Crippes
 Amalle         | Fudge
 Misha          | Blanchflower
 Christie       | Antonik
 Kerrill        | Perren
 Ashleigh       | Tregenna
 Victor         | Embling
 Konstantine    | Penke
 Twyla          | Hinz
 Tiphanie       | Loudiane
 Layney         | Faherty
 Loren          | Sheldon
 Edgardo        | Drewett
 Baird          | MacDougal

```

## ORDER BY

`ORDER BY `keyword takes a column and orders the results we get back `ASCENDING` or `DECENDING` order

```sql
SELECT * FROM person ORDER BY first_name;

```

```sql
  id  |   first_name   |   last_name    |                email                |   gender    | date_of_birth 
------+----------------+----------------+-------------------------------------+-------------+---------------
  940 | Ab             | Dransfield     | adransfieldq3@hugedomains.com       | Male        | 2022-04-18
  113 | Abbe           | Haquard        |                                     | Female      | 2022-04-06
  250 | Abbi           | Lillistone     |                                     | Female      | 2021-07-02
  754 | Abbie          | Grafton        | agraftonkx@macromedia.com           | Male        | 2021-10-31
  344 | Abel           | Pardoe         |                                     | Male        | 2021-06-23
  697 | Abel           | Digginson      | adigginsonjc@blogspot.com           | Male        | 2022-03-20
  897 | Adair          | Gilbane        |                                     | Male        | 2021-12-06
  996 | Adel           | Sottell        | asottellrn@chicagotribune.com       | Female      | 2021-11-03
  932 | Adelaida       | Edon           | aedonpv@home.pl                     | Female      | 2021-08-30

```

By default order is `ASCENDING` that's why we din't see any change here above table and this table

```sql
SELECT * FROM person ORDER BY first_name ASC;

```

```sql
  id  |   first_name   |   last_name    |                email                |   gender    | date_of_birth 
------+----------------+----------------+-------------------------------------+-------------+---------------
  940 | Ab             | Dransfield     | adransfieldq3@hugedomains.com       | Male        | 2022-04-18
  113 | Abbe           | Haquard        |                                     | Female      | 2022-04-06
  250 | Abbi           | Lillistone     |                                     | Female      | 2021-07-02
  754 | Abbie          | Grafton        | agraftonkx@macromedia.com           | Male        | 2021-10-31
  344 | Abel           | Pardoe         |                                     | Male        | 2021-06-23
  697 | Abel           | Digginson      | adigginsonjc@blogspot.com           | Male        | 2022-03-20
  897 | Adair          | Gilbane        |                                     | Male        | 2021-12-06
  996 | Adel           | Sottell        | asottellrn@chicagotribune.com       | Female      | 2021-11-03
  932 | Adelaida       | Edon           | aedonpv@home.pl                     | Female      | 2021-08-30

```

`DECENDING ORDER`

```sql
SELECT * FROM person ORDER BY first_name DESC;

```

```sql
  id  |   first_name   |   last_name    |                email                |   gender    | date_of_birth 
------+----------------+----------------+-------------------------------------+-------------+---------------
  794 | Zilvia         | Kamienski      | zkamienskim1@marketwatch.com        | Female      | 2021-08-22
  171 | Zed            | Scamaden       | zscamaden4q@census.gov              | Male        | 2022-05-15
  616 | Zebedee        | Bernardini     | zbernardinih3@nhs.uk                | Male        | 2021-08-07
  956 | Zarla          | Fear           |                                     | Female      | 2021-10-06
  224 | Zack           | Stansfield     | zstansfield67@goo.gl                | Male        | 2021-10-02
  361 | Zacharie       | Ringwood       | zringwooda0@shinystat.com           | Male        | 2021-08-17
  265 | Yolane         | Goldis         | ygoldis7c@aol.com                   | Female      | 2022-04-11
  254 | Yolanda        | Billson        |                                     | Female      | 2021-09-27
  510 | Yolanda        | Maciocia       |                                     | Genderqueer | 2021-06-19
  335 | Yoko           | Reaper         |                                     | Female      | 2021-08-10
  598 | Yetta          | Slinger        |                                     | Female      | 2021-11-10

```

## WHERE clause and AND

`WHERE` keyword allows us to filter the data based on the conditions

```sql
SELECT * FROM person WHERE gender = "Female" ;

```

```sql
 id  |   first_name   |   last_name   |                email                | gender | date_of_birth 
-----+----------------+---------------+-------------------------------------+--------+---------------
   1 | Adrianna       | Rottgers      | arottgers0@psu.edu                  | Female | 2021-06-21
   4 | Vanya          | Kitchingman   |                                     | Female | 2021-10-10
   6 | Chloette       | Ferruzzi      | cferruzzi5@addtoany.com             | Female | 2022-02-21
  10 | Misha          | Blanchflower  |                                     | Female | 2022-02-24
  11 | Christie       | Antonik       |                                     | Female | 2021-10-21
  12 | Kerrill        | Perren        | kperrenb@theatlantic.com            | Female | 2021-07-25
  13 | Ashleigh       | Tregenna      | atregennac@webeden.co.uk            | Female | 2022-01-20
  16 | Twyla          | Hinz          | thinzf@paginegialle.it              | Female | 2021-07-20
  17 | Tiphanie       | Loudiane      | tloudianeg@wunderground.com         | Female | 2021-10-27
  18 | Layney         | Faherty       | lfahertyh@miitbeian.gov.cn          | Female | 2022-02-23
  22 | Hulda          | Galland       |                                     | Female | 2021-05-21

```

`WHERE` Keyword with `AND, OR`

```sql
SELECT * FROM person WHERE gender = "Male" AND (country = "Poland" OR country = "China");

```

```sql
 id  | first_name |  last_name  |              email              | gender | date_of_birth | country 
-----+------------+-------------+---------------------------------+--------+---------------+---------
   6 | Steve      | Vigus       | svigus5@google.de               | Male   | 2022-01-19    | China
  14 | Alaric     | Shepcutt    | ashepcuttd@tumblr.com           | Male   | 2022-02-12    | China
  25 | Barnett    | O'Geaney    |                                 | Male   | 2021-12-08    | China
  34 | Ulberto    | Hartzog     | uhartzogx@admin.ch              | Male   | 2022-04-05    | China
  37 | Ben        | Sattin      |                                 | Male   | 2021-09-18    | China
  58 | Renato     | Dimsdale    | rdimsdale1l@arstechnica.com     | Male   | 2021-06-24    | China
  60 | Stinky     | Dudney      | sdudney1n@smugmug.com           | Male   | 2021-11-10    | China
  62 | Consalve   | Ganter      | cganter1p@booking.com           | Male   | 2022-01-19    | Poland
  73 | Tedie      | Ovendale    | tovendale20@apple.com           | Male   | 2021-12-22    | China
  75 | Ab         | Nehlsen     | anehlsen22@uiuc.edu             | Male   | 2021-09-19    | China
  76 | Tiler      | Dunnan      | tdunnan23@indiatimes.com        | Male   | 2021-12-14    | China
  79 | Meir       | Prosser     | mprosser26@discovery.com        | Male   | 2022-04-10    | China
  83 | Hashim     | McRoberts   | hmcroberts2a@accuweather.com    | Male   | 2022-01-27    | China
 102 | Cristian   | Giblett     | cgiblett2t@ftc.gov              | Male   | 2022-04-01    | Poland

```
## Comparison Operators

When both values are equal then postgres will return `TRUE`, here `t` means `TRUE` `f` means `FALSE`

```sql
test=# SELECT 1 = 1;
 ?column? 
----------
 t
(1 row)

```

```sql
test=# SELECT 1 = 2;
 ?column? 
----------
 f
(1 row)

```

## Limit, Offset & Fetch

`LIMIT ` Keywork will limit the response results, here i have used limit as 10, the below query will returns only 10 records

```sql
test=# SELECT * FROM person LIMIT 10;

```

```sql

 id | first_name |  last_name  |             email             | gender | date_of_birth |  country  
----+------------+-------------+-------------------------------+--------+---------------+-----------
  1 | Megen      | Haddock     | mhaddock0@youku.com           | Female | 2022-04-19    | Portugal
  2 | Hilly      | Fellnee     | hfellnee1@purevolume.com      | Male   | 2021-07-20    | Portugal
  3 | Dani       | Tansey      | dtansey2@dailymail.co.uk      | Male   | 2021-08-26    | Honduras
  4 | Grant      | Aucourte    | gaucourte3@etsy.com           | Male   | 2021-06-06    | Japan
  5 | Ashlee     | Clawsley    | aclawsley4@indiegogo.com      | Female | 2021-12-10    | China
  6 | Steve      | Vigus       | svigus5@google.de             | Male   | 2022-01-19    | China
  7 | Glyn       | Hazelgreave | ghazelgreave6@apache.org      | Male   | 2022-01-19    | Argentina
  8 | Levy       | Kinneally   | lkinneally7@dion.ne.jp        | Male   | 2021-12-21    | Russia
  9 | Kasper     | Brookes     | kbrookes8@mac.com             | Male   | 2021-07-20    | Ecuador
 10 | Kellen     | Bidgood     | kbidgood9@cargocollective.com | Male   | 2022-04-14    | Greece
(10 rows)

```

`LIMIT` keyword with `OFFSET`, Here i gave 5 as offset value this will ommit the first 5 records and it will give next 10 records as response

```sql
test=# SELECT * FROM person OFFSET 5  LIMIT 10;

```

```sql
 id | first_name |  last_name  |             email             | gender  | date_of_birth |  country  
----+------------+-------------+-------------------------------+---------+---------------+-----------
  6 | Steve      | Vigus       | svigus5@google.de             | Male    | 2022-01-19    | China
  7 | Glyn       | Hazelgreave | ghazelgreave6@apache.org      | Male    | 2022-01-19    | Argentina
  8 | Levy       | Kinneally   | lkinneally7@dion.ne.jp        | Male    | 2021-12-21    | Russia
  9 | Kasper     | Brookes     | kbrookes8@mac.com             | Male    | 2021-07-20    | Ecuador
 10 | Kellen     | Bidgood     | kbidgood9@cargocollective.com | Male    | 2022-04-14    | Greece
 11 | Chrysler   | Spinola     | cspinolaa@amazon.de           | Female  | 2022-01-08    | Indonesia
 12 | Walliw     | Popelay     | wpopelayb@unicef.org          | Agender | 2021-09-27    | Argentina
 13 | Emmi       | Gepson      | egepsonc@nih.gov              | Female  | 2021-07-17    | China
 14 | Alaric     | Shepcutt    | ashepcuttd@tumblr.com         | Male    | 2022-02-12    | China
 15 | Sidnee     | Crew        | screwe@umn.edu                | Male    | 2021-09-15    | Albania
(10 rows)

```
`LIMIT` the records using the `FETCH` keyword

```sql
test=# SELECT * FROM person OFFSET 5 FETCH FIRST 5 ROW ONLY;

```

```sql
 id | first_name |  last_name  |             email             | gender | date_of_birth |  country  
----+------------+-------------+-------------------------------+--------+---------------+-----------
  6 | Steve      | Vigus       | svigus5@google.de             | Male   | 2022-01-19    | China
  7 | Glyn       | Hazelgreave | ghazelgreave6@apache.org      | Male   | 2022-01-19    | Argentina
  8 | Levy       | Kinneally   | lkinneally7@dion.ne.jp        | Male   | 2021-12-21    | Russia
  9 | Kasper     | Brookes     | kbrookes8@mac.com             | Male   | 2021-07-20    | Ecuador
 10 | Kellen     | Bidgood     | kbidgood9@cargocollective.com | Male   | 2022-04-14    | Greece
(5 rows)

```
## IN Keyword

Using the `IN` keyword we can provide multiple values to filter the records, in the below query we are filtering the only `China, Brazil `records

```sql
SELECT * FROM person WHERE country IN ('China','Brazil');

```

```sql
 id  | first_name |  last_name   |                email                 |   gender    | date_of_birth | country 
-----+------------+--------------+--------------------------------------+-------------+---------------+---------
   5 | Ashlee     | Clawsley     | aclawsley4@indiegogo.com             | Female      | 2021-12-10    | China
   6 | Steve      | Vigus        | svigus5@google.de                    | Male        | 2022-01-19    | China
  13 | Emmi       | Gepson       | egepsonc@nih.gov                     | Female      | 2021-07-17    | China
  14 | Alaric     | Shepcutt     | ashepcuttd@tumblr.com                | Male        | 2022-02-12    | China
  19 | Matelda    | Vallerine    | mvallerinei@w3.org                   | Female      | 2021-11-20    | China
  20 | Michele    | Gulberg      | mgulbergj@networksolutions.com       | Female      | 2021-10-14    | China
  25 | Barnett    | O'Geaney     |                                      | Male        | 2021-12-08    | China
  34 | Ulberto    | Hartzog      | uhartzogx@admin.ch                   | Male        | 2022-04-05    | China
  37 | Ben        | Sattin       |                                      | Male        | 2021-09-18    | China
  40 | Gisela     | Merida       | gmerida13@ameblo.jp                  | Female      | 2021-05-26    | China
  50 | Dacia      | Spowage      | dspowage1d@mozilla.com               | Female      | 2021-09-12    | China
  51 | Jenn       | Heelis       | jheelis1e@nymag.com                  | Female      | 2021-12-01    | China
  53 | Rodi       | Fechnie      | rfechnie1g@tiny.cc                   | Female      | 2021-09-22    | China
  58 | Renato     | Dimsdale     | rdimsdale1l@arstechnica.com          | Male        | 2021-06-24    | China
  60 | Stinky     | Dudney       | sdudney1n@smugmug.com                | Male        | 2021-11-10    | China
  66 | Tate       | Dibson       |                                      | Male        | 2022-05-17    | Brazil
  67 | Sammy      | Dron         | sdron1u@zimbio.com                   | Male        | 2022-03-17    | Brazil
  69 | Stefa      | McJerrow     | smcjerrow1w@patch.com                | Female      | 2022-02-11    | China
  70 | Windy      | Huyton       | whuyton1x@usgs.gov                   | Female      | 2021-06-23    | China
  72 | Sharla     | Fancourt     | sfancourt1z@ifeng.com                | Female      | 2021-07-09    | Brazil

```

## `BETWEEN` Keyword 

`BETWEEN` keyword is used to filter the records given two dates, the below query will filter the records only  `from '2021-01-01' to '2022-01-01'`

```sql
SELECT * FROM person WHERE date_of_birth BETWEEN DATE '2021-01-01' AND '2022-01-01';

```

```sql

 id  | first_name  |       last_name       |                email                 |   gender    | date_of_birth |             country              
-----+-------------+-----------------------+--------------------------------------+-------------+---------------+----------------------------------
   2 | Hilly       | Fellnee               | hfellnee1@purevolume.com             | Male        | 2021-07-20    | Portugal
   3 | Dani        | Tansey                | dtansey2@dailymail.co.uk             | Male        | 2021-08-26    | Honduras
   4 | Grant       | Aucourte              | gaucourte3@etsy.com                  | Male        | 2021-06-06    | Japan
   5 | Ashlee      | Clawsley              | aclawsley4@indiegogo.com             | Female      | 2021-12-10    | China
   8 | Levy        | Kinneally             | lkinneally7@dion.ne.jp               | Male        | 2021-12-21    | Russia
   9 | Kasper      | Brookes               | kbrookes8@mac.com                    | Male        | 2021-07-20    | Ecuador
  12 | Walliw      | Popelay               | wpopelayb@unicef.org                 | Agender     | 2021-09-27    | Argentina
  13 | Emmi        | Gepson                | egepsonc@nih.gov                     | Female      | 2021-07-17    | China
  15 | Sidnee      | Crew                  | screwe@umn.edu                       | Male        | 2021-09-15    | Albania
  16 | Guthrey     | Timoney               | gtimoneyf@homestead.com              | Male        | 2021-07-22    | South Africa
  18 | Lanny       | Guyonnet              | lguyonneth@squarespace.com           | Male        | 2021-08-09    | Argentina
  19 | Matelda     | Vallerine             | mvallerinei@w3.org                   | Female      | 2021-11-20    | China
  20 | Michele     | Gulberg               | mgulbergj@networksolutions.com       | Female      | 2021-10-14    | China
  21 | Elfie       | Glaister              | eglaisterk@people.com.cn             | Female      | 2021-05-31    | Indonesia
  22 | Dulcia      | Bloxland              | dbloxlandl@cmu.edu                   | Female      | 2021-12-23    | Laos
  25 | Barnett     | O'Geaney              |                                      | Male        | 2021-12-08    | China
  28 | Greg        | Murty                 | gmurtyr@foxnews.com                  | Male        | 2021-07-10    | Indonesia
  29 | Kikelia     | Adan                  | kadans@chicagotribune.com            | Female      | 2021-09-22    | Israel
  30 | Bernadette  | Balharry              | bbalharryt@homestead.com             | Female      | 2021-06-08    | France
  33 | Fidel       | Bomb                  | fbombw@fc2.com                       | Male        | 2021-10-18    | Botswana
:

```
## LIKE and iLIKE

The LIKE operator is used in a WHERE clause to search for a specified pattern in a column.

- The percent sign (%) represents zero, one, or multiple characters
- The underscore sign (_) represents one, single character


|LIKE Operator |	Description|
|--------------|---------------|
|WHERE CustomerName LIKE 'a%'| Finds any values that start with "a"|
|WHERE CustomerName LIKE '%a'|	Finds any values that end with "a"|
|WHERE CustomerName LIKE '%or%'|	Finds any values that have "or" in any position|
|WHERE CustomerName LIKE '_r%'|	Finds any values that have "r" in the second position|
|WHERE CustomerName LIKE 'a_%'|	Finds any values that start with "a" and are at least 2 characters in length|
|WHERE CustomerName LIKE 'a__%'|	Finds any values that start with "a" and are at least 3 characters in length|
|WHERE ContactName LIKE 'a%o'|	Finds any values that start with "a" and ends with "o"|

Filter the all the records if email ends with `@google.com`

```sql
test=# SELECT * FROM person WHERE email LIKE '%google.com';

```

```sql

 id  | first_name |  last_name   |           email            | gender | date_of_birth |  country  
-----+------------+--------------+----------------------------+--------+---------------+-----------
 476 | Max        | Shadrach     | mshadrachd7@google.com     | Male   | 2022-03-12    | Peru
 626 | Mathilda   | Lamberteschi | mlamberteschihd@google.com | Female | 2021-11-05    | Indonesia
(2 rows)

```

Filter the all the records if email starts with `a`

```sql
test=# SELECT * FROM person WHERE email LIKE 'a%';

```

```sql

 id  | first_name  |  last_name   |              email               |   gender    | date_of_birth |             country              
-----+-------------+--------------+----------------------------------+-------------+---------------+----------------------------------
   5 | Ashlee      | Clawsley     | aclawsley4@indiegogo.com         | Female      | 2021-12-10    | China
  14 | Alaric      | Shepcutt     | ashepcuttd@tumblr.com            | Male        | 2022-02-12    | China
  26 | Alejandrina | Hassur       | ahassurp@nationalgeographic.com  | Female      | 2022-04-01    | Russia
  75 | Ab          | Nehlsen      | anehlsen22@uiuc.edu              | Male        | 2021-09-19    | China
 110 | Aurilia     | Burgane      | aburgane31@google.co.uk          | Female      | 2021-11-03    | Philippines
 116 | Abbie       | Abrahmer     | aabrahmer37@huffingtonpost.com   | Male        | 2022-01-29    | Botswana
 137 | Alexandra   | Peskin       | apeskin3s@github.io              | Female      | 2022-03-31    | Philippines
 141 | Ashby       | Sainthill    | asainthill3w@statcounter.com     | Male        | 2021-11-10    | Philippines
 149 | Alleen      | Eckart       | aeckart44@discovery.com          | Female      | 2022-03-23    | France
 184 | Angy        | Bushe        | abushe53@bbc.co.uk               | Female      | 2022-04-27    | Philippines

```
Ingnore Case with `LIKE` Operator

```sql
SELECT * FROM person WHERE email ILIKE 'A%';

```

```sql

 id  | first_name  |  last_name   |              email               |   gender    | date_of_birth |             country              
-----+-------------+--------------+----------------------------------+-------------+---------------+----------------------------------
   5 | Ashlee      | Clawsley     | aclawsley4@indiegogo.com         | Female      | 2021-12-10    | China
  14 | Alaric      | Shepcutt     | ashepcuttd@tumblr.com            | Male        | 2022-02-12    | China
  26 | Alejandrina | Hassur       | ahassurp@nationalgeographic.com  | Female      | 2022-04-01    | Russia
  75 | Ab          | Nehlsen      | anehlsen22@uiuc.edu              | Male        | 2021-09-19    | China
 110 | Aurilia     | Burgane      | aburgane31@google.co.uk          | Female      | 2021-11-03    | Philippines
 116 | Abbie       | Abrahmer     | aabrahmer37@huffingtonpost.com   | Male        | 2022-01-29    | Botswana
 137 | Alexandra   | Peskin       | apeskin3s@github.io              | Female      | 2022-03-31    | Philippines
 141 | Ashby       | Sainthill    | asainthill3w@statcounter.com     | Male        | 2021-11-10    | Philippines
 149 | Alleen      | Eckart       | aeckart44@discovery.com          | Female      | 2022-03-23    | France
 184 | Angy        | Bushe        | abushe53@bbc.co.uk               | Female      | 2022-04-27    | Philippines

```
## GROUP BY

The GROUP BY statement groups rows that have the same values into summary rows, like "find the number of persons in each country".

The GROUP BY statement is often used with aggregate functions `(COUNT(), MAX(), MIN(), SUM(), AVG())` to group the result-set by one or more columns.

The below query will give output how many persons comes from each country.

```sql
SELECT country, COUNT(*) FROM person GROUP BY country; 

```
```sql
             country              | count 
----------------------------------+-------
 Bangladesh                       |     2
 Indonesia                        |   121
 Mayotte                          |     1
 Venezuela                        |     4
 Luxembourg                       |     1
 Czech Republic                   |    12
 Sweden                           |    22
 Uganda                           |     1
 Montenegro                       |     1
 Jordan                           |     1
 Dominican Republic               |     3
 Cambodia                         |     1
 Ireland                          |     5
 Sri Lanka                        |     2
 Laos                             |     2
 Uzbekistan                       |     2
 Finland                          |     9
 Portugal                         |    36
 Malta                            |     1
 Colombia                         |    16

```
`GROUP BY` with `ORDER BY `

```sql
SELECT country, COUNT(*) FROM person GROUP BY country ORDER BY country;

```

```sql
             country              | count 
----------------------------------+-------
 Afghanistan                      |     4
 Albania                          |     7
 Argentina                        |    18
 Armenia                          |     5
 Australia                        |     1
 Azerbaijan                       |     4
 Bangladesh                       |     2
 Belarus                          |     4
 Belgium                          |     1
 Benin                            |     3
 Bolivia                          |     2
 Bosnia and Herzegovina           |     2
 Botswana                         |     3
 Brazil                           |    42
 Bulgaria                         |     2
 Burkina Faso                     |     2
 Cambodia                         |     1
 Canada                           |     7
 Chad                             |     3
 Chile                            |     2

```

## HAVING Keyword

The having keyword works with `GROUP BY` basically it allow us to perform extra filtering after ferforming the aggregate.
Make sure the having keyword must be before `ORDER BY`

[Aggregate Functions](https://www.postgresql.org/docs/9.5/functions-aggregate.html)

The below query will the results more then `5` persons form the each country

```sql
SELECT country, COUNT(*) FROM person GROUP BY country HAVING COUNT(*) > 5 ORDER BY country;

```

```sql

    country     | count 
----------------+-------
 Albania        |     7
 Argentina      |    18
 Brazil         |    42
 Canada         |     7
 China          |   192
 Colombia       |    16
 Czech Republic |    12
 Finland        |     9
 France         |    34
 Greece         |    13
 Indonesia      |   121
 Iran           |     6
 Japan          |    16
 Mexico         |    15
 Morocco        |     6
 Nigeria        |    10
 Peru           |     6
 Philippines    |    52
 Poland         |    34
 Portugal       |    36

```
## Calculating MIN, MAX & AVG

The below query will give the most expensive car

```sql
test=# SELECT MAX(price) FROM cars;

   max    
----------
 99773.30
(1 row)

```

The below query will give the low expensive car

```sql
test=# SELECT MIN(price) FROM cars;

   min    
----------
 10037.80
(1 row)

```
The below query will give `Average` price of the cars  

```sql
test=# SELECT AVG(price) FROM cars;

        avg         
--------------------
 55878.591130000000
(1 row)

```

`ROUND` the average value

```sql
test=# SELECT ROUND(AVG(price)) FROM cars;

 round 
-------
 55879
(1 row)

```

`SUM`  of the all the cars

```sql
test=# SELECT SUM(price) FROM cars;

     sum     
-------------
 55878591.13
(1 row)

```
```sql
SELECT model, SUM(price) FROM cars GROUP BY model;

```

```sql

       model         |    sum    
----------------------+-----------
 Suburban 2500        | 215620.23
 300E                 |  82964.54
 Cherokee             | 191180.98
 Regal                |  58328.99
 Grand Am             | 190578.15
 G5                   |  78823.53
 2500                 | 131528.46
 Sportvan G20         |  21248.48
 Touareg              |  50939.90
 Safari               | 131550.35
 Azure                |  42295.44
 Navigator L          |  12576.59
 Savana 3500          | 136495.06
 350Z Roadster        |  97273.43

```

## Basics of Arthimetic Operators


```sql
test=# SELECT 1 + 2;
 ?column? 
----------
        3
(1 row)

test=# SELECT 10 - 5;
 ?column? 
----------
        5
(1 row)

test=# SELECT 10 * 5;
 ?column? 
----------
       50
(1 row)

test=# SELECT 10 * 2 + 8;
 ?column? 
----------
       28
(1 row)

test=# SELECT 10^2;
 ?column? 
----------
      100
(1 row)

test=# SELECT 5!;
 ?column? 
----------
      120
(1 row)

test=# SELECT 10 % 3;
 ?column? 
----------
        1
(1 row)

test=# SELECT 10 / 2;
 ?column? 
----------
        5
(1 row)

```

Calculating `10%` of each car price

```sql
SELECT id, make, model, price, price * .10 FROM CARS;

```

```sql

  id  |     make      |        model         |  price   | ?column?  
------+---------------+----------------------+----------+-----------
    1 | Oldsmobile    | Aurora               | 34973.11 | 3497.3110
    2 | Oldsmobile    | LSS                  | 72679.36 | 7267.9360
    3 | Mitsubishi    | Tredia               | 51701.98 | 5170.1980
    4 | Jeep          | Liberty              | 96688.24 | 9668.8240
    5 | Ford          | Ranger               | 60903.46 | 6090.3460
    6 | GMC           | Yukon                | 93403.29 | 9340.3290
    7 | Plymouth      | Prowler              | 70359.80 | 7035.9800
    8 | Chevrolet     | Lumina               | 66220.33 | 6622.0330
    9 | Honda         | Ridgeline            | 19385.56 | 1938.5560
   10 | Mercedes-Benz | SL-Class             | 24780.34 | 2478.0340

```

Remove `10%` from the actuall car price

```sql
SELECT id, make, model, price, ROUND(price * .10), ROUND(price - (price * .10), 2) FROM CARS;

```

```sql

  id  |     make      |        model         |  price   | round |  round   
------+---------------+----------------------+----------+-------+----------
    1 | Oldsmobile    | Aurora               | 34973.11 |  3497 | 31475.80
    2 | Oldsmobile    | LSS                  | 72679.36 |  7268 | 65411.42
    3 | Mitsubishi    | Tredia               | 51701.98 |  5170 | 46531.78
    4 | Jeep          | Liberty              | 96688.24 |  9669 | 87019.42
    5 | Ford          | Ranger               | 60903.46 |  6090 | 54813.11
    6 | GMC           | Yukon                | 93403.29 |  9340 | 84062.96
    7 | Plymouth      | Prowler              | 70359.80 |  7036 | 63323.82
    8 | Chevrolet     | Lumina               | 66220.33 |  6622 | 59598.30
    9 | Honda         | Ridgeline            | 19385.56 |  1939 | 17447.00
   10 | Mercedes-Benz | SL-Class             | 24780.34 |  2478 | 22302.31
   11 | Mercedes-Benz | SL-Class             | 69375.77 |  6938 | 62438.19
   12 | Bentley       | Azure                | 42295.44 |  4230 | 38065.90
   13 | Audi          | A4                   | 82490.08 |  8249 | 74241.07
   14 | Volkswagen    | GTI                  | 47303.01 |  4730 | 42572.71
   15 | Hyundai       | Azera                | 91418.81 |  9142 | 82276.93
   16 | Bentley       | Continental          | 21701.21 |  2170 | 19531.09


```

## Alias
If we not provided any `Alias` name by default postgres will take `function name or ?column` like that

```sql
SELECT id, make, model, price, ROUND(price * .10) AS ten_percentage, ROUND(price - (price * .10),2) AS discount_price FROM CARS;

```

```sql

  id  |     make      |        model         |  price   | ten_percentage | discount_price 
------+---------------+----------------------+----------+----------------+----------------
    1 | Oldsmobile    | Aurora               | 34973.11 |           3497 |       31475.80
    2 | Oldsmobile    | LSS                  | 72679.36 |           7268 |       65411.42
    3 | Mitsubishi    | Tredia               | 51701.98 |           5170 |       46531.78
    4 | Jeep          | Liberty              | 96688.24 |           9669 |       87019.42
    5 | Ford          | Ranger               | 60903.46 |           6090 |       54813.11
    6 | GMC           | Yukon                | 93403.29 |           9340 |       84062.96
    7 | Plymouth      | Prowler              | 70359.80 |           7036 |       63323.82
    8 | Chevrolet     | Lumina               | 66220.33 |           6622 |       59598.30
    9 | Honda         | Ridgeline            | 19385.56 |           1939 |       17447.00
   10 | Mercedes-Benz | SL-Class             | 24780.34 |           2478 |       22302.31
   11 | Mercedes-Benz | SL-Class             | 69375.77 |           6938 |       62438.19
   12 | Bentley       | Azure                | 42295.44 |           4230 |       38065.90
   13 | Audi          | A4                   | 82490.08 |           8249 |       74241.07
   14 | Volkswagen    | GTI                  | 47303.01 |           4730 |       42572.71
   15 | Hyundai       | Azera                | 91418.81 |           9142 |       82276.93

```
## Coalesce

Coalesce keyword allows us to provide default if value is not preset

```sql
test=# SELECT COALESCE(1);
 coalesce 
----------
        1
(1 row)

test=# SELECT COALESCE(1) AS number;
 number 
--------
      1
(1 row)

test=# SELECT COALESCE(null, 1) AS number;
 number 
--------
      1
(1 row)

test=# SELECT COALESCE(null,null, 1) AS number;
 number 
--------
      1
(1 row)

test=# SELECT COALESCE(null,null, 1, 10) AS number;
 number 
--------
      1
(1 row)

```
```sql
SELECT COALESCE(email,'Email Not Provided') from person;

```

```sql
               coalesce               
--------------------------------------
 mhaddock0@youku.com
 hfellnee1@purevolume.com
 dtansey2@dailymail.co.uk
 gaucourte3@etsy.com
 aclawsley4@indiegogo.com
 svigus5@google.de
 ghazelgreave6@apache.org
 lkinneally7@dion.ne.jp
 kbrookes8@mac.com
 kbidgood9@cargocollective.com
 cspinolaa@amazon.de
 wpopelayb@unicef.org
 egepsonc@nih.gov
 ashepcuttd@tumblr.com
 screwe@umn.edu
 gtimoneyf@homestead.com
 slegliseg@sina.com.cn
 lguyonneth@squarespace.com
 mvallerinei@w3.org
 mgulbergj@networksolutions.com
 eglaisterk@people.com.cn
 dbloxlandl@cmu.edu
 lleonidam@sciencedaily.com
 efarguharn@themeforest.net
 Email Not Provided ------------------------------------> default value 

```
## Timestamp and Dates

[Date & Time](https://www.postgresql.org/docs/8.2/datatype-datetime.html)

```sql
test=# SELECT NOW();
               now                
----------------------------------
 2022-05-21 10:44:18.889974+05:30
(1 row)

test=# SELECT NOW()::DATE;
    now     
------------
 2022-05-21
(1 row)

test=# SELECT NOW()::TIME;
       now       
-----------------
 10:44:31.198678
(1 row)

test=# 

```

```sql
test=# SELECT NOW() - INTERVAL '1 YEAR';
             ?column?             
----------------------------------
 2021-05-21 10:47:33.000334+05:30
(1 row)

test=# SELECT NOW() - INTERVAL '10 YEAR';
             ?column?             
----------------------------------
 2012-05-21 10:47:53.201786+05:30
(1 row)

test=# SELECT NOW() - INTERVAL '10 MONTHS';
             ?column?             
----------------------------------
 2021-07-21 10:47:57.819459+05:30
(1 row)

test=# SELECT NOW() - INTERVAL '10 DAYS';
             ?column?             
----------------------------------
 2022-05-11 10:48:05.918251+05:30
(1 row)

test=# SELECT NOW() - INTERVAL '10 DAY';
             ?column?             
----------------------------------
 2022-05-11 10:48:08.229571+05:30
(1 row)

test=# SELECT (NOW() - INTERVAL '10 DAY')::DATE;
    date    
------------
 2022-05-11
(1 row)

```

## Extracting Fields

```sql
test=# SELECT EXTRACT(YEAR FROM NOW());
 date_part 
-----------
      2022
(1 row)

test=# SELECT EXTRACT(MONTH FROM NOW());
 date_part 
-----------
         5
(1 row)

test=# SELECT EXTRACT(DAY FROM NOW());
 date_part 
-----------
        21
(1 row)

test=# SELECT EXTRACT(DOW FROM NOW());
 date_part 
-----------
         6
(1 row)

test=# SELECT EXTRACT(CENTURY FROM NOW());
 date_part 
-----------
        21
(1 row)

```

## Age Function

Actually `AGE` functio will take two arguments `AGE(NOW(), date_of_birth)` from date and to date

```sql
SELECT first_name, last_name, gender, country, date_of_birth, AGE(NOW(), date_of_birth) FROM person;

```

```sql

 first_name  |       last_name       |   gender    |             country              | date_of_birth |               age               
-------------+-----------------------+-------------+----------------------------------+---------------+---------------------------------
 Megen       | Haddock               | Female      | Portugal                         | 2022-04-19    | 1 mon 2 days 10:59:11.367512
 Hilly       | Fellnee               | Male        | Portugal                         | 2021-07-20    | 10 mons 1 day 10:59:11.367512
 Dani        | Tansey                | Male        | Honduras                         | 2021-08-26    | 8 mons 26 days 10:59:11.367512
 Grant       | Aucourte              | Male        | Japan                            | 2021-06-06    | 11 mons 15 days 10:59:11.367512
 Ashlee      | Clawsley              | Female      | China                            | 2021-12-10    | 5 mons 11 days 10:59:11.367512
 Steve       | Vigus                 | Male        | China                            | 2022-01-19    | 4 mons 2 days 10:59:11.367512
 Glyn        | Hazelgreave           | Male        | Argentina                        | 2022-01-19    | 4 mons 2 days 10:59:11.367512
 Levy        | Kinneally             | Male        | Russia                           | 2021-12-21    | 5 mons 10:59:11.367512
 Kasper      | Brookes               | Male        | Ecuador                          | 2021-07-20    | 10 mons 1 day 10:59:11.367512
 Kellen      | Bidgood               | Male        | Greece                           | 2022-04-14    | 1 mon 7 days 10:59:11.367512
 Chrysler    | Spinola               | Female      | Indonesia                        | 2022-01-08    | 4 mons 13 days 10:59:11.367512
 Walliw      | Popelay               | Agender     | Argentina                        | 2021-09-27    | 7 mons 24 days 10:59:11.367512
 Emmi        | Gepson                | Female      | China                            | 2021-07-17    | 10 mons 4 days 10:59:11.367512
 Alaric      | Shepcutt              | Male        | China                            | 2022-02-12    | 3 mons 9 days 10:59:11.367512
 Sidnee      | Crew                  | Male        | Albania                          | 2021-09-15    | 8 mons 6 days 10:59:11.367512

```
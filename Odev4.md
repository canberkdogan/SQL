`--film tablosunda bulunan replacement_cost sütununda bulunan birbirinden farklı değerleri sıralayınız.`
```SQL
SELECT DISTINCT replacement_cost
FROM film
```

`--film tablosunda bulunan replacement_cost sütununda birbirinden farklı kaç tane veri vardır?`
```SQL
SELECT COUNT (DISTINCT replacement_cost) 
FROM film	
```
`--film tablosunda bulunan film isimlerinde (title) kaç tanesini T karakteri ile başlar ve aynı zamanda rating 'G' ye eşittir?`
```SQL
SELECT COUNT(*)
FROM film 
WHERE title LIKE 'T%' AND rating = 'G';
```

`--country tablosunda bulunan ülke isimlerinden (country) kaç tanesi 5 karakterden oluşmaktadır?`
```SQL
SELECT COUNT (*) 
FROM country
WHERE LENGTH (country) = 5; 
```
`--city tablosundaki şehir isimlerinin kaç tanesi 'R' veya r karakteri ile biter?`
```SQL
SELECT COUNT (*)
FROM city 
WHERE city LIKE '%R' OR city LIKE '%r';
```

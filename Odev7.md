`--film tablosunda bulunan filmleri rating değerlerine göre gruplayınız.`

```SQL
SELECT rating 
FROM film
GROUP BY rating;
```

`--film tablosunda bulunan filmleri replacement_cost sütununa göre grupladığımızda film sayısı 50 den fazla olan replacement_cost değerini ve karşılık gelen film sayısını sıralayınız.`

```SQL
SELECT replacement_cost 
FROM film 
GROUP BY replacement_cost
HAVING COUNT (*) > 50;
```

`--customer tablosunda bulunan store_id değerlerine karşılık gelen müşteri sayılarını nelerdir?`

```SQL
SELECT store_id 
FROM customer
GROUP BY store_id ;
```

`--city tablosunda bulunan şehir verilerini country_id sütununa göre gruplandırdıktan sonra en fazla şehir sayısı barındıran country_id bilgisini ve şehir sayısını paylaşınız.`

```SQL
SELECT country_id, COUNT (*) 
FROM city 
GROUP BY country_id 
ORDER BY COUNT(*)
```

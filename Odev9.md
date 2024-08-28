`--city tablosu ile country tablosunda bulunan şehir (city) ve ülke (country) isimlerini birlikte görebileceğimiz INNER JOIN sorgusunu yazınız.`

```SQL
SELECT city, country 
FROM country
INNER JOIN city ON city.country_id = country.country_id;
```


`--customer tablosu ile payment tablosunda bulunan payment_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz INNER JOIN sorgusunu yazınız.`

```SQL
SELECT payment.payment_id, first_name, last_name FROM payment 
INNER JOIN customer ON customer.customer_id = payment.customer_id;
```

`--customer tablosu ile rental tablosunda bulunan rental_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz INNER JOIN sorgusunu yazınız.`

```SQL
SELECT first_name, last_name, rental_id FROM customer c
INNER JOIN rental r ON r.customer_id = c.customer_id;
```

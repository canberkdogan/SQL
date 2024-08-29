`SORU 1: film tablosunda film uzunluğu length sütununda gösterilmektedir. Uzunluğu ortalama film uzunluğundan fazla kaç tane film vardır?`

```SQL
SELECT COUNT(length) FROM film
WHERE length > 
(
	SELECT AVG(length) FROM film
)
```
`SORU 2: film tablosunda en yüksek rental_rate değerine sahip kaç tane film vardır?`

```SQL
SELECT COUNT(rental_rate) FROM film
WHERE rental_rate = ALL
(
	SELECT rental_rate FROM film
	WHERE rental_rate = 4.99 
)
```
`SORU 3: film tablosunda en düşük rental_rate ve en düşün replacement_cost değerlerine sahip filmleri sıralayınız.`

```SQL
SELECT title, rental_rate, replacement_cost FROM film
WHERE rental_rate = ALL
(
	SELECT rental_rate FROM film
	WHERE rental_rate = 0.99
)
AND replacement_cost = ALL
(
	SELECT replacement_cost FROM film
	WHERE replacement_cost = 9.99
)
```
`SORU 4: payment tablosunda en fazla sayıda alışveriş yapan müşterileri(customer) sıralayınız.`

```SQL
SELECT SUM(amount), customer.first_name, customer.last_name
FROM payment
JOIN customer ON customer.customer_id = payment.customer_id
GROUP BY payment.customer_id, customer.first_name, customer.last_name
ORDER BY SUM(amount) DESC
LIMIT 5;
```

## PROJE 12
Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

1-film tablosunda film uzunluğu length sütununda gösterilmektedir. Uzunluğu ortalama film uzunluğundan fazla kaç tane film vardır?

2-film tablosunda en yüksek rental_rate değerine sahip kaç tane film vardır?

3-film tablosunda en düşük rental_rate ve en düşün replacement_cost değerlerine sahip filmleri sıralayınız.

4-payment tablosunda en fazla sayıda alışveriş yapan müşterileri(customer) sıralayınız.

### ÇÖZÜM

```
SELECT COUNT(*) AS film_sayisi FROM film
WHERE length > (SELECT AVG(length) FROM film);

SELECT COUNT(*) AS film_sayisi FROM film
WHERE rental_rate = (SELECT MAX(rental_rate) FROM film);

SELECT title, rental_rate, replacement_cost FROM film
WHERE rental_rate = (SELECT MIN(rental_rate) FROM film)
AND replacement_cost = (SELECT MIN(replacement_cost) FROM film);

SELECT c.customer_id, c.first_name, c.last_name, COUNT(p.payment_id) AS toplam_alisveris FROM payment p
JOIN customer c ON p.customer_id = c.customer_id
GROUP BY c.customer_id, c.first_name, c.last_name
ORDER BY toplam_alisveris DESC;

```



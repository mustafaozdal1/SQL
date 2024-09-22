## PROJE 7

Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

1-film tablosunda bulunan rental_rate sütunundaki değerlerin ortalaması nedir?

2-film tablosunda bulunan filmlerden kaç tanesi 'C' karakteri ile başlar?

3-film tablosunda bulunan filmlerden rental_rate değeri 0.99 a eşit olan en uzun (length) film kaç dakikadır?

4-film tablosunda bulunan filmlerin uzunluğu 150 dakikadan büyük olanlarına ait kaç farklı replacement_cost değeri vardır?

### ÇÖZÜM

```
SELECT rating, COUNT(*) AS film_count FROM film
GROUP BY rating;

SELECT replacement_cost, COUNT(*) AS film_count FROM film
GROUP BY replacement_cost 
HAVING COUNT(*) > 50;

SELECT store_id, COUNT(*) AS customer_count FROM customer
GROUP BY store_id;

SELECT country_id, COUNT(*) AS city_count FROM city
GROUP BY country_id ORDER BY city_count DESC LIMIT 1;
```
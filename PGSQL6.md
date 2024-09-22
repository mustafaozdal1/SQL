## PROJE 6

Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

1-film tablosunda bulunan rental_rate sütunundaki değerlerin ortalaması nedir?

2-film tablosunda bulunan filmlerden kaç tanesi 'C' karakteri ile başlar?

3-film tablosunda bulunan filmlerden rental_rate değeri 0.99 a eşit olan en uzun (length) film kaç dakikadır?

4-film tablosunda bulunan filmlerin uzunluğu 150 dakikadan büyük olanlarına ait kaç farklı replacement_cost değeri vardır?

### ÇÖZÜM

```
SELECT AVG(rental_rate) AS average_rental_rate FROM film;

SELECT COUNT(*) AS count_starting_with_C FROM film
WHERE title LIKE 'C%';

SELECT MAX(length) AS max_length FROM film
WHERE rental_rate = 0.99;

SELECT COUNT(DISTINCT replacement_cost) AS distinct_replacement_cost_count FROM film
WHERE length > 150;


```
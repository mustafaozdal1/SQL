## PROJE 4

Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

1-film tablosunda bulunan replacement_cost sütununda bulunan birbirinden farklı değerleri sıralayınız.

2-film tablosunda bulunan replacement_cost sütununda birbirinden farklı kaç tane veri vardır?

3-film tablosunda bulunan film isimlerinde (title) kaç tanesini T karakteri ile başlar ve aynı zamanda rating 'G' ye eşittir?

-4country tablosunda bulunan ülke isimlerinden (country) kaç tanesi 5 karakterden oluşmaktadır?

5-city tablosundaki şehir isimlerinin kaç tanesi 'R' veya r karakteri ile biter?

### ÇÖZÜM

```
SELECT DISTINCT replacement_cost FROM film 
ORDER BY replacement_cost;

SELECT COUNT(DISTINCT replacement_cost) 
FROM film;

SELECT COUNT(*) FROM film 
WHERE title LIKE 'T%' AND rating = 'G';

SELECT COUNT(*) FROM country 
WHERE LENGTH(country) = 5;

SELECT COUNT(*) FROM city 
WHERE city LIKE '%R' OR city LIKE '%r';
```

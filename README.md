# SQL_Assignment_6

## Sorgu Senaryoları

* Film tablosunda bulunan rental_rate sütunundaki değerlerin ortalaması nedir?

```bash
SELECT AVG(rental_rate) AS ortalama_rental_rate
FROM film;
```

* Film tablosunda bulunan filmlerden kaç tanesi 'C' karakteri ile başlar?

```bash
SELECT COUNT(*) AS c_ile_baslayan_film_sayisi
FROM film
WHERE title LIKE 'C%';
```


* Film tablosunda bulunan filmlerden rental_rate değeri 0.99 a eşit olan en uzun (length) film kaç dakikadır?

```bash
SELECT MAX(length) AS en_uzun_film_suresi
FROM film
WHERE rental_rate = 0.99;
```

* Film tablosunda bulunan filmlerin uzunluğu 150 dakikadan büyük olanlarına ait kaç farklı replacement_cost değeri vardır?

```bash
SELECT COUNT(DISTINCT replacement_cost) AS farkli_replacement_cost_sayisi
FROM film
WHERE length > 150;
```
# Ptika ödev 12 

1. film tablosunda film uzunluğu length sütununda gösterilmektedir. Uzunluğu ortalama film uzunluğundan fazla kaç tane film vardır?

* SELECT count(*) WHERE lenght > (SELECT AVG(lenght) FROM film );

2. film tablosunda en yüksek rental_rate değerine sahip kaç tane film vardır?

* SELECT COUNT(*) FROM film WHERE (SELECT MAX(rental_rate) FROM film);

3. film tablosunda en düşük rental_rate ve en düşün replacement_cost değerlerine sahip filmleri sıralayınız.

* SELECT film FROM film WHERE 
* rental_rate = ANY (SELECT MIN(rental_rate) FROM film)
* AND
* replacement_cost = (SELECT MIN(replacement_cost) FROM film)

4. payment tablosunda en fazla sayıda alışveriş yapan müşterileri(customer) sıralayınız.

* SELECT customer_id, COUNT(*) AS most_payments FROM payment
* GROUP BY customer_id
* ORDER BY most_payments DESC;
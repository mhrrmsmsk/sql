# Patika ödev 11

1. actor ve customer tablolarında bulunan first_name sütunları için tüm verileri sıralayalım.

* (SELECT first_name FROM customer )
* UNION 
* (SELECT first_name FROM actor);

2. actor ve customer tablolarında bulunan first_name sütunları için kesişen verileri sıralayalım.

* (SELECT first_name FROM customer )
* INTERSECT 
* (SELECT first_name FROM actor);

3. actor ve customer tablolarında bulunan first_name sütunları için ilk tabloda bulunan ancak ikinci tabloda bulunmayan verileri sıralayalım.

* (SELECT first_name FROM customer )
* EXCEPT 
* (SELECT first_name FROM actor);
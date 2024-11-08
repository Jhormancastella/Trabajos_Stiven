## consultas INNER JOIN 

### Consulta 1 mostar los Pagos realizados por Clientes
```sql
SELECT p.payment_id AS payment_id, p.amount AS payment_amount,
cu.first_name AS customer_first_name, cu.last_name AS customer_last_name
FROM payment AS p
JOIN customer AS cu ON p.customer_id = cu.customer_id
LIMIT 8;

```
### Resultado:

![image](https://github.com/user-attachments/assets/7c7a24b5-240f-4691-b45d-d1ee9699a4eb)

### Consulta 2 mostrar películas junto con el número de inventario disponible
```sql
SELECT f.title AS movie_title, i.inventory_id AS inventory_number
FROM film AS f
JOIN inventory AS i ON f.film_id = i.film_id
LIMIT 5;

```
### Resultado:
![image](https://github.com/user-attachments/assets/bdb0757b-80b6-4888-b92d-bcfc3cb2d5dc)

### Consulta 3 mostrar los nombres de los clientes junto con sus ciudades de residencia
```sql
SELECT cu.first_name AS customer_first_name,
cu.last_name AS customer_last_name, ci.city AS city_name
FROM customer AS cu
JOIN address AS a ON cu.address_id = a.address_id
JOIN city AS ci ON a.city_id = ci.city_id;

```
### Resultado:
![image](https://github.com/user-attachments/assets/dc821ef8-1064-471e-9f45-a989a36bcef5)


### Consulta 4
```sql
SELECT p.payment_id AS payment_id, p.amount AS payment_amount,
cu.first_name AS customer_first_name, cu.last_name AS customer_last_name
FROM payment AS p
JOIN customer AS cu ON p.customer_id = cu.customer_id
ORDER BY p.amount ASC
limit 15;

```
### Resultado:
![image](https://github.com/user-attachments/assets/be25e224-4846-4fef-921f-f0efa32614e6)

![image](https://github.com/user-attachments/assets/05a3c5ac-24f7-4ccb-88f3-52a4fc999194)



### Consulta 5 mostar los nombres de los actores y el número de películas en las que han actuado,
```sql
SELECT a.first_name AS actor_first_name,
a.last_name AS actor_last_name, COUNT(fa.film_id) AS film_count
FROM actor AS a
JOIN film_actor AS fa ON a.actor_id = fa.actor_id
GROUP BY a.actor_id
ORDER BY film_count DESC
LIMIT 10;

```
### Resultado:
![image](https://github.com/user-attachments/assets/3e74c81c-2019-4aed-a207-0ee26f947cd5)


## Procedimientos almacenados

### Consulta 1
```sql

```
### Resultado:

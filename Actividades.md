# Challenge
Detalle de resolución de Challenge

## Análisis de datos y visualización

Se adjuntan en el repositorios los archivos de Caso Práctico Análisis de datos.pdf y Reporte Caso Práctico.pbix  [pip](https://github.com/emmanuelalejandro/Challenge/blob/main/Caso%20Pr%C3%A1ctico%20An%C3%A1lisis%20de%20datos.pdf)

## Challenge SQL
El DER se encuentra adjunto en el repositorio. DER.pdf

## Actividades de SQL
1.	Cantidad de usuarios Femeninos donde su apellido comience con la letra “R” 

```SQL
SELECT count(*) as cantidad
FROM users 
WHERE gender = "F"
AND last_name like 'R%';
```
2.	De los usuarios listados del punto 1 contar la cantidad de usuarios por País.

```SQL
SELECT Country, 
count(*) as cantidad
FROM users 
WHERE gender = "F"
AND last_name like 'R%'
GROUP BY country;
```
3. Crear un listado de las órdenes de compra que se crearon en 2021.
  ```SQL
SELECT* FROM orders
WHERE created_at like '%2021%';
```
4. De las OC del punto 3 quedarse solamente con las que tiene estado “Complete
```SQL
SELECT* FROM orders
WHERE created_at like '%2021%'
AND status = "Complete";
```
5.	Se necesita el monto total de “sale_prices”  de las OC del punto 4.
  ```SQL
SELECT
sum(order_items.sale_price) as SalePrice
FROM orders 
INNER JOIN order_items ON orders.order_id = order_items.order_id
WHERE orders.created_at like '%2021%'
AND orders.status = "Complete";
```
10.	Se necesita el monto de “sale_prices” de las OC del punto 4 por Centro de Distribución.
11.	Se necesita conocer el ranking de los 10 Brand más vendidos en el año 2021 con estado “Complete”.
12.	Se necesita saber el ranking de los países con más cantidad de OC y desplegarlo por año. Con estado “Complete”
## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)

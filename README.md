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

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)

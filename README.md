# consultas1.sql

## CONSULTAS SQL
![alt text](/img/tabla%20usuario.png "tabla usuario")

1. Para visualizar toda la informacion que contiene la tabla usuarios se puede incluir con lainstruccion SELECT el caracter '*' o cada uno de los campos de la tabla
`select * from usuario`
![consulta1](/img/consulta1.png "consulta1")

2. Visualizar solamente la identificación del usuario.

`select Identificacion from 'usuario'`
![consula2](/img/consulta2.png "consulta2")

3. si se desea obtener los registros cuya identificacion sean mayoreso iguales a 150, se debe utulizar la clausula WHERE que espicifica las condiciones que deben reunir los registros que se van a seleccionar.

`SELECT * FROM usuario WHERE Identificación>='150'`
![consulta3](/img/consulta3.png "consulta3")

4. si se desea obtener los registros cuyos los apellidos sean Vanegas o Cetina, se debe utilizar el operador IN que especifica los registros que se quieren visualizar de unatabla.

`SELECT apellidos FROM usuario WHERE apellidos IN ('Vanegas','Cetina')`
![consulta4](/img/consulta4.png "consulta4")

O se puede utilizar el operador OR.

`SELECT apellidos FROM usuario WHERE apellidos='Vanegas' OR apellidos='Cetina'`
![consulta4..1](/img/consulta4..1.png "consulta4..1")

5. si se desea obtener los registros cuya identificacion sea menor de '110' y la ciudad sea 'Cali', se debe utilizar el operador AND.

`SELECT * FROM usuario WHERE Identificacion<'110' AND ciudad_nac='Cali'`
![consulta5](/img/consulta5.png "consulta5")

6. Si se desea obtener los registros cuyos nombres empiezan con la letra 'A' se debe utilizar el operador LIKE que utiliza los patrones '%' (todos) y '_' (caracter).

`SELECT * FROM usuario WHERE nombre LIKE 'A%'`
![consulta6](/img/consulta6.png "consulta6")

7. Si se desea obtener los registros cuyos nombres contengan la letra 'a'

`SELECT * FROM usuario LIKE nombre LIKE '%a%'`
![consulta7](/img/consulta7.png "consulta7")

8. Si se desea obtener los registros donde la cuarta letra del nombre sea una 'a'

`SELECT * FROM usuario WHERE nombre LIKE '___a%'`
![consulta8](/img/consulta8.png "consulta8")

9. Si se desea obtener los registro cuya identificación esté entre el intervalo '110' y '150', sebe utilizar la clausula BETWEEN, que sirve para especificar un intervalo de valores

`SELECT * FROM usuario WHERE Identidicación BETWEEN '110' AND '150'`
![consulta9](/img/consulta9.png "consulta9")

## comando Delete

10. Para eliminar solamente los registros cuya identificación sea mayor de 138

`DELETE FROM usuario WHERE identificación'130`
![consulta10](/img/consulta10.png "consulta10")
![consulta10.2](/img/consulta10.2.png "consulta10.2")

11. Para actualizar la ciudad de nacimiento de cristian vanegas, cuya Identificación es 114

`UPDATE usuario SET ciudad_nac = 'Manizales'  WHERE Identificación='114'`
![consulta11](/img/consulta11.png"consulta11")
![consulta11.2](/img/consulta11.2.png "consulta11.2")

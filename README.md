## TP integrador BD

Grupos separados: Comisión 23560

 Trabajo Práctico Integrador Base de Datos

Se deberá crear una base de datos llamada “integrador_cac” y crear la siguiente tabla llamada “oradores”:

 ![Imagen TP BD](https://github.com/3dl3rw0lf/c_c_tp_integrados_bbdd/blob/main/Imagen%20TP%20BD.PNG)

- Definir los tipos de datos correspondientes
- Definir la clave primaria correspondiente
- Definir las restricciones correspondientes
- Insertar 10 registros
- Hacer un backup de la base de datos

La entrega deberá ser subiendo el Backup de la base de datos, una captura de la estructura de la tabla y una captura de los registros insertados a un repositorio de Github y luego compartir el enlace.

Para crear la tabla se utiliza la sentencia DDL [CREATE TABLE](https://github.com/3dl3rw0lf/c_c_tp_integrados_bbdd/blob/main/MySQL_statements/create_table_oradores.sql).

```mysql
-- integrador_cac.oradores definition

CREATE TABLE integrador_cac.oradores (
	id_orador INT auto_increment NOT NULL,
	nombre varchar(100) NOT NULL,
	apellido varchar(100) NOT NULL,
	mail varchar(100) NOT NULL,
	tema varchar(255) NOT NULL,
	fecha_alta DATE NOT NULL,
	CONSTRAINT oradores_pk PRIMARY KEY (id_orador)
)
ENGINE=InnoDB
DEFAULT CHARSET=utf8mb4
COLLATE=utf8mb4_general_ci;
```

La obtención de la [estructura](https://github.com/3dl3rw0lf/c_c_tp_integrados_bbdd/blob/main/desc_oradores.png) de la tabla **oradores** se utiliza la sentencia [DESCRIBE](https://github.com/3dl3rw0lf/c_c_tp_integrados_bbdd/blob/main/MySQL_statements/desc.sql).

```mysql
DESC ORADORES;
```

Para la inserción de los oradores se utilizó en la tabla se usó la sentencia DML [INSERT](https://github.com/3dl3rw0lf/c_c_tp_integrados_bbdd/blob/main/MySQL_statements/create_table_oradores.sql).

```mysql
INSERT
	INTO
	INTEGRADOR_CAC.oradores (id_orador,
	nombre,
	apellido,
	mail,
	tema,
	fecha_alta)
VALUES
 	(7,"Donald D.","Chamberlin","don-cham@sql.com","What is the Structured Query Language","2023-10-28"),	
	(8,"Raymond F.","Boyce", "ray-boyce@sql.com","What is the Structured Query Language","2023-10-28"),
	(14,"Michael","Widenius","widenius_m@mariadb.com","The creation of MariaDB Foundation","2023-11-09"),
	(15,"David","Axmar","axmar_d@mariadb.com","The creation of MariaDB Foundation","2023-11-09"),
	(21,"Michael","Stonebraker","stone_braker_m@postgres.com","Object-Oriented Relational Databases","2023-10-21"),
	(24,"Edgar Frank", "Codd","codd-edgarf@ibm.com","Relational Database Model","2023-11-04"),
	(25, "Stephen", "Cook", "cook-stephen@harvard.com", "The Complexity of Theorem Proving Procedures","2023-10-28"),
	(28,"Mike", "Saranga","mike_saranga@informix.com","DB/2 Database","2023-11-07"),
	(35,"Tony","Hoare","hoare@quicksort.com","What is the Quicksort sorting algorithm?","2023-10-21"),
	(42,"Paula","Hawthtorn","hawthtorn_p@postgres.com","How to market postgres","2023-11-01");
```

El [backup](https://github.com/3dl3rw0lf/c_c_tp_integrados_bbdd/blob/main/MySQL_statements/dump-integrador_cac-202311082039.sql) de la tabla se realiza automáticamente con la herramienta *Dump database* del **DBMS**.

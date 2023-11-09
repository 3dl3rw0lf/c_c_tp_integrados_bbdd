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


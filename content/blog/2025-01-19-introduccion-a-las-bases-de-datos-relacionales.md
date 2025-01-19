---
title: Introducción a las bases de datos relacionales
draft: false
tags:
  - bbdd
---
# **Introducción a las bases de datos relacionales**

## **¿Qué es una base de datos relacional?**

En una base de datos relacional abandonamos el modelo clásico de almacenamiento de datos en ficheros y pasamos a almacenar los datos en tablas. Cada tabla es un conjunto de datos que se organiza en filas y columnas. Las filas representan los registros y las columnas los campos de cada registro.

Lo importante no es tanto su estructura, sino la relación que existen entre las tablas. De ahí el nombre de base de datos relacionales.

## **Tipos de datos**

Las bases de datos relacionales poseen tipos de datos que se pueden almacenar en las tablas.

### **Tipos de datos numéricos**

\- `INT`: Números enteros.

\- `DECIMAL`: Números decimales.

\- `NUMERIC`: Números decimales.

### **Tipos de datos de texto**

\- `CHAR`: Cadena de texto de longitud fija.

\- `VARCHAR`: Cadena de texto de longitud variable.

\- `TEXT`: Cadena de texto de longitud variable.

### **Tipos de datos de fecha y hora**

\- `DATE`: Fecha.

\- `TIME`: Hora.

\- `DATETIME`: Fecha y hora.

\- `TIMESTAMP`: Fecha y hora.

### **Otros datos**

\- `BLOB`: Datos binarios.

\- `ENUM`: Lista de valores.

\- `SET`: Conjunto de valores.

\- `JSON`: Datos en formato JSON.

## **Características de los tipos de datos**

### **No-nulidad**

Indica si un campo puede tener valores nulos o no, es decir, si el campo debe tener un valor o puede estar vacío.

### **Unicidad**

Indica si un campo debe tener valores únicos, es decir, si el campo puede tener valores repetidos o no.

### **Clave primaria**

Es un campo o conjunto de campos que identifica de forma única a cada registro de una tabla. Una clave primaria **siempre** debe ser única y no nula.

### **Clave foránea**

Es un campo que se usa para establecer relaciones entre dos tablas. La clave foránea en una tabla es la clave primaria de otra tabla.

### **Autoincremento**

Indica si un campo se incrementa automáticamente en cada inserción de un nuevo registro.

## **Clave primaria**

Una clave primaria es un campo que identifica de forma única a cada registro de una tabla. Una clave primaria no puede tener valores repetidos, y no puede ser nula.

Las claves primarias son **muy importantes** para identificar los registros de una tabla.

Considera una tabla de alumnos con las siguentes columnas:

\- `id`: clave primaria, numero

\- `nombre`: texto

\- `password`: texto

En esta tabla, el campo `id` es la clave primaria, ya que identifica de forma única a cada registro de la tabla.

## **Clave foránea**

Una clave foránea es un campo que se utiliza para relacionar dos tablas. Una clave foránea puede tener valores repetidos, y puede ser nula.

Piensa en la tabla anterior:

\- `usuario_id`: clave primaria, numero

\- `nombre`: texto

\- `password`: texto

\- `pedido_id`: clave foránea, numero

Piensa que tenemos otra tabla de pedidos con las siguientes columnas:

\- `pedido_id`: clave primaria, numero

\- `usuario_id`: clave foránea, numero

\- `producto`: texto

\- `cantidad`: numero

En esta tabla, el campo `usuario_id` es una clave foránea, ya que se utiliza para relacionar las dos tablas, al igual que el campo `pedido_id`, que es la clave primaria de la tabla de pedidos y la clave foránea de la tabla de usuarios.
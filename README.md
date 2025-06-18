# Reto Pragma 2 - API Fake Store con Dart

Este proyecto desarrollado en Dart consume datos de la API Fake Store (https://fakestoreapi.com/) con el objetivo de crear modelos y manejo de errors usando 'Either' del paquete dartz y mostrar la información proveniente de la API en consola.

## Objetivo

- Consumir 3 endpoints de la API Fake Store.
- Crear modelos de datos inmutables.
- Manejar errores usando el Either de la librería dartz.
- Mostrar la información en consola.

## Dependencias

- http – Para realizar peticiones HTTP.
- dartz – Para manejar errores con Either.


## Modelos de Datos
Product
Incluye id, title, description, price, etc.

Cart
Incluye id, userId, date, y una lista de productos (CartProduct).

User
Incluye username, email, y una dirección con ciudad.

Todos los modelos están diseñados para ser inmutables y se construyen usando factory constructors.

## API Fake Store

Se consumen los siguientes endpoints:

/products : Lista de productos.

/carts : Lista de carritos.

/users : Lista de usuarios.

El consumo se realiza mediante la clase ApiService, que devuelve un Either para cada llamada.

## Manejo de Errores con Either
Todas las funciones retornan Future<Either<String, List<T>>>, lo cual permite capturar errores y mostrarlos sin lanzar excepciones:


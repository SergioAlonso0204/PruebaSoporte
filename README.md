# Prueba Técnica - Sistema de Gestión de Tareas

## Descripción del Proyecto

Este proyecto es un sistema básico de gestión de tareas desarrollado con Laravel y Vue.js. El objetivo de esta prueba técnica es identificar y corregir errores en el código tanto en el backend como en el frontend. El sistema permite a los usuarios crear, actualizar, eliminar y visualizar tareas.

## Objetivo de la Prueba

El objetivo principal de esta prueba es evaluar tus habilidades para depurar y corregir errores en un proyecto existente que utiliza Laravel, PHP, JavaScript, y Vue.js. Deberás:

- Identificar y corregir errores en el backend relacionado con la creación, actualización, eliminación y validación de tareas.
- Corregir problemas en el frontend que afectan la visualización y manejo de la lista de tareas.
- Asegurarte de que las tareas se gestionen correctamente en la interfaz de usuario.

Además, deberás agregar una funcionalidad extra para filtrar las tareas completadas y pendientes.



## SOLUCION

Al Montar el proyecto, lo primero que vemos es un formulario basico, con 3 inputs "nombre de la tarea, descripcion y correo del usuario", para agregar una tarea, 
realizo la prueba de agregarla y encuentro el primer error.

Al guardar una tarea esta realizando la sentencia La tabla "Users", y en la base de datos es "user"
Table 'laravel.users' doesn't exist (SQL: select * from `users` where `email` = andres@gmail.com limit 1)"
aqui se evidencia que se realiza mal la consulta desde el momento uno al querer buscar en una tabla no existente.

Solucion, se busco en el modelo User, la variable $table que hace referencia a la tabla en la base de datos y vemos que tiene asignada el valor "users", se cambia este por el correspondiente en la bd el cual es "user" 

Se continua realizando el proceso normal "Crear, Actualizar, Eliminar" al momento de actualizar el estado a completo - terminado, sale un error en el catch, ademas de esto en el eliminar sale un error 404 lo cual evidencia que no existe o esta mal llamada la funcion, en el front evidenciamos que solo lista la tarea al crearla y las demas que esten en la base de datos no las muestra, al recargar la pagina se quita la que agregamos y no se visualizan las tareas creadas, las cuales en la base de datos estan correctamente agregadas, estos son los errores principales que encuentro al realizar las pruebas

Agradesco la oportunidad de realizar esta prueba tecnica, ha sido de mucha ayuda para ponerme a prueba, no la logre completar  logre identificar los problemas comunes en el proyecto, le di solucion a uno y estuve revisando y haciendo pruebas para solucionar los demas, seguire intentandolo por mi parte

Quedo pendiente al proceso, si le dan continuidad o lo dan por finalizado, de todas formas muchas gracias 


   

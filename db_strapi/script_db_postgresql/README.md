# Levantar ambiente de strapi
A continuación se describe como levantar **strapi** de forma local en el sistema operativo Linux(Ubuntu).
Se necesitan tener instalados estas herramientas para la configuración del ambiente. 
-- https://dbeaver.io/
-- https://www.postgresql.org/download/
-- https://nodejs.org/es/download/


# 	Archivos

Se tiene comprimido un archivo **cms-sat** en la cual se encuentran las imágenes y los archivos de las colecciones creadas en strapi **api y public**


## Base de datos

- Se debe crear la base de datos en postgresql en este caso la versión 13.2
	> CREATE DATABASE strapi_sat;
- Crear el proyecto de strapi.
	>  npx create-strapi-app cms-sat
- Va a recomendar de utilizar un templete en este caso indicamos que no. 
- Seleccionamos que se va a conectar con postgres, insertamos las credenciales y la damos continuar (por los regular el puerto es 5432 y el user postgres).


# Strapi

Una vez terminado de crear el proyecto, entramas en la carpeta **cd cms-sat** y luego **npm run develop**, entramos a la url http://localhost:1337/admin
>  creamos nuestro usuario para poder ingresar a la pantalla principal de strapi. 
>  Luego de haber creado el usuario, en la terminal detenemos el strapi. 
>  
## Configuración de base de datos y archivos
Con la ayuda de DBeaver nos conectamos a la base de datos y ejecutamos primero el script del archivo **script_tablas_strapi_sat.sql**  y luego  **Insert_data_colecciones_strapi.sql**

- En la carpeta del proyecto en *api y public* remplazamos los archivos que vienen comprimidos en este repositorio. 
---
Iniciamos de nuevo strapi  **npm run develop**  y podemos observar que ya se encuentran nuestras colecciones
-  Nos vamos a **Settings**  > **Roles**  > **Public**  y en permisos seleccionamos **find** en todas las colecciones y damos **Save** con eso ya se puede acceder a las colecciones 
- por ejemplo la colección de contribuyentes http://localhost:1337/contribuyentes

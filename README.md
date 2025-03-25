# PPS-Unidad3Actividad1-Aaron


## Entorno de pruebas
Vamos también a crear un entorno de pruebas en los que vamos a realizar las prácticas, creando servidores y archivos con vulnerabiliades presentes, para corregirlas posteriormente.

Tenemos diferentes opciones para realizarlo, entre ellas:

- Crear una máquina virtual e instalar todo lo necesario: Una pila sea del tipo que sea: LAMP, LEMP, MEAN, XAMPP, WAMP y AMPPS.

- Crear un escenario multicontenedor con cualquiera de esas pilas.

En esta ocasión vamos utilizar la segunda opción, crearemos un escenario multicontenedor con cualquiera de las pilas que nos podemos encontrar en docker hub. Yo he utilizado la primera que me he encontrado:https://github.com/sprintcube/docker-compose-lamp.git

Veamos:

- Clonamos el repositorio en nuestro equipo local.
```bash
git clone https://github.com/sprintcube/docker-compose-lamp.git
```
- Entramos dentro de la carpeta del proyecto.
```bash
cd docker-compose-lamp/
```
-  Hacemos una copia del fichero sample.env en un fichero llamado .env. Démonos cuenta que este fichero es el que contiene las variables que se van a utilizar en las diferentes máquinas que vamos a crear. si lo abrimos, tiene este aspecto:
```bash
cp sample.env .env
```

Antes de continuar, para securizar las variables por defecto que vienen en sample.env vamos a modificarlas.
En mi caso, he cambiado las variables de los puertos y las varibales de credeciales por defecto.

![](imagenes/img_sample.png)

Al finalizar la configuración de las variables, podemos levantar el entorno con el siguiente comando:
```bash
docker-compose up -d
```

Y su todo nos va bien, tendremos el entorno correctamente levando al que podemos acceder desde el puerto que hayamos especificado en las variables.

![](imagenes/img_entornos.png)

Dentro del entorno podemos acceder a todos los servicios que hemos levantado desde el apartado de links rápidos.

![](imagenes/img_links.png)

Si accedemos a cada uno de los apartados debería mostrar algo como lo siguiente:

![](imagenes/img_php.png)
![](imaganes/img_sql.png)
![](imagenes/img_test_sql.png)
![](imagenes/img_test_db.png)

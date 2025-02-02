<h2 align="center">CASOS PRÁCTICOS</h2>

## A) Versión de Nginx

Ejecutamos el comando _nginx -v_

![Comprobación de red](./imagenes/A_VERSION_NGINX_INSTALADO.PNG)

## B) Servicio asociado

Ejecutaremos _systemctl status nginx_ para comprobar que ha sido instalado correctamente y que está en funcionamiento.

![Comprobación de red](./imagenes/B_SERVICIO_ASOCIADO.PNG)

## C) Ficheros de configuración

El fichero está situado en _/etc/nginx_.

![Comprobación de red](./imagenes/C_INSPECCIONAR_FICHEROS.PNG)

<br>

Se puede configurar en _/etc/nginx/nginx.conf_

![Comprobación de red](./imagenes/C_ARCHIVO_CONFIGURACION.PNG)

## D) Modificación de la página web

Para que no nos aparezca la página predeterminada de nginx, modificaremos el archivo que se encuentra en _/var/www/html/index.nginx-debian.html_

![Comprobación de red](./imagenes/D_MODIFICACION_PAGINAWEB.PNG)

## E) Virtual hosting

Crearemos dos directorios para las dos webs.

![Comprobación de red](./imagenes/E_VIRTUAL_HOSTING_CREACION_DIRECTORIO.PNG)

Le concedemos los permisos pertinentes a los directorios.

![Comprobación de red](./imagenes/E_VIRTUAL_HOSTING_CONCESION_PERMISOS.PNG)

Crearemos el `index.html` para las dos páginas webs.

![Comprobación de red](./imagenes/E_VIRTUAL_HOSTING_CREACION_INDEX1.PNG)

![Comprobación de red](./imagenes/E_VIRTUAL_HOSTING_CREACION_INDEX2.PNG)

Crearemos los sites-availables para las webs.

![Comprobación de red](./imagenes/E_VIRTUAL_HOSTING_SITES-AVAILABLE.PNG)

Configuraremos el archivo hosts para nuestras dos webs.

![Comprobación de red](./imagenes/E_VIRTUAL_HOSTING_ARCHIVO_HOSTS.PNG)

Finalmente, tendremos esto como resultado.

![Comprobación de red](./imagenes/E_VIRTUAL_HOSTING_RESULTADO_FINAL.PNG)

## F) Autenticación, autorización Y control de acceso

Le dotaremos a la web1 de conexión tanto interna como externa, sin embargo a la web2 le daremos solo conexión con la red interna.

Para conseguir este objetivo deberemos mofdificar los `sites-availabes` de cada uno como vemos en la imágenes.

![Comprobación de red](./imagenes/F_MODIFICACIÓN_SITES-AVAILABLE.PNG)

![Comprobación de red](./imagenes/F_MODIFICACIÓN_SITES-AVAILABLE2.PNG)

Modificaremos las ip's permitidas en el archivo hosts tanto para red interna como externa

![Comprobación de red](./imagenes/F_MODIFICACIÓN_ARCHIVO_HOSTS.PNG)

Comprobaremos la red externa para saber si se ha realizado con éxito los cambios que hemos realizado con anterioridad.

![Comprobación de red](./imagenes/F_COMPROBACION_REDEXTERNA_OPCIONBUENA.PNG)

También comprobaremos la red interna mediante el comando `curl`

![Comprobación de red](./imagenes/F_COMPROBACION_REDINTERNA_CURL.PNG)





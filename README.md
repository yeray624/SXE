

La siguiente práctica es una lista de tareas que tenéis que hacer. 

Por cada tarea tenéis que ir poniendo los comandos utilizados y, brevemente, describir el proceso y como compruebas que se ha realizado lo pedido en un fichero (nombre "Readme.md") con formato markdown.

Crear un repositorio en github para subir este fichero

Cada dos apartados tenéis que hacer un commit nombrando el numero del apartado

En la respuesta pon el enlace a tu repositorio en github

Utiliza la imagen de Apache, tag 2.4 y apoyandote en la mini guía de docker sigue las instrucciones:

## Descarga la imagen 'httpd' y comprueba que está en tu equipo.
'''docker pull httpd'''

## Crea un contenedor con el nombre 'dam_web1'.
'''docker run -d --name=dam_web1 httpd'''

## Si quieres poder acceder desde el navegador de tu equipo, ¿que debes hacer?
Utiliza bind mount para que el directorio del apache2 'htdocs' esté montado un directorio que tu elijas.
'''docker run -d --name=dam_web1 -p 8080:80 -v /home/youbinarey/dam2/sxe:/usr/local/apache2/htdocs httpd'''
Al desplegar el servidor y acceder a traves de un cliente como el navegador propio me muestra el contenido directorio referenciado /home7youbinarey/dam2/sxe
    
## Realiza un 'hola mundo' en html y comprueba que accedes desde el navegador.
'''echo "hola mundo" > web.html'''
Indexo la ruta en el navegador http://10.0.9.102:8080/web.html o accedor atraves del directorio principal

## Crea otro contenedor 'dam_web2' con el mismo bind mount y a otro puerto, por ejemplo 9080.
docker run -d --name=dam_web2 -p 9090:80 -v /home/youbinarey/dam2/sxe:/usr/local/apache2/htdocs httpd

## Comprueba que los dos servidores 'sirven' la misma página, es decir, cuando consultamos en el navegador:
        Sí muestran ambos puertos referencian el mismo contenido
## Realiza modificaciones de la página y comprueba que los dos servidores 'sirven' la misma página
'''touch "NUEVO CONTENIDO PARA LA TAREA 2" > web.html'''

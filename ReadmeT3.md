# TAREA 3
***
## Descarga la imagen 'httpd' y comprueba que está en tu equipo.
``docker pull httpd``

## Crea un contenedor con el nombre 'dam_web1'.
``docker run -d --name=dam_web1 httpd``

## Si quieres poder acceder desde el navegador de tu equipo, ¿que debes hacer? Utiliza bind mount para que el directorio del apache2 'htdocs' esté montado un directorio que tu elijas.
``docker run -d --name=dam_web1 -p 8080:80 -v /home/youbinarey/dam2/sxe:/usr/local/apache2/htdocs httpd``

Al desplegar el servidor y acceder a traves de un cliente como el navegador propio me muestra el contenido directorio referenciado /home/youbinarey/dam2/sxe

## Realiza un 'hola mundo' en html y comprueba que accedes desde el navegador.
``echo "hola mundo" > web.html``  

Indexo la ruta en el navegador http://10.0.9.102:8080/web.html o accedor atraves del directorio principal

## Crea otro contenedor 'dam_web2' con el mismo bind mount y a otro puerto, por ejemplo 9080.
``docker run -d --name=dam_web2 -p 9090:80 -v /home/youbinarey/dam2/sxe:/usr/local/apache2/htdocs httpd``

## Comprueba que los dos servidores 'sirven' la misma página, es decir, cuando consultamos en el navegador:
Sí las muestra, ambos puertos referencian el mismo contenido
        
## Realiza modificaciones de la página y comprueba que los dos servidores 'sirven' la misma página
``touch "NUEVO CONTENIDO PARA LA TAREA 2" > web.html``

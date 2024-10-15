# TAREA 3
# Descarga la imagen 'httpd' y comprueba que está en tu equipo.
'''docker pull httpd'''

## Crea un contenedor con el nombre 'dam_web1'.
'''docker run -d --name=dam_web1 httpd'''

## Si quieres poder acceder desde el navegador de tu equipo, ¿que debes hacer? Utiliza bind mount para que el directorio del apache2 'htdocs' esté montado un directorio que tu elijas.
'''docker run -d --name=dam_web1 -p 8080:80 -v /home/youbinarey/dam2/sxe:/usr/local/apache2/htdocs httpd'''
Al desplegar el servidor y acceder a traves de un cliente como el navegador propio me muestra el contenido directorio referenciado /home/youbinarey/dam2/sxe

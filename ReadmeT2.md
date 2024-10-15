# TAREA 2

## Descarga la imagen "alpine" SIN ARRANCARLA y comprueba que está en tu equipo
'''docker pull alpine'''
'''docker images'''

## Crea un contenedor sin ponerle nombre. ¿está arrancado? Obtén el nombre
'''docker create alpine'''
'''docker ps -a'''
No está arrancado

## Crea un contenedor con el nombre 'dam_alp1'. ¿Como puedes acceder a él?
'''docker run -it --name=dam_alp1 alpine /bin/sh
'''
Se abre una terminal y estoy dentro del contenedor

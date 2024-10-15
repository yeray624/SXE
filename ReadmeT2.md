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

## Comprueba que ip tiene y si puedes hacer un ping a google.com
'''hostname -i'''
Arroja la 172.17.0.2

## Crea un contenedor con el nombre 'dam_alp2'. ¿Puedes hacer ping entre los contenedores?
'''docker run -it --name=dam_alp2 alpine /bin/sh'''
''' ping172.17.0.2'''
Sí pueden hacer ping entre los contenedores

## Sal del terminal, ¿que ocurrió con el contenedor?
'''exit'''
Se ha detenido la ejecución del contenedor

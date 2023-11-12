# Crear, copiar, mover y eliminar ficheros #

## Crear ficheros (touch) ##
Para crear ficheros disponemos del comando "touch" el cual crea un fichero vacio con el nombre indicado. El fichero no es necesario que tenga extensión en caso de que no se quiera.

    touch file_1

o

    touch file_2.txt

## borrar ficheros (rm) ##
Para borrar cualquier fichero utilizaremos el comando "rm" y el nombre del fichero indicado.

    rm file_1

o

    rm file_2.txt

## mover ficheros (mv) ##
Para mover ficheros utilizaremos el comando "mv" el cual necesitará dos parámetros:

- El primero es la ruta de origen
- El segundo es la ruta destino

El comando seria de la siguiente forma:

    # mv ruta_origen ruta_destino

Este comando también se puede utilizar para cambiar el nombre del fichero:

    # mv origin_name new_name

***
***NOTA***
El comando mover (mv) no modifica ni el usuario ni los permisos del fichero original.
***

## copiar ficheros (cp) ##
Para copiar ficheros utilizaremos el comando "cp" el cual necesitará dos parámetros:

- El primero es la ruta de origen
- El segundo es la ruta destino

El comando seria de la siguiente forma:

    # cp ruta_origen ruta_destino

Tambien se puede copiar varios ficheros a un destino en particular:

    # cp file_1 file_2 file_3 ruta_destino

Este comando también se puede utilizar para cambiar el nombre del fichero:

    # cp origin_name new_name

***
***NOTA***
El comando copiar (cp) al crear un fichero nuevo, se crea con los permisos del usuario que ejecuta el comando.
***

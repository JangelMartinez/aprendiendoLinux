# Crera, eliminar y mover directorios #
## Crear directorios (mkdir) ##
Con el comando "mkdir" podemos crear uno o varios directorios en la ruta actual.

Para crear un directorio

    # mkdir name_directory

Para crear varios directorios a la vez

    # mkdir name_dir1 name_dir2 name_dir3

El espacio entre ellos indica que son directorios diferentes

Crear un nombre de directorio que tenga un espacio en mitad hay que utilizar las comillas

    # mkdir "name directory"

Crear un directorio dentro de otro que ya existe en tu ruta actual (ruta relativa)

    # mkdir directory_exist/new_directory

Crear directorios aunque no existan en la ruta con la opción "-p"
 
    # mkdir -p directory_not_exists/new_directory

Con este ejemplo crearia los dos directorios

## Eliminar directorios (rm -r) ##
Se puede eliminar directorios con todo su contenido con el comando "rm -r" de la ruta que le indiques (rutas absolutas o relativas).

Eliminas el directorio dir1 que existe en la ruta actual.

    rm -r dir1

Eliminar un directorio sin entrar en la carpeta correspondiente:

    rm -r directory/name_remove_directory

## Mover directorios (mv) ##
Se puede mover carpetas de la misma forma que ficheros pero identificando el directorio con la "/" al final.

    mv ruta_origen/ ruta_destino/

También puedes cambiar el nombre de la misma forma:

    mv name_directory/ new_name_directory/

***
***NOTA***
El comando mover (mv) no modifica ni el usuario ni los permisos del directorio original.
***

## copiar directorios (cp -r) ##
Para copiar ficheros utilizaremos el comando "cp -r" el cual necesitará dos parámetros:

- El primero es la ruta de origen
- El segundo es la ruta destino

El comando seria de la siguiente forma:

    # cp -r ruta_origen_directory ruta_destino_directory

Este comando también se puede utilizar para cambiar el nombre del fichero:

    # cp -r origin_name_directory new_name_directory

***
***NOTA***
El comando copiar (cp -r) al hacer una copia del directorio indicado, se crea con los permisos del usuario que ejecuta el comando.
***

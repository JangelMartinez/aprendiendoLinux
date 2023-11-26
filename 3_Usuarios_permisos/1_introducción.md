# Introducción a usuarios y permisos #
En Linux es un sistema multiusuario. Esto significa que puede haber varios usuarios en el mismo sistema y se puede trabajar con cada uno de ellos o todos ellos a la vez.

Por defecto, cada usuario dispone una carpeta con el nombre del usuario en el directorio raiz "/home". Dentro de esa carpeta el usuario tiene todos los privilegios y puede crear, modificar o borrar todos las carpetas o archivos. En cambio, si trabaja fuera de ese directorio "/home/nombre_usuario/" podrá tener problemas al intentar realizar alguna acción. Para poder realizar esas modificaciones, necesitaras pedir permisos de administrador para realizarlas como 'root' (usuario administrador).

Depende de la distribución de Linux, se podría utilizar un comando diferente. Por ejemplo, en Ubuntu se utiliza la palabra 'sudo' o en Debian 'su' antes del comando para pedir permisos de administrador. Para eso necesitaras saber la contraseña de administrador, porque siempre te la pide.

## Permisos de usuario y de grupo ##
Los permisos se pueden dar a un usuario o a un grupo. 

Si listas un directorio (ls -l), encontraras delante del todo un código de letras de 10 carácteres que te indica que es y que permisos tiene.

El primer carácter te indica de que tipo es: d (directorio), - (archivo), l (link).
Los nueve caracteres siguientes te indica los permisos de usuario, grupo y otros. Cada uno de ellos tiene 3 carácteres.

Los permisos que existen son: w (escritura/write), r (lectura/read) y x (ejecución/execute). Depende de los permisos que e tenga, se podrá realizar ciertas acciones u otras. Si algún permiso está con el '-' significa que no tiene permiso.

Para los directorios, la r(lectura/read) significa que puede listar, w (escritura/write) significa que podemos crear, modificar y eliminar los elementos que hay dentro del directorio (no lo que hay dentro de cada elemento) y x (ejecutar/execute) signfica que podemos acceder a dicho directorio.


Ejemplos:

    drwxrwxrwx -> indica que es un directorio y tiene permisos para escribir, leer y ejecutar tanto en el usuario, como el grupo y en otros.

    -r-xr-xr-x -> indica que es un archivo y tiene permiso de usuario, grupo y otros para lectura y ejecución.

Un usario, pertenece a un grupo, por defecto, el grupo del mismo usuario. Pero se puede crear un grupo con unos permisos específicos e incorporar el usuario en dicho grupo para que pueda realizar dichas acciones sin problemas.

Dentro del listado de ficheros vemos varias columnas:

- La primera donde indica el tipo que tiene y los permisos
- También dispones la columna del nombre del usuario
- Despues la columnas del grupo al que pertenece el usuario por defecto
- El tamaño que tiene el fichero o carpeta
- La fecha de creación
- El nombre del fichero o carpeta

## Comandos ##

Para saber que usuario eres se puede mirar delante del promt donde te indica normalmente el usuario y la ruta donde estas de la siguiente forma:

    usuario@~#  -> Indica que tu usuario es "usuario" y estas en tu carpeta personal "/home/usuario/

En caso de no verlo, puedes averiguarlo con el comando:

    # whoami

También puedes ver a que grupo perteneces con:

    # groups

Puedes ver el usuario y a que grupos perteneces con:

    # id

Si quieres ver a que grupos pertenece un usuario solo tienes que escribir:

    # id nombre_usuario

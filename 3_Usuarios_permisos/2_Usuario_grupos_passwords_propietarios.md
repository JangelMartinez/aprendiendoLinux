# Usuarios #

## Crear un usuario ##

Para crear un usuario tienes que ser root (administrador del sistema). Para ello tendremos que utilizar el comando:

Ubuntu

    # sudo root

Te pedirá contraseña de root para acceder a él.

Una vez que ya estás en root podrás añadir usuarios con:

    # adduser nombre_usuario

En consola te indicará que va haciendo. Cuando termina, te pide el password para ese usuario que tendrás que confirmar y te pedirá los datos de ese usuario (no es necesario rellenarlos).

## Crear grupo ##

Dentro del usuario root, podemos crear un grupo con:

    # addgroup nombre_grupo

Para añadir un usuario al grupo nuevo se utilizará:

    # usermod -g nombre_grupo nombre_usuario

De esta forma, modificamos el grupo del usuario (usermod -g) con el grupo indicado al usuario indicado.

## Cambiar propietario:grupo de un fichero o carpeta ##

Cuando se crea un archivo o carpeta, por defecto se crea con el nombre y grupo por defecto de dicho usuario que lo ha creado.

Si quisieramos cambiar ese propietario y grupo, podriamos hacer:

    # chown usuario:grupo elemento_a_cambiar

chown (change own) -> Cambio de propietario

Puedes cambiar solo el usuario:

    # chown usuario elemento_a_cambiar

o cambiar el grupo:

    # chown :grupo elemento_a_cambiar

## Cambiar contraseña ##

Para cambiar la contraseña de un usuario necesitaras ser 'root' y se utilizará:

    # passwd nombre_usuario

Una vez ejecutado el comando te pedirá introducir un password y confirmarlo.


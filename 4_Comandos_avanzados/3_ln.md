# Enlaces ln #

El comando "ln" crea un enlace a un elemento del sistema de ficheros.

Por defecto crea un enlace duro. Un enlace duro es un puntero a la información de disco.

Un enlace blando apunta a la ruta. Normalmente utilizado en los directorios.

Opciones:

    -s -> Crea un enlace simbólico (o blando)

## Enlace duro ##
Un enlace duro se muestra en la lista de comandos como un fichero más pero te indica, despues de los permisos, cuantos archivos existen.

Cuando se crea enlaces duros, con modificar el valor de uno de los enlaces duros, cambiará en todos.

Si eleminas un enlace duro, no se borrará la información hasta que se borre el último fichero existente (sea enlace o fichero).

Al mostrar el total del tamaño de un directorio con enlaces fuertes realizando un **'ls -lh'** nos mostrara un tamaño irreal ya que al mostrarse como archivos normales, cuenta todos los archivos. Pero si se utiliza el comando **'du -sh .'** nos mostrará el tamaño real ya que los enlaces no ocupan espacio en disco.

***Ejemplo***

    # ln /etc/apt/sources.list ~/repos

    Crea un enlace fuerte llamado repos en mi directorio home que tendrá la misma información que el sources.list.

    ---

    # ls -l

    -rw-r--r-- 2 usuario usuario 10 nov 13 20:46 mifichero2
    -rw-r--r-- 2 usuario usuario 10 nov 13 20:46 mifichero


## Enlace blando ##

Si creas un enlace blando se muestra en la lista de comandos con un 'l' delante de los permisos y el nombre del archivo con una flecha al archivo del que se ha creado.

Si elimino el fichero original del enlace simbólico ya no puede enlazar a él y el enlace simbólico puede aparecer en color rojo indicando que ya no se puede utilizar.

***Ejemplo***

    # ln -s /var/cache/apt/archives/ /paquetes/

    Crea un enlace simbólico llamado paquetes, que irá a /var/cache/apt/archives/

    ---

    # ls -l

    lrwxrwxrwx 1 usuario usuario 10 nov 13 20:46 mifichero_s -> mifichero


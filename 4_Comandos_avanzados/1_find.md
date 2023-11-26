# Find #

Es un comando muy potente para hacer búsquedas en el sistema de ficheros.

Busca de forma recursiva en un directorio todos los ficheros que cumplan ciertas condiciones.

Sintaxis:

    # find path options

## Opciones ##

Se puede hacer búsquedas por nombre utilizando la opción ***-name*** distinguiendo entre mayúsculas y minúsculas. Si no quieres hacer la distinción se puede utilizar la opción ***-iname***. El valor siempre se pone entre comillas.

    # find . -iname '*.mp3'

    Busca todos los ficheros que haya en el directorio actual recursivamente con la extensión .mp3

    # find . -iname '*i*'

    Busca todos los ficheros y directorios que dispongan de una 'i' en su nombre.

También se puede hacer búsquedas por el tipo de archivo con la opción ***-type***

    d -> directory (directorios)
    f -> files (archivos)
    l -> links (enlaces simbólicos)
    b -> dispositivos de bloque
    c -> dispositivos de carácter
    p -> tuberias
    s -> sockets

Se puede utilizar de la siguiente forma:

    # find . -iname '*i*' -type d
    
    Busca todos los elementos de tipo directorio que contengan una 'i'.

Otra opción que se puede utilizar es la búsqueda por tamaño con la opción ***-size*** utilizando el símbolo '+' o el '-' para referirse a que sea mayor o menor que :

    -size +/-<n>

    Donde n es un número con una magnitud específica:

    - c -> Bytes
    - k -> Kilobytes
    - M -> Megabytes
    - G -> Gigabytes

    Si no se utiliza la magnitud n será el número de bloquess de 512 bytes.

Un ejemplo seria el siguiente:

    # find -size +2M

    Busca archivos en el directorio actual recursivamente archivos con tamaño superior a 2 Megabytes.

    # find -size -1G

    Buscar archivos en el directorio actual recursivamente archivos con tamaño inferior a 1 Gigabytes

Si quieres buscar por permisos también se puede hacer con la opción ***-perm*** y el número de los permisos. Si lo utilizas acompañandolo con un guión '-' le estaras indicando que tiene que tener ese permiso/s en concreto. Si utilizas la barra '/' te buscará que tenga alguno de los permisos que hayas puesto.

    # find -perm 600

    Busca los elementos que tengan los permisos de lectura y escritura en los permisos de usuario y ninguno en los otros dos grupos de permisos.

    # find -perm +600

    En este caso se realiza la búsqueda obligatoria de lectura y escritura en el grupo de usuarios, pero los otros no son obligatorios.

    # find -perm /600

    Con la barra te indica que tiene que tener el permiso de lectura o el de escritura. No es necesario tener los dos.

Otra de las opciones que hay es realizar búsquedas por un cierto propietario o usuario mediante ***-user*** o por un cierto grupo ***-group***

    # find -user nombre_usuario

    Buscar todos los elementos que el propietario sea el nombre_usuario que has introducido

    # find -group nombre_grupo

    Busca todos los elementos que tenga el nombre del grupo que has instroducido.

***Ejemplo con varias opciones ***

    # find . -type f user nombre_usuario -perm /200

Realiza una búsqueda con todas las características definidas y que las contenga todas ellas:

    . -> directorio actual

    -type f -> que sea de tipo archivo
    
    -user nombre_usuario -> que sea de un usuario determinado
    
    -perm /200 -> que contenga como mínimo el permiso de escritura(w)

Los ficheros que contemplen todas estas opciones, te apareceran en el listado.

## Opciones de tiempo ##

Otras opciones de búsquedas son las de tiempo.

    -mmin +/-minutos -> hace búsqueda por fecha de modificación que sea mayor o menor al tiempo en minutos que le indiques

    -mtime +/-n -> hace búsqueda por fecha de modificación donde n es el número de días. La n es multiplicada por 24horas internamente.

Ejemplos:

    # find -mmin -50 

    Hace la búsqueda de ficheros que se haya modificado dentro de los últimos 50 minutos

    # find +mtime 3

    Hace la búsqueda de ficheros que se hayan modificado sea más antigua de 72 horas o 3 días (3*24horas)

## Ejecutar comandos en una búsqueda de find ##

Puedes realizar una búsqueda de find y por cada resultado ejecutarse un comando que te interese.

Para eso, puede utilizar la opción ***-exec***

Sintaxis:

    -exec <comando>

    La cadena '{}' se sustituye por cada elemento encontrado. El símbolo ';' indica el fin del comando. Tanto un símbolo como el otro tiene que ir entre comillas.

***Ejemplo***

    # find /etc/ -iname "*.conf" -type f -size -1M -exec cp '{}' /home/copias/ ';'

    Copia todos los ficheros que tengan extensión .conf y que sean menor de 1 Megabyte al directorio /home/copias

    # find ~ -size +2G -exec rm '{}' ';'

    Elimina todos los ficheros de nuestro directorio persona (/home/Nombre_usuario) que sean mayores a 2 Gigabytes.
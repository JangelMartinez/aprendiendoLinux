# Redirecciones #

Cuando un comando produce unos resultados en modo texto, los envía a la salida estándar del sistema, que de forma prederterminado es el monitor.

Algunos ejemplos son el comando echo, cat, etc..

Este comportamiento se puede cambiar con el simbolo '>' o '>>'.

***Ejemplos***

    # echo "Hola Mundo" > saludo.txt

    Con este redireccionamiento, en vez de sacar la información por pantalla hace que lo guarde en un fichero llamado "saludo.txt"

Si se utilizar el simbolo '>' si el fichero existe, lo sobreescribe.

Si se utiliza el simbolo '>>' si el fichero existe, añade el texto al final.

Si hay algún error se visualizará por pantalla.

## Redirigir errores ##

Igual que se redirigen los resultados de texto, se pueden redirigir los errores.

Para redirigir los errores se de de utilizar '2>' o '2>>' . 

## Redirigir mensajes y errores ##

Se pueden redirigir tanto los mensajes de texto como los errores con '&>' o '&>>' .

## Redirigir la entrada de texto ##

También se puede reidirigir la entrada de texto, para ello utilizamos el carácter '<', que enviará la información que lee de un fichero al comando.

***Ejemplos***

    # sort < listado

Ordena la información que tiene el fichero listado.

    # mysql < db_backup.sql

El comando mysql ejecuta las instrucciones que hay dentro del fichero db_backup.sql

## Desechar información ##

Si queremos desechar alguna salida, podemos usar el dispositivo /dev/null. Enviar texto hará que no aparezca ni se guarde en ningún sitio.

    # grep -r max_size /etc/* &> /dev/null

    La información no aparecerá ni por pantalla ni se guardará en ningún archivo.
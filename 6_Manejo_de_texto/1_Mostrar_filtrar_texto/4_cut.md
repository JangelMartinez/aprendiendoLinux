# Comando #

Muestra sólo una parte e cada línea. Hace u "corte" vertical.

Opciones:

    -c -> selecciona solo los carácteres que le indiquemos. Se puede utilizar números independientes separados por comas o dos números separados por guión para indicar el inicio y el fin de un rango. Si alguno no está presente se entiende que será el inicio o fin de línea.

    # cut -c 5,10 file.txt
    # cut -c 7-25 file.txt

***
    -d -> Indica un carácter separador entre los distintos campos de una línea. Así podremos seleccionar la información por columnas. Por defecto es el carácter tabulador.

    -f -> Elige las columnas que queremos que se muestren. La forma de seleccionar funciona igual que para la opción '-c'.

    # cut -d":" -f1 file

Ejemplos:

    # cut -c1 file.txt

    Solo te muestra el primer carácter de cada línea del fichero.

    # cut -c1-10 file.txt

    Te muestra desde el primer carácter hasta el número 10 de cada línea del fichero.

    # cut -c8,15 file.txt

    Solo mostraria 2 caráteres de cada línea. El que está en posición 8 y la que está en la posición 15

    # cut -c 1-3,10-15,25 file.txt

    En este caso, juntamos las dos posibilidades mostrandonos:
    - los carácteres 1 al 3
    - los carácteres 10 al 15
    - el carácter 25

Ejemplos con -d y -f :

    # cut -d":" -f1 /etc/passwd

    Separa en columnas por el carácter ":" y solo muestra la primera columna del fichero /etc/passwd.
    De esta forma solo mostrará el nombre de los usuarios que hay en el fichero.

    # cut -d":" -f1,4,7,8-10 /etc/passwd

    Te muestra las columnas que le indicas por rango o individual.

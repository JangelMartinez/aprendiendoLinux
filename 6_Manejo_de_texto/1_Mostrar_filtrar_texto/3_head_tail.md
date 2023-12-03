# Comando head y tail #

## head ##
Este comando te muestra las primeras  10 lineas del archivo.

    # head fichero

## tail ##
Este comando te muestra las últimas 10 lineas del archivo.

    # tail fichero

## Opciones comunes de head y tail ##
Con la opción -n y un número te muestra las líneas que le has indicado. También se puede indicar sin la 'n' y poniendo el número (-20)

***head***

    # head -n1 fichero

    Te muestra la primera línea

    # head -n20 fichero

    Te muestra las 20 primeras líneas

    # head -30 fichero

    Te muestra las 30 primeras líneas

***tail***

    # tail -n1 fichero

    Te muestra la última línea

    # tail -n20 fichero

    Te muestra las 20 últimas líneas

    # tail -30 fichero

    Te muestra las 30 últimas líneas

Pueden leer varios ficheros a la vez

    # head *.log
    # tail *.log

Te muestra una cabecera con el nombre del archivo y despues las líneas de ese fichero.

Con la opción '-q' quita los nombres de los ficheros.
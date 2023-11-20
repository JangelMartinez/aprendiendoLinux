# Comodines #
Cuando realizas cualquier comando, puedes utilizar en cualquier parámetro de los comandos los comodines del arterisco y/o interrogante.

Se pueden utilizar tanto uno, como los dos en el mismo parámetro.

## Arterisco (*) ##
El arterisco se utiliza para un número indeterminados (0 - infinito) de letras.

***
***Ejemplo con arterisco***

Este ejemplo moverá todos los ficheros con extensión gif que hay en el directorio actual a otro directorio.

    mv *.git /directory

Este ejemplo copia todos los ficheros que empiecen por la letra h a otro directorio.

    cp h* /directorio

Este ejemplo buscará todos los directorios o ficheros que contenga un 2 (al principo, al medio o al final) que haya en el directorio actual

    ls -l *2*


## Interrogante (?) ##
El interrogante se utiliza para un solo caracter de la palabra (no se lo puede saltar). Sirver para cualquier letra del abecedario, número, simbolo, etc..

***
***Ejemplo con interrogante***

Este ejemplo moverá todos los ficheros que empiecen por "cas" y otro caracter que hay en el directorio actual a otro directorio.

    mv cas?.txt /directory

En el ejemplo anterior si el interrogante fuera una vocal podría listar ficheros con el nombre "casa.txt", "case.txt", "casi.txt", "caso.txt", "casu.txt". 

Este ejemplo copia todos los ficheros que empiecen por la letra h a otro directorio.

    cp ?ola /directorio

En el ejemplo anterior podría listar nombres como: "bola", "cola", "hola", "mola", etc..

Este ejemplo buscará todos los directorios o ficheros que contenga un 2 al principio y que sea solo de 2 caracteres que haya en el directorio actual

    ls -l 2?

## Los dos comodines ##
Se pueden utilizar los dos comodines indistintamente en el mismo o distintos parámetros.

***Ejemplos con los dos comodines***

En este ejemplo queremos listar cualquier directorio o fichero que empiece por un carácter cualquiera, despues siga con "ola" y detrás no contenga nada, uno o más carácteres.

    ls -l ?ola*

Por ejemplo podrá listar palabras como: "bola", "cola", "bolas", "colación", "molas", etc..

Otro ejemplo seria al revés, da igual como empiece y con cuantos carácteres, pero debe de ir seguido de "ola" y terminada con un carácter cualquiera:

    ls -l *ola?

Con esta búsqueda se podría listar palabras como: "olas", "bolas", "colas", "caracolas", "gominolas", etc..
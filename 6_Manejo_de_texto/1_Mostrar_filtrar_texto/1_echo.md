# Comando echo #

Este comando muestra el texto que recibe.

Opciones:

    -e -> interpreta los carácteres especiles despues de \

***Interprete de carácteres para utilizar con la opción -e***

    \n -> salto de línea
    \t -> tabulador

Para ver más opciones de carácteres pues teclear:

    # man echo

    Te saldrá la explicación de lo que hace el comando y todas las opciones de carácteres que tiene.

***Comillas dobles y simples***

Las comillas dobles interpreta las opciones y variables de entorno que se indica dentro del string

Las comillas simples no interpreta nada y lo deja tal cual está escrito

Ejemplo:

    # echo "usuario ==> $USER"

    usuario ==> root

    # echo 'usuario ==> $USER'

    usuario ==> $USER

***
***NOTA:*** 
si que interpreta los carácteres mediante la \ como el salto de línea o el tabulador.
***
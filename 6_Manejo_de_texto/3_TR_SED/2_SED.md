# Comando SED #

Este comando lee y modifica línea a línea mediante un script especificado

    # sed [-n] [-e'script'] [-f archivo] archivo1 archivo2

Opciones:

    -n -> indica que se suprima la salida estándar
    -e -> indica que se ejecute el script que viene a continuación
    -f -> indica que las órdenes se tomarán de un archivo
    -r -> se utilizan expresiones regulares EXTENDIDAS

## Sintaxis del script ##

    [ inicio_ubicación [,fin_ubicacion]] instrucción [ argumentos ]

***Ejemplo***

    # sed '2,5p' texto.txt

    sed -> comando
    2 -> inicio_ubicación
    5 -> fin_ubicación
    p -> instrucción
    texto.txt -> argumentos


### Ubicación ###

Si no se especifica se verán afectadas todas la líneas.

Se pude indicar de dos formas:

1. Mediante números: Especificamos los núeros de línea de principio y fin. ("$" significa la última línea)
2. Mediante patros de texto: son las líneas que cumplen con la expresión regular especificada /EXPRESION/

En los dos métodos se pueden aplicar rangos, indicando el inicio y fin separados por comas

    1,5 -> de la línea 1 a la 5
    /pepe/, $ -> desde línea que contiene la palabra pepe hasta la última.

### Instrucciones ###

    i\ -> Insertar línea antes de la línea actual
    a\ -> Insertar línea después de la línea actual
    c\ -> Sustituye la linea catual por la especifiada a continuación
    d -> borra línea actual
    p -> Imprimir línea actual en salida estándar ( Se utiliza con la opción -n)
    s -> Sustituir cadena en línea actual
    ! -> Aplicar instrucción a las líneas no seleccionadas por la condición
    q -> Abandona el proceso cuando se alacanza la línea especificada.

***Ejemplos***

Elimina de la línea 1 a la 5 del fichero 'texto.txt'

    # sed -e '1,5d' texto.txt

Elimina la línea en la que encuentra la palabra 'Mancha'

    # sed -e '/Mancha/d' quijote.txt

Elimina las líneas desde que encuentra la palabra 'Mancha' hasta la línea 10 indicada.

    # sed -e '/Mancha/,10d' quijote.txt





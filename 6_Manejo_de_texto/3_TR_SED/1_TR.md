# Comando TR #

El comando TR sustituye o elimina carácteres de la entrada estándar.

    # tr a e

    Sustituye la vocal a por la e

    Si se escribe 'casa' y se pulsa intro, cambiará la palabra a 'cese'

    Con ctrl + c se sale del comando.

Opciones:

    -d -> elimina las letras indicadas
    -s -> elimina el caracter que esté repetido
    -c ->

## Rangos ##

Se puede utilizar rangos de carácteres utilizando el símbolo del guión '-'.

    a-z incluye todas las minúsculas
    d-g incluye las letras 'defg'

## Repeticiones ##

Se puede utilizar repiticiones mediante '[caracter*número]'

    [a*3] indica la cadena aaa

## Carácteres especiales ##

    \\: Barra invertida
    \a: Carácter audible (Campana/Bell)
    \b: Retroceso
    \f: Salto de Página
    \n: Nueva línea
    \r: Retorno de carro
    \t: Tabulador
    \v: Tabulador vertical

## Clases ##

Las clases representan un conjunto predifinido de carácteres.

    [:alnum:] : Las letras y Dígitos
    [:alpha:] : Letras
    [:blank:] : Espacios en blanco
    [:cntrl:] : Carácteres de control
    [:space:] : Los espacios en blanco verticales y horizontales
    [:graph:] : Carácteres imprimibles, sin incluir el espacio en blanco
    [:print:] : Carácteres imprimibles, incluyendo el espacio en blanco
    [:digit:] : Dígitos
    [:lower:] : Letras minúsculas
    [:upper:] : Letras mayúsculas
    [:punct:] : Sígnos de puntuación
    [:xdigit:] : Dígitos Hexadecimales

***Ejemplos***

    # echo "Esto es una frase. Con varias palabras por ejemplo 15 ollas" > fichero.txt

    Crea el fichero 'fichero.txt' con la frase indicada.

    # tr [:digit:] X < fichero.txt
    
    Coge la frase de dentro del fichero 'fichero.txt' y sustituye los dígitos por una X quedando de la siguiente forma:

    Esto es una frase. Con varias palabras por ejemplo XX ollas

    # tr [:alpha:] X < fichero.txt
    
    Coge la frase de dentro del fichero 'fichero.txt' y sustituye las letras por una X quedando de la siguiente forma:

    XXXX XX XXX XXXXX. XXX XXXXXX XXXXXXXX XXX XXXXXXX 15 XXXXX


Elimina la letra a de un texto

    # tr -d a < fichero.txt

    El texto quedaria de la siguiente forma:

    Esto es un frse. Con vris plbrs por ejemplo 15 olls



Elimina la letra repetida de un texto

    # tr -s l < fichero.txt

    El texto quedaria de la siguiente forma:

    Esto es una frase. Con varias palabras por ejemplo 15 olas
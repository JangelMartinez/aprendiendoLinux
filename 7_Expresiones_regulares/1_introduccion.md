# Expresiones Regulares #

Las expresiones regulares son un conjunto de carácteres que hacen referencia a como tiene que estar constituida una palabra, frase, etc.. que estamos buscando o verificando.

Se pueden utilizar en varios comandos de linux como RD o SED, pero además se utilizan también, por ejemplo, en la programación.

## Carácteres especiales ##

    ^ (acento circunflejo) -> Inicio de línea
    $ -> Fin de línea
    . -> cualquier carácter. Si queremos quitar el signficado especial tendremos que poner la contrabarra \ delante
    [] -> se usan para indicar que en una posición determiada pueden aparecer un conjunto determinada de caracteres. Por ejemplo [aeiou] siginfica donde se encuentre puede haber cualquier volcal minúscula.

***Ejemplo***

    La expresión regular ^c[aei]s[ao]$
    
    Coincidira con palabras como 'casa', 'caso', 'ceso', 'cisa' y 'ciso'. En cambio no coincidiran con 'casi','case','casu', 'cese', 'cesi', 'cise' 'cosa', etc..

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

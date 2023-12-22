# Otras opciones de expresiones regulares #

## Alternativa - OR ##

Se puede usar el operador lógico OR(|) para dar por buena cualquiera de las dos expresiones regulares conectadas.

***Ejemplo***

    ^a.*t$|^e.*x$ 
    
    Palabras que empiecen por a y acaben en t o las que empiecen por e y acaben por x 

## Agrupación - () ##

Se puede usara paréntesis para agrupar expresiones regulares o especificar a que se debe afectar un determinado carácter especial.

***Ejemplo***

    (c[aeiou]){2}

    se tiene que repetir una c seguida de una vocal 2 veces

## Abreviaturas ##

    \w -> cualquier carácter alfanumerico y el guión bajo(_)
    \W -> lo contrario de \w, signos de puntuación, espacios, etc..

## Límites de palabra ##

No representan carácteres, sino límites, estarías entre dos carácteres, normalmente entre un alfanumérico y uno de puntuación o separadores.

    \< -> Inicio de palabra
    \> -> Fin de palabra
    \b -> Límite de palabra (inicio o fin)
    \B -> Lo contrario a \b

## Referencias ##

Podemos usar \n siendo n n número entre 1 y 9 para hacer referencia a una agrupación dentro de la propia expresion regular.

***Ejemplo***

    ([aei])s\1

    Significa que el primera carácter puede ser a, e o i, luego una s y el \1 haría referencia que tiene que haber lo mismo que haya en el primer carácter

    ([[:digit:]])([[:digit:]])0\2\1

    Expresa que tiene que haber dos números seguidos de un 0 y después el mismo número que esté en la segunda posición, seguido del mismo número que esté en la primera. Es decir, capicúa, como 13031, 91019
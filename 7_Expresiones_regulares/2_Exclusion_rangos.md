# Exclusiones y rangos #

## Corchetes ##

### Exclusion ###

    ^ -> Se usa para indicar que en una posición puede encontrarse cualquier carácter excepto los que se encuentran entre corchetes.

***Ejemplos***

    La expresión ^c[^aei]s[^ao]$

    Coincide con las palabras 'cose', 'cusi', pero no coincidiria con 'casa', 'cese', 'coso'.

### Rangos ###

    - -> Se usa para indicar todos los valores intermedios entre un inicio y un final. Tienen que ser datos con una ordenación conocida, por ejemplo números o letras.

***Ejemplos***

    La expresión c[a-d]s[0-5] seria lo mismo que indicarle c[abcd]s[012345]

---
***Nota***

Las expresiones se pueden mezclar, por ejemplo: [3-8[:upper:]mty] en esta posición se admiten números del 3 al 8 o cualquier mayúscula o las minúsculas m, t o y
---


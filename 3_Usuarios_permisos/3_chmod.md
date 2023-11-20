# Chmod #
Es el comando que hace cambios de permisos en los elementos (ficheros o directorios) que le indiques.

Dispone de varias opciones para realizar los cambios de permisos:

    u -> indica que es para los permisos de usuario
    g -> indica que es para los permisos de grupo
    o -> indica que es para los permisos de otros

Los simbolos que puedes utilizar son:

    + -> para añadir permisos
    - -> para eliminar permisos
    = -> para indicarle que permisos va a tener 

Los permisos que puedes modificar son:

    r -> lectura (read)
    w -> escritura (write)
    x -> ejecución (execute)

## Añadir permisos ##

Para añadir permisos utilizaremos el comando chmod y con el simbolo + le añadiremos las letras de los permisos que queremos al elemento seleccionado.

***Ejemplos:***

- Añadimos el permiso de lectura en todos sus grupos de permisos (usuario, grupo y otros) al archivo carta.txt

        # chmod +r carta.txt

- Añadimos el permiso de lectura en los permisos de usuario al archivo carta.txt

        # chmod u+r carta.txt

- Añadimos el permiso de lectura en los permisos de usuario y el de escribir en los permisos de grupos al archivo carta.txt

        # chmod u+r,g+w carta.txt

## Eliminar permisos ##

Para eliminar permisos utilizaremos el comando chmod y con el simbolo - le añadiremos las letras de los permisos que queremos al elemento seleccionado.

***Ejemplos:***

- Eliminamos el permiso de lectura en todos sus grupos de permisos (usuario, grupo y otros) al archivo carta.txt

        # chmod -r carta.txt

- Eliminamos el permiso de lectura en el grupo de usuario al archivo carta.txt

        # chmod u-r carta.txt

- Eliminamos el permiso de lectura en los permisos de usuario y el de escribir en los permisos de grupos al archivo carta.txt

        # chmod u-r,g-w carta.txt

## Indicar directamente los permisos ##

Para indicarle los permisos directamente sin añadir ni eliminar, utilizaremos el símbolo =. 

Con este símbolo le diremos que permisos va a tener. En caso de no tener los que le indiquemos, se los añadirá. En caso de que tenga permisos que nosotros no le hemos dicho, los eliminará.

***Ejemplo:***

Le indicamos que en los permisos de usuario solo debe tener permisos de escritura.

    # chmod u=w carta.txt

Le indicamos que en los permisos de usuario tiene opción de lectura y escritura, en los permisos de grupo tiene opción de lectura y no va a tener ninguna opción en los permisos de otros

    # chmod u=rw,g=r,o= carta.txt

## Cambiar permisos por números ##

Para cambiar los permisos por número hay que utilizar el binario convertido a decimal.

El número binario solo dispone de 2 opciones: SI/verdadero (1), NO/falso (0).

Hay que tener en cuenta que hemos indicado que cada grupo de permisos dispone de 3 elementos (r, w, x). Cada elemento dispone de 2 opciones: SI tiene permiso (1), NO tiene permiso (0).

Por lo que si cogemos, por ejemplo, el primero grupo de permisos (usuario), tendremos que verificar que permisos tiene y cuales no tiene para convertirlo a un número binario.

Ejemplo 1:

    todos los permisos habilitados:
    r w d

    En binario seria todo 1 al ser todo verdadero (habilitado)
    1 1 1 

Ejemplo 2:

    lectura y escritura habilitados
    r w -

    En binario seria poner a 1 los verdadederos (habilitados) y 0 los falsos (deshabilitados)
    1 1 0

Ejemplo 3:

    No tiene permisos habilitados
    - - -

    El binaria seria todo 0 al ser todo falso (deshabilitado)
    0 0 0

Una vez pasado a binarios hay que realizar la operación para pasarlo a decimal.

Para realizar esto hay que tener en cuenta varias cosas:
- que número (0 o 1) hay en cada posición y la posicion siempre empieza por el número 0
- La posición siempre empieza por la derecha. Es decir, la posición 0 será el número que esté más a la derecha e irá aumentando según vayamos en dirección a la izquierda
- La pontencia de un número elevado a cero siempre es 1.
- En este caso, como solo tenemos 3 posiciones, serán la posición 0, la posición 1 y la posición 2.
- Un número binario de 3 posiciones solo puede tener un rango de de 0 a 7, que son 8 números(2³ = 8 -> 2 opciones elevado a 3 posiciones). Como siempre se cuenta el 0, el número máximo seria 7.
- Cada posición tiene que ser multiplicado por 2 (número de opciones que tiene - 0 y 1) elevado al número de la posición en la que está
- El resultado de cada posición, se deben de sumar para saber el resultado final.

Siguiendo lo dicho anteriormente se quedaria la formula siguiente:

    resultado = posicion2*2² + posicion1*2¹ + posicion0*2⁰

***Ejemplo:***
***

Siguiendo el patrón de permisos:

    rwx r-x ---

Podemos separarlo en tres resultados:

**1 resultado**

Todos los permisos tendría un binario de 1 1 1 por lo que siguiendo la formula quedaria:

    resultado = 1*2² + 1*2¹ + 1*2⁰
    resultado = 4 + 2 + 1
    resultado = 7

**2 resultado**

Solo tiene permisos de lectura y ejecución (r - x) con lo que el binario quedaria 1 0 1. Realizando la formula:

    resultado = 1*2² + 0*2¹ + 1*2⁰
    resultado = 4 + 0 + 1
    resultado = 5

**3 resultado**

No tiene permisos por lo que el binario seria 0 0 0 con lo que la formula quedaria:

    resultado = 0*2² + 0*2¹ + 0*2⁰
    resultado = 0 + 0 + 0
    resultado = 0

Una vez que ya hemos calculado el número de cada grupo de permisos, podriamos realizar el cambio de permisos con números siguiendo el siguiente formato:

    chmod 750 cartas.txt

Este comando indica lo siguiente:

- 7 -> le pone todas las opciones, lectura, escritura y ejecución a los permisos del usuario
- 5 -> le pone lectura y ejecución a los permisos de grupo
- 0 -> no incorpora ninguna opción a los permisos de otros.

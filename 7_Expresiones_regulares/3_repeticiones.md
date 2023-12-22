# Repeticiones #

Las expresiones regulares se dividen en estándar y en extendidas. Para las repeticiones se va a explicar las expresiones regulares extendidas ya que en el estandar es mucho más lioso.

    X* -> El arterisco concuerda con cero o más repeticiones de la expresion regular que le precede (X).
    X? -> La interrogación concuerda con cero o una aparición de la expresión regular que le precede (X).
    X+ -> El signo más concuerda con una o más repeticiones de la expresión regular que le precede (X).
    X{n} -> Concuerda con n repeticiones exactas de X
    X{n,} -> Concuerda con n o más repeciones de X
    X{,n} -> Concuerda con cero o a lo sumo n repeticiones de X
    X{n,m} -> Concuerda con al menos n repeticiones de X o como mucho m repeticiones.

---
***Nota***

Para utilizar las expresiones regulares extendidas, hay que utilizar en los comandos algunas opciones adjuntas.

Por ejemplo:

    # grep -E expresion_regular_extendida archivo

    El -E indica que vas a utilizar una expresión regular extendida.

---

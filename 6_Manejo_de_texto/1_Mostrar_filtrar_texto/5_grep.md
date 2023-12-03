# Comando grep #

Muestra sólo las líneas que cumplen con un patrón. Se puede usar palabras o expresiones regulares.

Opciones:

    -v -> Muestra las que NO coinciden con el patrón

    -l -> Sólo indica el nombre del fichero donde ha encontrado alguna coincidencia

    -w -> El patrón tiene que ser una palabra independiente

    -n -> Indica el número de línea

    -i -> No distingue entre mayúscula y minúscula

    -c -> Muestra la cantidad de líneas que cumplen con el patrón

    -r -> Busca en los ficheros de forma recursiva

***Ejemplos***

    # grep al file.txt

    Te muestra todas las líneas que aparecezcan las letras 'al' juntas.

    # grep -v al file.txt

    Te muestra todas las líneas que no contenga las letras 'al' juntas

    # grep hola -l /directorio/*.log

    Te muestra todos los nombres de ficheros que contenga la palabra 'hola' dentro de ellos.

    # grep 100 file.txt

    Te muestra todas la líneas que contengan el número 100 o que contengan el número 100 como, por ejemplo, el 1000.

    # grep -n hola file.txt

    Te muestra la línea que coincide y el número de línea que lo contiene.

    # grep -i A file.txt

    Por defecto linux distingue mayúsculas y minúsculas por lo que la opción -i hace que no las distinga. En este caso buscaría tanto 'A' como 'a'.

    # grep -c hola file.txt

    Te indica el número de coincidencias hay dentro del fichero con el conjunto de carácteres 'hola'.

    # grep -r  hola /directorio/*

    Busca de forma recursiva en todo el directorio, subdirectorios y archivos el conjunto de carácteres 'hola' indicando el nombre del fichero y las líneas en las que aparece.
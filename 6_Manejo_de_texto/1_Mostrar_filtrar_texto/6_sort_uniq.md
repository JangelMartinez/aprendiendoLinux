# Comando sort #

Te muestra las líneas ordenadas por orden alfabetico a - z

    # sort file.txt

Para ordenarlo descendentemente de la z - a se utilizará la opción '-r'

    # sort -r file.txt

Para ordenar de forma númerica utilizaremos la opción '-n'.

    # sort -n file.txt

Para ordenar con magnitudes (bytes,kilobytes, megabytes, etc..) utilizaremos la opción '-h'

    # sort -h file.txt

# Comando uniq #

Trabaja con líneas de texto identicas. Elimina todas las líneas iguales y que estén juntas.

    # uniq file.txt

Opciones:

    -d -> Muestra solo las líneas que están repetidas

    -i -> Ignora la diferencia entre mayúsculas y  minúsculas

    -c -> Cuenta las veces que una línea está repetida

***Ejemplos***

    # uniq -i file.txt

    Elimina las líneas que están repetidas y aunque no coincidan mayúsculas y minúsculas.

    # uniq -d file.txt

    Solo mostrara la línea que ha sido repetida.

    # uniq -id file.txt

    Solo mostrará las líneas que han sido repetida aunque no coincidean mayúsculas y minúsculas.

    # uniq -ic file.txt

    Te mostrará las líneas que han sido repetidas aunque no coincidan mayúsculas y minúsculas y no indicará delante cuantes veces se ha repetido.
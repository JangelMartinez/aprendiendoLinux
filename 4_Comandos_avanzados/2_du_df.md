# Comandos df y du #

Estos comandos se usan para ver información de los discos duros.

## df (disk free) ##

Este comando nos da información sobre la particiones del sistema: tamaño total, usado y libre.

Se puede usar sin argumentos u opciones, pero la opción -h nos ayuda a interpretar mejor las cifras que nos muestra.

Si le pasamos como parámetro cualquier directorio nos dará la información de la partición donde se encuentra ese directorio.

***Ejemplo***

    # df -h

    S.ficheros  Size    Used    Disp.   Use%    Mounted in
    /dev/sda1   916G    22G     848G    3%      /
    tmpfs       1,2G    2,1M    1,2G    1%      /run
    tmpfs       5,8G    17M     5,8G    1%      /dev/shm
    tmpfs       5,0M    4,0K    5,0M    1%      /run/lock
    tmpfs       1,2G    128K    1,2G    1%      /run/user/1000
    /dev/sda2   511M    6.1M    505M    2%      /boot/efi

    ---

    # df -h /home/usuario

    S.ficheros  Size    Used    Disp.   Use%    Mounted in
    /dev/sda1   916G    22G     848G    3%      /


## du (disk usage) ##

Muestra el espacio de disco ocupado por un fichero o por un directorio. Si le pasaos un directorio mostrára recursivamente el tamaño de todos los subdirectorios.

Opciones:

    -s -> si le pasamos un directorio, solo mostraré el tamaño del directorio y no de los subdirectorios

    -h -> muestra el tamaño en KB, MB, etc..

***Ejemplo***

    # du -sh /*

    Muestra en formato "humano" el total de lo que ocupa todos los elementos de la raíz del sistema.

    ---

    # du -sh * | sort -h

    Muestra en formato "humano" los archivos del directorio actual ordenados (sort) de menor a mayor.


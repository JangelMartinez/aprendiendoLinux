# Comando cd (directorios) #
Para cambiar de directorio se utiliza el comando "cd" (change directory) y se puede utilizar con rutas absolutas y relativas.

    # cd ruta_relativa

o

    # cd ruta_absoluta

En todos los directorios existen dos opciones que son el "." y el ".." que ayudan a ubicar las rutas relativas.

    . -> indica la ubicación actual
    .. -> retrocede al directorio anterior

## Ruta relativa ##
Las **rutas relativas** son aquellas que dependen de la ruta donde estas actualmente. 

Utiliza "./" para indicar que es a partir de la ruta actual o sin el "./" y sin "/" al principio.

***
***Ejemplos Rutas relativas***

Entra en la carpeta directory_1 en caso de que exista en la ruta actual en la cual estas

    # cd directory_1

Vuelves al directorio anterior al que estas actualmente

    # cd ..

Entrar en un directorio que está en la directorio anterior

    # cd ../directory_1

Entra en la ruta que estás introduciendo desde la ruta actual en la que estas en caso de que exista.

    # cd directory_1/subdirectory/

o

    # cd ./directory_1/subdirectory/

## Rutas absolutas ##
Las **rutas absolutas** son aquellas que disponen de toda la ruta desde la unidad de origen.

Utiliza siempre la "/" en el principio de la ruta
***
***Ejemplos Rutas absolutas***

Entra en la ruta que estás introducción en caso de que exista

    # cd /var/www/html

Un atajo para entrar en tu directorio personal sin utilizar la ruta absoluta

    # cd

o

    # cd ~


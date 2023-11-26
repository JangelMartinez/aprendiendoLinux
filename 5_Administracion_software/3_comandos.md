# Comandos para administración de software #
Recuerde que todos estos comando se deben utilizar con el usuarios de administración del sistema root

## Actualizar aplicaciones (paquetes) existentes en el repositorio ##

Para actualizar la lista de aplicaciones (paquetes) en los repositorios utilizaremos el comando:

Ubuntu:

    # apt-get update

## Buscar paquetes en el listado ##

Se puede realizar una búsqueda de un software en particular o que contenga de unos carácteres correspondiente.

Busca tanto en el nombre como en la descripción de la lista de software.

    # apt-cache search software_a_buscar

    # apt-cache search palabra_a_buscar

## Instalar un paquete ##

Para instalar un paquete determinado se utilizará el comando:

    # apt-get install nombre_software

Una vez ejecutado, te indicará que paquetes se van a instalar, ya que algunos de ellos dependen de otros y podría ser que para utilizar un software, se tengan que instalar varios paquetes.

## Desinstalar un paquete ##

Para desintalar un paquete es mucho más rápido al no tener que descargarse nada y es bastante sencillo.

    # apt-get remove nombre_software

Igual que en la instalación, te indicará que paquetes se van a eliminar ya que un software, puede depender de varios paquetes, y hay que revisarlos.

Al eliminar, se puede quedar elementos de configuración en el sistema de ese software.

Si deseamos eliminar todo lo relacionado con ese software habrá que ejecutar el comando:

    # apt-get purge nombre_software



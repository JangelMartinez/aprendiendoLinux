# Tuberias #

Además de enviar texto a un dispositivo, disponemos de otra potente opción: enviarlo a otro comando. Esto se realiza con el carácter '|' llamado tuberia.

La tuberia establece un canal por el que pasará el texto de un comando a otro.

    echo "HOLA MUNDO" | wc 
    
    grep -w ana /etc/passwd | cut -d":" -f1 | sort




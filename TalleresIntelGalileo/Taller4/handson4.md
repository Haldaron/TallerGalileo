##Hands On 4: Procedimiento
###Intalando Arduino IDE

+ Acceder a la dirección web http://www.intel.com/support/galileo/sb/CS-035101.htm
+ Descargar la Intel Arduino IDE 1.5.3 disponible en la sección `Previous releases
+ Descomprima el archivo descargado en una carpeta dentro perteneciente a su usuario. Para esto pueden usar el comando:
```tar -xvf arduino-linux64-1.0.4.tgz```
+ Ingrese a la carpeta que acaba de descomprimir y corra el ejecutable de conmbre "arduino". Esto abrira la IDE de arduino para la Intel Galileo: ```cd arduino-1.5.3-Intel.1.0.4; ./arduino```
+ Una vez abierta la interfaz, identifique un botón en la parte superior izquierda de la interfaz cuyo ícono es una flecha hacia la derecha
+ Haga click en este botón. Esto instalará el software de la Galileo en su máquina
+ Cree la ruta de directorios /opt/clanton-tiny/1.4.2/sysroots
+ ```sudo mkdir -p /opt/clanton-tiny/1.4.2/sysroots```
+ Copie la carpeta [RUTA_ARDUINO]/ hardware/tools/sysroots/i586-poky-linux-uclibc a aquella carpeta que acaba de crear
+ ```sudo cp  [RUTA_ARDUINO]/ hardware/tools/sysroots/i586-poky-linux-uclibc /opt/clanton-tiny/1.4.2/sysroots/```
+ Agregue al la variable de ambiente PATH, la ubicación del compilador que usa Arduino
+ ```export PATH=[RUTA_ARDUINO]/hardware/tools/sysroots/x86_64-pokysdk-linux/usr/bin/i586-poky-linux-uclibc/:$PATH ```

Ahora puede utilizar el programa  i586-poky-linux-uclibc-gcc para compilar los ejecutables que desee correr en la tarjeta

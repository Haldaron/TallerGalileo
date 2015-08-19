##Hands On 1: Procedimiento
###Formateo de la tarjeta SD

+ Conecte la tarjeta SD a su computador.(No olvide desbloquearla conanterioridad).
+ Desmonte el FileSystem de la tarjeta SD de la jerarquía de archivos de Linux.
+ ```dmesg``` (Obtener nombre de dispositivo recien conectado Ej: mmcblk).
+ sudo fdisk /dev/[Nombre del Dispositivo] .
+ Ingrese **d** al programa para borrar las particiones existentes.
+ Ingrese **n** para crear una nueva particion. (Opciones por Default)
+ Ingrese **t** para modicar el tipo de la particion y a continuacion **c** para seleccionar el tipo W95 FAT32 (LBA).
+ Por último, ingrese **w** para escribir los cambios sobre el dispositiv

###Inicialización de FyleSystem sobre la SD

+ ```sudo mkfs.vfat -F32 /dev/[Nombre Del Dispositivo ][Número de la Partición].``` ```Ej: sudo mkfs.vfat -F32 mmcblk01```
+ Remueva la tarjeta SD del puerto del computador y acto seguido
+ vuelva a insertarla en el mismo lugar.
+ Verifique que Linux efectivamente monta el sistema de archivos de la tarjeta SD al sistema operativo.


###Mover la distribución a la SD

+ Descomprima el archivo .bz2 obtenido desde la página de Galileo para descargas.
```bzip2 -d SDCard.1.0.4.tar.bz2 ; tar -xvf SDCard.1.0.4.tar```
+ Localice la carpeta donde se descomprimieron los archivos.
+ Corte o copie los contenidos de dicha carpeta y muévalos al lugar en donde fue montado el sistema de archivos de la tarjeta SD.
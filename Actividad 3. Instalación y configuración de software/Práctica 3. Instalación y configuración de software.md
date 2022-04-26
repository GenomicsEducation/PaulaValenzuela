#### 3) INSTALACIÓN Y CONFIGURACIÓN SOFTWARE 
###### Realizar el análisis integral de control de calidad de secuencias NGS con fastqc.

##### 3.1) Control de calidad
###### Se procedió a configurar bioconda e instalación de software

## ![Instalación software](https://user-images.githubusercontent.com/80971762/121821313-4584e580-cc66-11eb-8e30-2c7a000b7835.png)
## ![](https://user-images.githubusercontent.com/80971762/121821380-811faf80-cc66-11eb-9f56-a9991ef11d17.png)
## ![3 3](https://user-images.githubusercontent.com/80971762/121821388-91378f00-cc66-11eb-9af6-1be92acaa8f7.png)
## ![3 4](https://user-images.githubusercontent.com/80971762/121821527-9a752b80-cc67-11eb-8a1f-59429a187e75.png)
## ![3 5](https://user-images.githubusercontent.com/80971762/121821549-b7a9fa00-cc67-11eb-9490-5dc1a6d8502f.png)

##### 3.2) ETAPAS ANÁLISIS DE CONTROL DE CALIDAD, FILTRADO Y PODA.
###### Descargar secuencias NGS usando SRA toolkit: Para descarga de biomuestra desde SRAS, se utilizó el siguiente script 
        #!/bin/bash 
        #SBATCH -J prefetch_usuario
        /home2/usuario/sratoolkit.2.11.0-centos_linux64/bin/prefetch --max-size 100G SRR2006763 -O /home2/usuario/SRA_samples/
        /home2/usuario/sratoolkit.2.11.0-centos_linux64/bin/vdb-validate /home2/usuario/SRA_samples/SRR2006763/SRR2006763.sra
 
## ![3 6](https://user-images.githubusercontent.com/80971762/121821568-d0b2ab00-cc67-11eb-95d6-9c7956f67d2c.png)

###### Este script contiene las instrucciones necesarias para la descarga de la secuencia con el comando *prefetch* que es parte del kit de herramientas de SRA y su función es descargar archivos de secuencia en formato SRA comprimido. Además, incluye un segundo comando llamado *vdb-validate* que realiza varios chequeos luego de la descarga para asegurar que esta se ha desarrollado correctamente

## ![3 7](https://user-images.githubusercontent.com/80971762/121821574-dc9e6d00-cc67-11eb-9fc7-c6126680ded3.png)

###### Se accedió a la carpeta **SRR2006763** y creó el siguiente script (nano fdump.sh ó en mi caso nano SRR2006763) que permitió obtener los archivos fastq de la muestra SRR2006763
      #!/bin/bash
      #SBATCH - J fdump_usuario
      /home2/usuario/sratoolkit.2.11.0-centos_linux64/bin/fasterq-dump /home2/usuario/SRA_samples/SRR2006763/*.sra -O      /home2/usuario/SRA_samples/SRR2006763/
  
##   ![paula valenzuela@test-pomeo_~_SRA_samples_SRR2006763 10-06-2021 13_42_10](https://user-images.githubusercontent.com/80971762/121821908-03f63980-cc6a-11eb-8ac1-4127e6c9e34d.png)

##### 3.3) Comprobación de integridad de archivos
##![3 8](https://user-images.githubusercontent.com/80971762/121821923-21c39e80-cc6a-11eb-9358-472dbed35fe3.png)

##### 3.4) Realizar análisis de control de calidad
###### Se corrió el siguiente script, donde la salida de la ejecuación del sript dío dos archivos 
        #!/bin/bash
        #SBATCH - J fastqc_usuario
        fastqc /home2/usuario/SRA_samples/SRR2006763/*.fastq
    
## ![3 9](https://user-images.githubusercontent.com/80971762/121822013-ab736c00-cc6a-11eb-8e84-f39841fb8f07.png)

###### Para descargar los archivos, POMEO tiene instalado Rstudio server por lo que fue posible acceder a los archivos directamente ingresando al servidor a traves del puerto 8787.

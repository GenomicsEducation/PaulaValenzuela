# ***Descripción genómica de la especie salmón del Atlántico (Salmo salar)***
##### - CURSO DBT 972 (GENÉTICA Y GENÓMICA EN PRODUCCIÓN ANIMAL)
#### Autor: 
- Paula Valenzuela Aviés
- Ingeniero en Biotecnología

## **Objetivos**
### 1) Seleccionar una especie de interes comercial de la producción animal y buscar información de su genoma en Assembly, Refseq y Bioproyectos en SRA.
### 2) Instalar y configurar el software para acceso remoto y transferencia de archivos.
### 3) Realizar un análisis integral de control de calidad de secuencias NGS con fastqc.Adicionalmente filtrar y podar las secuencias con el software trimmomatic.

### * Descripción del trabajo realizado*
#### Se Selecciono la especie de importancia económica en producción animal Salmón del Atlántico. En la primera etapa se buscó información de su genoma en Assembly y Refseq para resumir la información genómica de interés en REDME del repositorio Git: GenomicsEducation/PaulaValenzuela. Posteriomente se busco información del Bioproyectos en SRA que presenta el número de acceso **SRX1103127816S** que evalua el impacto de la alimetación en el microbioma intestinal de salmón del atlántico juvenil a través de la secuenciaón del 16S rRNA del instestino.<https://www.ncbi.nlm.nih.gov/sra/SRX11031278[accn]>. Por ultimo se descargo el metadata de las muestras en formato.txt archivada en ** Metadata 2 update**. En la segunda etapa se procedio a instalar y configurar el software para acceso remoto y transferencia de archivos.Está actividad fue realizada desde R-markdown a github con el objetivo de aprender a clonar el repositorio. La tercera etapa consitió en realizar un análisis de control de calidad de las secuencias NSG con fastqc, para esto el análisis se realizó desde la base de datos SRA del NCBI y corresponden lecturas crudas del salmón del Atlántico *Salmo salar* en formato fastq, obtenidas por secuenciación de extremos emparejados con un secuenciador Illumina HiSeq2000; Las descargas de las secuencias NGS se procesedió utilizando SRA toolkit, luego se comprobó la integridad de descarga de archivos usando md5sum o similar, posteriormente se realizó el análisis de control de calidad. Para finalizar esta etapa se realizó el filtrado y poda de secuencias utilizando el software trimmomatic y se transfirieron los archivos de control de calidad mediante protocolo FTP desde Servidor a Cliente.

## ![Salmón del Atlántico](https://th.bing.com/th/id/OIP.yVdBR79JssLwOb82BdbHPgHaEK?pid=ImgDet&rs=1)

### _Actividades_

#### 1) Genoma del Samón del Atlántico en Assembly, Refseq y Bioproyectos en SRA
- 1.1) Assembly

  **CSASG_v2**
 
  - Nombre del Organismo: Salmo salar (Atlantic salmon)
  - Nombre inespecifico: Salmón Atlantico
  - Raza: aislado doble haploide 
  - Sexo: Hembra 
  - Biomuestra: SAMN02749551 <https://www.ncbi.nlm.nih.gov/biosample/SAMN02749551/>
  - Projecto: PRJNA72713 <https://www.ncbi.nlm.nih.gov/bioproject/PRJNA72713/>
  - Remitente : International Cooperation to Sequence the Atlantic Salmon Genome
  - Fecha: 2015/06/10
  - Nivel de Ensamblel: Cromosoma
  - Representacion del genoma: Completo
  - Categoria RefSeq : genoma representativo
  - Acceso GenBank assembly : GCA_000233375.4 (latest)
  - Acceso RefSeq assembly : GCF_000233375.1 (latest)
  - identico RefSeq assembly y GenBank assembly: no 
  - WGS Project: AGKD04 <https://www.ncbi.nlm.nih.gov/nuccore/AGKD00000000.4/>
  - Método Ensamble: MaSuRCA v. 2.0.3
  - Tecnología de secuanción: Illumina HiSeq; PacBio; Sanger; Illumina GAIIx

 ##### Este es un nuevo ensamble de todo el genoma del Salmón del Atlántico. El ensamble fue realizado con MaSuRCA v. 2.0.3 y post procesado para lograr cerrar los espacios de los andamios se utilizaron secuencias de otros ensamblajes. La muestra de ADN fue extraida desde el músculo de un donor doble haploide. 
 #### Estadisticas Globales
  
  |longitud de la secuencia total| 2,966,890,203| 
  |------------|--------------|
  |Longitud total sin espacios   | 2,618,890,303|
  |Gaps entre andamios| 9,418|  
  |Número total de cromosomas y plásmidios| 30| 
 
- 1.2) RefSeq
- 
  **CSASG_v2** 
  
#### Aceso = Público
#### Fuente =
DNA(7,164)
RNA(3,779)
#### Type =genome(1,283)

#### Dispoción de la biblioteca =
pares(6,805)
simple(4,340)

#### Plataformas=
-ABI SOLiD(31)   
-BGISEQ(13)   
-Capillary(321)   
-Illumina(10,514)   
-Ion Torrent(132)   
-LS454(11)   
-Oxford Nanopore(14)   
-PacBio SMRT(109)  

#### Estrategía=
-EpiGenomics(314) 
-Exome(425)

#### Genome(1,605)
#### other(8,801)
#### Tipo de fila=
-bam(394)

##### -fastq(9,009)
##### -sff(4)
##### -* Datos alineados* =(152)
##### -Link de accceso muestra *ERX4787613*
##### -Número de referencia de la Muestra= ERX4787613: HiSeq X Ten paired end sequencing; Raw reads: Library_IoA-00,Sample_IoA-00_9(A9)
##### -subido por =Institute of Aquaculture, University of Stirling, Stirling, UK (Institute of Aquaculture, University of Stirling, )
##### -Muestra: Laboratory strain IoA-00, SAMEA7690915 • ERS5447441
##### - Organism: Lepeophtheirus salmonis

|Run	| N°of Spots|	N° of Bases|	Size|	Published|
|----|-----|-----|-----|-----|
|ERR4968416|	27,846,466	|8.4G	|2.5Gb	|2021-05-12|

- 1.3) SRA

#### **SRX11031278** : 16S rRNA microbioma intestinal de salmón del atlántico juvenil <https://www.ncbi.nlm.nih.gov/sra/SRX11031278[accn]>
1 ILLUMINA (Illumina MiSeq) run: 71,300 spots, 38.9M bases, 22.5Mb descarga

##### Diseño: el ADN de cada muestra de intestino se sometió a PCR de una región que cubre la región V3-V4 del gen rRNA 16S utilizando el par de cebadores bacterianos universales SD-Bact-0341-bS-17 (5-CCTACGGGNGGCWGCAG-3) / SD- Bact-0785-aA-21 (5-GACTACHVGGGTATCTAATCC-3) (Klindworth et al., 2013). Las reacciones de PCR se configuraron utilizando 10 ng de ADN molde, 5 l de tampón 5X Phusion HF (New England BioLabs), dNTP 200 M, cebadores directos 0,5 M y inversos 0,5 M que contienen adaptadores de proyección Illumina, 0,2 l de ADN polimerasa de alta fidelidad Phusion y agua libre de nucleasas hasta un volumen total de reacción de 25 l. Las condiciones del termociclador se establecieron con un paso de desnaturalización inicial a 98ºC durante 30 s seguido de 30 ciclos de: desnaturalización a 98ºC durante 10 s, hibridación a 52ºC durante 30 sy extensión a 72ºC durante 30 s. La extensión final se fijó a 72ºC durante 5 min. Las bibliotecas se multiplexaron utilizando códigos de barras Nextera XT v2 (Illumina), se normalizaron en placas de normalización Sequel-Prep (ThermoFisher Scientific) y se secuenciaron en un secuenciador de escritorio MiSeq (Illumina) utilizando química v3 y 2 x 300 ciclos.

|Estudio: Metamorphosis_salmongut_insectmeal|--------|
|------------|----------------------|
|PRJNA733893|<https://www.ncbi.nlm.nih.gov/bioproject/PRJNA733893>
|SRP321989|<https://trace.ncbi.nlm.nih.gov/Traces/sra/?study=SRP321989|

##### Abstract: Diferentes tratamientos de larvas de mosca para alimentar a alevines de salmón del Atlántico (Salmo salar) para evaluar el impacto en el microbioma intestinal.

#### Biblioteca:
|Nombre| BSFC-tank3replicate3|
|------|------------|
|Instrumento| Illumina MiSeq|
|Estrategia| AMPLICON|
|Fuente| METAGENOMIC|
|Selección| PCR|

|Run| # of Spots|	# of Bases|	Size	Published|
|---|-----------|-----------|----------------|
|SRR14693097|	71,300	|38.9M|	22.5Mb|	2021-05-31|


#### 2) Posteriormente se Procedio a Instalar y configurar el software para acceso remoto y transferencia de archivos.Está actividad fue realizada desde R-markdown a github con el objetivo de aprender a clonar el repositorio. 
##### El trabajó realizado se encuentra en disponible en la carpeta Instlacion_y_configuracion_del_software_para_acceso_remoto_y_trasnferencia

##### Para acceder al servidor POMEO de la Escuela de Ciencias del Mar usando los siguientes nombres de usuario (*paula.valenzuela*) y password (*05student2021*)

##### Cabe mencionar que los sript utilizados fueron los siguientes: 
##### 2.1) - nano script1.sh
           # !/bin/bash
           # Mi primer script
           echo Curso de Bioinformática
##### 2.2) - nano script1.sh
           # !/bin/bash
           # Descarga y descomprime SRA Toolkit wget http://ftp-trace.ncbi.nlm.nih.gov/sra/sdk/current/sratoolkit.current-centos_linux64.tar.gz tar -xzf sratoolkit.current-  centos_linux64.tar.gz


#### 3) Al realizar el análisis integral de control de calidad de secuencias NGS con fastqc.

##### 3.1) Se procedió a configurar bioconda e instalación de software
## ![Instalación software](https://user-images.githubusercontent.com/80971762/121821313-4584e580-cc66-11eb-8e30-2c7a000b7835.png)
## ![](https://user-images.githubusercontent.com/80971762/121821380-811faf80-cc66-11eb-9f56-a9991ef11d17.png)
## ![3 3](https://user-images.githubusercontent.com/80971762/121821388-91378f00-cc66-11eb-9af6-1be92acaa8f7.png)
## ![3 4](https://user-images.githubusercontent.com/80971762/121821527-9a752b80-cc67-11eb-8a1f-59429a187e75.png)
## ![3 5](https://user-images.githubusercontent.com/80971762/121821549-b7a9fa00-cc67-11eb-9490-5dc1a6d8502f.png)

##### 3.2)  Descarga de biomuestra desde SRA
###### Se utilizó el siguiente script 

## #!/bin/bash 
   #SBATCH -J prefetch_usuario
   /home2/usuario/sratoolkit.2.11.0-centos_linux64/bin/prefetch --max-size 100G SRR2006763 -O /home2/usuario/SRA_samples/
   /home2/usuario/sratoolkit.2.11.0-centos_linux64/bin/vdb-validate /home2/usuario/SRA_samples/SRR2006763/SRR2006763.sra
 
## ![3 6](https://user-images.githubusercontent.com/80971762/121821568-d0b2ab00-cc67-11eb-95d6-9c7956f67d2c.png)

###### Este script contiene las instrucciones necesarias para la descarga de la secuencia con el comando *prefetch* que es parte del kit de herramientas de SRA y su función es descargar archivos de secuencia en formato SRA comprimido. Además, incluye un segundo comando llamado *vdb-validate* que realiza varios chequeos luego de la descarga para asegurar que esta se ha desarrollado correctamente

## ![3 7](https://user-images.githubusercontent.com/80971762/121821574-dc9e6d00-cc67-11eb-9fc7-c6126680ded3.png)

###### Se accedió a la carpeta **SRR2006763** y creó el siguiente script (nano fdump.sh ó en mi caso nano SRR2006763) que permitió obtener los archivos fastq de la muestra SRR2006763
## #!/bin/bash
  #SBATCH - J fdump_usuario
  /home2/usuario/sratoolkit.2.11.0-centos_linux64/bin/fasterq-dump /home2/usuario/SRA_samples/SRR2006763/*.sra -O   /home2/usuario/SRA_samples/SRR2006763/
  
##   ![paula valenzuela@test-pomeo_~_SRA_samples_SRR2006763 10-06-2021 13_42_10](https://user-images.githubusercontent.com/80971762/121821908-03f63980-cc6a-11eb-8ac1-4127e6c9e34d.png)

##### 3.3)Comprobación de integridad de archivos
##![3 8](https://user-images.githubusercontent.com/80971762/121821923-21c39e80-cc6a-11eb-9358-472dbed35fe3.png)

##### 3.4) Análisis de control de calidad
###### Se corrió el siguiente script, donde la salida de la ejecuación del sript dío dos archivos 
###   #!/bin/bash
     #SBATCH - J fastqc_usuario
     fastqc /home2/usuario/SRA_samples/SRR2006763/*.fastq
    
## ![3 9](https://user-images.githubusercontent.com/80971762/121822013-ab736c00-cc6a-11eb-8e84-f39841fb8f07.png)

###### Para descargar los archivos POMEO tiene instalado Rstudio server por lo que fue posible acceder a los archivos directamente ingresando al servidor a traves del puerto 8787.

## ![Introducción al análisis de secuencias NGS y 3 páginas más - Personal_ Microsoft​ Edge 10-06-2021 13_42_24](https://user-images.githubusercontent.com/80971762/121822116-4f5d1780-cc6b-11eb-87c1-f037c7bd6baf.png)
## ![RStudio y 3 páginas más - Personal_ Microsoft​ Edge 13-06-2021 17_17_02](https://user-images.githubusercontent.com/80971762/121822119-53893500-cc6b-11eb-9f73-9f7fd0f01ae8.png)

##### 3.5) Filtrar y podar 

###### Se ejecutó el siguinte script desde la carpeta donde constan los archivos fastq (SRR2006763/) 
###   #!/bin/bash
      #SBATCH - J trimm_usuario
      trimmomatic PE SRR2006763_1.fastq SRR2006763_2.fastq -baseout SRR20067634_filtered.fastq.gz SLIDINGWINDOW:5:25 MINLEN:60

##### De la ejecucion anterior se ejecutaron 4 archivos comprimidos que posteriormente se descomprimieron
## ![3 10](https://user-images.githubusercontent.com/80971762/121822280-46b91100-cc6c-11eb-99fa-048197451a91.png)
## ![3 11](https://user-images.githubusercontent.com/80971762/121822294-57698700-cc6c-11eb-912e-5f38a4081378.png)
## ![3 12](https://user-images.githubusercontent.com/80971762/121822299-605a5880-cc6c-11eb-995b-2b195f0fbc38.png)

##### Cabe desctacar que los archivos descargados y descomprimidos en formato HTLM se enuentran en la carpeta ---



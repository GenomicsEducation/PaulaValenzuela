# ***Descripción genómica de la especie salmón del Atlántico (Salmo salar)***
##### - CURSO DBT 972 (GENÉTICA Y GENÓMICA EN PRODUCCIÓN ANIMAL)
#### Autor: 
- Paula Valenzuela Aviés
- Ingeniero en Biotecnología

## **Objetivos**
### 1) Seleccionar una especie de interes comercial de la producción animal y buscar información de su genoma en Assembly, Refseq y Bioproyectos en SRA.
### 2) Instalar y configurar el software para acceso remoto y transferencia de archivos.
### 3) Instalación y configuración de software.
### 4) Realizar el alineamiento de una muestra en formato .fastq a un genoma de referencia.
### 5) Realizar el llamado de variantes de una secuencia de Salmo salar obtenida por secuenciación de extremos emparejados

### * Descripción del trabajo realizado*
#### Se Selecciono la especie de importancia económica en producción animal Salmón del Atlántico. En la primera etapa se buscó información de su genoma en Assembly y Refseq para resumir la información genómica de interés en REDME del repositorio Git: GenomicsEducation/PaulaValenzuela. Posteriomente se busco información del Bioproyectos en SRA que presenta el número de acceso **SRX1103127816S** que evalua el impacto de la alimetación en el microbioma intestinal de salmón del atlántico juvenil a través de la secuenciaón del 16S rRNA del instestino.<https://www.ncbi.nlm.nih.gov/sra/SRX11031278[accn]>. Por ultimo se descargo el metadata de las muestras en formato.txt archivada en ** Metadata 2 update**. En la segunda etapa se procedio a instalar y configurar el software para acceso remoto y transferencia de archivos.Está actividad fue realizada desde R-markdown a github con el objetivo de aprender a clonar el repositorio. La tercera etapa consitió en realizar un análisis de control de calidad de las secuencias NSG con fastqc, para esto el análisis se realizó desde la base de datos SRA del NCBI y corresponden lecturas crudas del salmón del Atlántico *Salmo salar* en formato fastq, obtenidas por secuenciación de extremos emparejados con un secuenciador Illumina HiSeq2000; Las descargas de las secuencias NGS se procesedió utilizando SRA toolkit, luego se comprobó la integridad de descarga de archivos usando md5sum o similar, posteriormente se realizó el análisis de control de calidad. Para finalizar esta etapa se realizó el filtrado y poda de secuencias utilizando el software trimmomatic y se transfirieron los archivos de control de calidad mediante protocolo FTP desde Servidor a Cliente. La cuarta etapa consistio en realizar un alinamiento de la muestra en formato .fastaq a un genoma de referencia que para este caso será con el genoma de la mitocondria del salmón del atlántico (dado su pequeño tamaño) para terminar con el análisis del alinamiento. En la quinta etapa se continuará utilizando las  secuencias filtradas o podadas pero ahora se encontrarán las variantes de las secuencias descargadas, esto comparandolas con el genoma de referencia DNA mitocondrial del salmón del  Atlantico utilizando el software  HaplotypeCaller de GATK, posteriormente el analisis de las variantes de realizará en Linux y vcftoolts, para terminar visualizandolas en IGV. 

## ![Salmón del Atlántico](https://th.bing.com/th/id/OIP.yVdBR79JssLwOb82BdbHPgHaEK?pid=ImgDet&rs=1)

### _Actividades_

#### 1) GENOMA DEL SALMÓN DEL ATLÁNTICO EN Assembly, Refseq y Bioproyectos EN SRA
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


#### 2) INSTALAR Y CONFIGURAR EL SOFTWARE PARA ACCESO REMOTO Y TRANSFERENCIA DE ARCHIVOS
##### Está actividad fue realizada desde R-markdown a github con el objetivo de aprender a clonar el repositorio. 
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


#### 3) INSTALACIÓN Y CONFIGURACIÓN SOFTWARE 
###### Realizar el análisis integral de control de calidad de secuencias NGS con fastqc.

##### 3.1) Control de calidad
###### Se procedió a configurar bioconda e instalación de software
## ![Instalación software](https://user-images.githubusercontent.com/80971762/121821313-4584e580-cc66-11eb-8e30-2c7a000b7835.png)
## ![](https://user-images.githubusercontent.com/80971762/121821380-811faf80-cc66-11eb-9f56-a9991ef11d17.png)
## ![3 3](https://user-images.githubusercontent.com/80971762/121821388-91378f00-cc66-11eb-9af6-1be92acaa8f7.png)
## ![3 4](https://user-images.githubusercontent.com/80971762/121821527-9a752b80-cc67-11eb-8a1f-59429a187e75.png)
## ![3 5](https://user-images.githubusercontent.com/80971762/121821549-b7a9fa00-cc67-11eb-9490-5dc1a6d8502f.png)

##### 4.1) Alineamiento
###### El sotfware BWA es un algoritmo de alineación para alinear lecturas de secuencia o secuencias de consulta largas en este caso con el genoma de referencia del salmo salar (ICSAGS_V2), especificamente el mirocondrial (NC_001960.1). 
###### Por otra parte el sotfware Samtools, permite manipular alineaciones en los formatos SAM (Sequence Alignment Map), BAM y CRAM. Convierte entre los formatos, clasifica, fusiona e indexa, y puede recuperar lecturas en cualquier región rápidamente
## ![paula valenzuela@test-pomeo_~ 17-06-2021 12_16_51](https://user-images.githubusercontent.com/80971762/123139725-8332fc80-d424-11eb-98ef-244adadc6dd0.png)
## ![paula valenzuela@test-pomeo_~ 17-06-2021 12_16_59](https://user-images.githubusercontent.com/80971762/123139788-93e37280-d424-11eb-9ef3-c6d56f2b5ce7.png)
## ![paula valenzuela@test-pomeo_~ 17-06-2021 12_18_21](https://user-images.githubusercontent.com/80971762/123139837-9fcf3480-d424-11eb-9943-b91e6cbbe616.png)

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

## ![Introducción al análisis de secuencias NGS y 3 páginas más - Personal_ Microsoft​ Edge 10-06-2021 13_42_24](https://user-images.githubusercontent.com/80971762/121822116-4f5d1780-cc6b-11eb-87c1-f037c7bd6baf.png)
## ![RStudio y 3 páginas más - Personal_ Microsoft​ Edge 13-06-2021 17_17_02](https://user-images.githubusercontent.com/80971762/121822119-53893500-cc6b-11eb-9f73-9f7fd0f01ae8.png)

##### 3.5)  Realizar filtrado y poda de secuencias.

###### Se ejecutó el siguinte script desde la carpeta donde constan los archivos fastq (SRR2006763/) 
         #!/bin/bash
         #SBATCH - J trimm_usuario
          trimmomatic PE SRR2006763_1.fastq SRR2006763_2.fastq -baseout SRR20067634_filtered.fastq.gz SLIDINGWINDOW:5:25 MINLEN:60

##### De la ejecucion anterior se ejecutaron 4 archivos comprimidos que posteriormente se descomprimieron
## ![3 10](https://user-images.githubusercontent.com/80971762/121822280-46b91100-cc6c-11eb-99fa-048197451a91.png)
## ![3 11](https://user-images.githubusercontent.com/80971762/121822294-57698700-cc6c-11eb-912e-5f38a4081378.png)
## ![3 12](https://user-images.githubusercontent.com/80971762/121822299-605a5880-cc6c-11eb-995b-2b195f0fbc38.png)

##### Transferir archivos de control de calidad mediante protocolo FTP desde Servidor a Cliente: Cabe desctacar que los archivos descargados y descomprimidos en formato HTLM se encuentran en la carpeta ---

#### 4) ETAPAS DE ALINEAMIENTO

##### 4.2) Obtener secuencias Fastq
## ![paula valenzuela@test-pomeo_~ 17-06-2021 12_38_42](https://user-images.githubusercontent.com/80971762/123141865-d73ee080-d426-11eb-9232-b2f928122610.png)
## ![paula valenzuela@test-pomeo_~_alineamiento 17-06-2021 12_50_03](https://user-images.githubusercontent.com/80971762/123141949-ede53780-d426-11eb-9985-625c7eff4ce9.png)
## ![paula valenzuela@test-pomeo_~_alineamiento 17-06-2021 12_50_09](https://user-images.githubusercontent.com/80971762/123142028-07867f00-d427-11eb-972c-5fe2024bdb91.png)

##### 4.3) Subir genoma a POMEO con software de acceso remoto
## ![paula valenzuela@test-pomeo_~_alineamiento 17-06-2021 12_52_44](https://user-images.githubusercontent.com/80971762/123142475-782d9b80-d427-11eb-91fc-e77640bd6aa9.png))

##### 4.4) Indexación genoma mitocondrial
## ![paula valenzuela@test-pomeo_~_alineamiento 17-06-2021 12_52_44](https://user-images.githubusercontent.com/80971762/123142935-fdb14b80-d427-11eb-8afa-65e1fbe561d9.png)
## ![PaulaValenzuela - paula valenzuela@200 54 220 141 - WinSCP 17-06-2021 12_48_50](https://user-images.githubusercontent.com/80971762/123142803-d490bb00-d427-11eb-84fd-d5e164855359.png)

##### Para ejecutar todas las etapas se debe ejecutar el script con nano denominado aln_mt.sh
     #!/bin/bash -l
     # para alinear tus dos secuencias fastq al genoma mitocondrial
     bwa mem mt.fasta SRR2006763_1.fastq SRR2006763_2.fastq > SRR2006763.sam 
     # Transformar tu archivo sam a bam
     samtools view -Sb -q 30 SRR2006763.sam > SRR2006763.bam 
      # ordenar tu archivo binario bam
      samtools sort SRR2006763.bam -o SRR2006763.sort.bam 
      # indexar tu archivo bam
      samtools index SRR2006763.sort.bam 

##### 4.5)Alineamiento de secuencias contra genoma mitocondrial
## ![paula valenzuela@test-pomeo_~_alineamiento 17-06-2021 12_57_44](https://user-images.githubusercontent.com/80971762/123143143-3b15d900-d428-11eb-8c07-5e661e105be6.png)
## ![paula valenzuela@test-pomeo_~_alineamiento 17-06-2021 12_58_05](https://user-images.githubusercontent.com/80971762/123143181-4832c800-d428-11eb-890f-a785ede0e49e.png)

##### 4.6) Conversión SAM a BAM y análisis estadistico estandar
## ![paula valenzuela@test-pomeo_~_alineamiento 17-06-2021 12_59_22](https://user-images.githubusercontent.com/80971762/123143526-b24b6d00-d428-11eb-8b13-1c25c8e150fa.png)
## ![paula valenzuela@test-pomeo_~_alineamiento 17-06-2021 12_59_50](https://user-images.githubusercontent.com/80971762/123144050-40275800-d429-11eb-862c-e3b03bac0396.png)

##### 4.7) Orden de lecturas alineadas por posición, Indexación con Samtools , Exploración de archivos de salida en cada etapa
## ![paula valenzuela@test-pomeo_~_alineamiento 17-06-2021 13_22_24](https://user-images.githubusercontent.com/80971762/123144080-49b0c000-d429-11eb-86a3-d36fa24936e7.png)
## ![paula valenzuela@test-pomeo_~_alineamiento 17-06-2021 13_26_59](https://user-images.githubusercontent.com/80971762/123144135-5af9cc80-d429-11eb-97ca-eba1eb85f865.png)

##### 4.8) Explorar alineamiento con samtools
## ![paula valenzuela@test-pomeo_~_alineamiento 23-06-2021 11_54_33](https://user-images.githubusercontent.com/80971762/123144447-add38400-d429-11eb-8540-3e11f7e14b9a.png)
## ![paula valenzuela@test-pomeo_~_alineamiento 23-06-2021 11_54_47](https://user-images.githubusercontent.com/80971762/123144526-bdeb6380-d429-11eb-8f1a-c85bea85a20a.png)
##  ![paula valenzuela@test-pomeo_~_alineamiento 23-06-2021 11_55_07](https://user-images.githubusercontent.com/80971762/123144564-c8a5f880-d429-11eb-9230-02a9714dd4af.png)
## ![paula valenzuela@test-pomeo_~_alineamiento 23-06-2021 11_55_32](https://user-images.githubusercontent.com/80971762/123144601-d22f6080-d429-11eb-965a-6f42b60008d0.png)
## ![paula valenzuela@test-pomeo_~_alineamiento 23-06-2021 12_08_40](https://user-images.githubusercontent.com/80971762/123144702-f723d380-d429-11eb-862d-e07e0d670d5c.png)
## ![paula valenzuela@test-pomeo_~_alineamiento 23-06-2021 12_12_34](https://user-images.githubusercontent.com/80971762/123144752-0440c280-d42a-11eb-9cab-6a2e7d408619.png)

##### 4.9) Visualizacion de la salida del alinamiento
##![IGV 23-06-2021 12_37_14](https://user-images.githubusercontent.com/80971762/123145011-54b82000-d42a-11eb-8d4e-4973372d954e.png)

#### 5) ETAPAS DE LLAMADO DE VARIANTES 

##### 5.1)Configurar bioconda e instalar programas para análisis

## ![paula valenzuela@test-pomeo_~ 24-06-2021 12_17_10](https://user-images.githubusercontent.com/80971762/123453278-552cf400-d5ad-11eb-8bcd-1910c08de683.png)
## ![paula valenzuela@test-pomeo_~ 24-06-2021 12_19_00](https://user-images.githubusercontent.com/80971762/123453313-62e27980-d5ad-11eb-9d55-0909809c643b.png)
## ![paula valenzuela@test-pomeo_~ 24-06-2021 12_19_20](https://user-images.githubusercontent.com/80971762/123453370-7392ef80-d5ad-11eb-9226-41f160153736.png)
## ![paula valenzuela@test-pomeo_~ 24-06-2021 12_19_36](https://user-images.githubusercontent.com/80971762/123453391-7c83c100-d5ad-11eb-903d-733a48d7da98.png)

##### 5.2) Crear directorio de trabajo “variant_call” y preparar archivos para el llamado de variantes.
## ![paula valenzuela@test-pomeo_~_variant_call 24-06-2021 11_52_39](https://user-images.githubusercontent.com/80971762/123453547-b05ee680-d5ad-11eb-9bb3-3b03575b0ac7.png)
## ![paula valenzuela@test-pomeo_~_variant_call 24-06-2021 11_54_04](https://user-images.githubusercontent.com/80971762/123453672-c40a4d00-d5ad-11eb-9d7a-fd8cc07f601f.png)
## ![paula valenzuela@test-pomeo_~_variant_call 24-06-2021 12_01_03](https://user-images.githubusercontent.com/80971762/123453702-ccfb1e80-d5ad-11eb-8a5f-b2f59c151662.png)
## ![paula valenzuela@test-pomeo_~_variant_call 24-06-2021 12_01_58](https://user-images.githubusercontent.com/80971762/123453769-d7b5b380-d5ad-11eb-9102-f2755d2899e0.png)
## ![paula valenzuela@test-pomeo_~_variant_call 24-06-2021 12_03_19](https://user-images.githubusercontent.com/80971762/123453830-e1d7b200-d5ad-11eb-882c-648f8812450d.png)
## ![paula valenzuela@test-pomeo_~_variant_call 24-06-2021 12_03_40](https://user-images.githubusercontent.com/80971762/123453870-ed2add80-d5ad-11eb-8f2b-302ceafe9ab2.png)
## ![paula valenzuela@test-pomeo_~_variant_call 24-06-2021 12_03_54](https://user-images.githubusercontent.com/80971762/123453899-f5831880-d5ad-11eb-952d-da0f1f767735.png)
## ![paula valenzuela@test-pomeo_~_variant_call 24-06-2021 12_05_07](https://user-images.githubusercontent.com/80971762/123453958-06338e80-d5ae-11eb-9f4c-dbf4d449e569.png)
## ![paula valenzuela@test-pomeo_~_variant_call 24-06-2021 12_05_20](https://user-images.githubusercontent.com/80971762/123454003-13e91400-d5ae-11eb-8390-e16c02ac1461.png)
## ![paula valenzuela@test-pomeo_~_variant_call 24-06-2021 12_05_41](https://user-images.githubusercontent.com/80971762/123454039-1c414f00-d5ae-11eb-9b08-723e725e3441.png)
## ![paula valenzuela@test-pomeo_~_variant_call 24-06-2021 12_06_06](https://user-images.githubusercontent.com/80971762/123454070-26fbe400-d5ae-11eb-803d-e4e95b27b57b.png)

##### 5.3) Llamado de variantes
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_15_21](https://user-images.githubusercontent.com/80971762/123455524-ca99c400-d5af-11eb-8d6f-74a5e77b4ff0.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_21_10](https://user-images.githubusercontent.com/80971762/123455670-fd43bc80-d5af-11eb-805b-3bb07d3b4239.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_21_40](https://user-images.githubusercontent.com/80971762/123455753-1482aa00-d5b0-11eb-88f0-fe9dbe07e82c.png)



###### comando HaplotypeCaller del sofatware GATK
## ![paula valenzuela@test-pomeo_~_variant_call 24-06-2021 13_36_52](https://user-images.githubusercontent.com/80971762/123454842-fd8f8800-d5ae-11eb-91d4-97d6a4721959.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_24_32](https://user-images.githubusercontent.com/80971762/123455834-2b290100-d5b0-11eb-98f9-680d1cb52b81.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_25_05](https://user-images.githubusercontent.com/80971762/123455922-4267ee80-d5b0-11eb-9514-7d78604b4308.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_25_52](https://user-images.githubusercontent.com/80971762/123455949-4a279300-d5b0-11eb-8d24-ecc5c889ea81.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_26_15](https://user-images.githubusercontent.com/80971762/123456012-5ad80900-d5b0-11eb-8957-a59dcf9ce294.png)

###### usar grep para contar el numero de lineas en el “vcf header”
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_27_10](https://user-images.githubusercontent.com/80971762/123456138-82c76c80-d5b0-11eb-9eac-ebf2f19c93e8.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_27_38](https://user-images.githubusercontent.com/80971762/123456189-8fe45b80-d5b0-11eb-930a-bc8fbde48fd6.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_27_38](https://user-images.githubusercontent.com/80971762/123456227-9bd01d80-d5b0-11eb-992e-b08746517d92.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_28_18](https://user-images.githubusercontent.com/80971762/123456261-a4c0ef00-d5b0-11eb-91ee-d45b42810a13.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_29_30](https://user-images.githubusercontent.com/80971762/123456286-ae4a5700-d5b0-11eb-940e-5a741e324c7b.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_30_02](https://user-images.githubusercontent.com/80971762/123456317-b73b2880-d5b0-11eb-9af8-c3d8cbafd18f.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_30_37](https://user-images.githubusercontent.com/80971762/123456356-bf936380-d5b0-11eb-976b-d7a8a1a8474c.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_30_37](https://user-images.githubusercontent.com/80971762/123456399-cb7f2580-d5b0-11eb-9e7f-e8db8f6eef91.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_30_58](https://user-images.githubusercontent.com/80971762/123456457-da65d800-d5b0-11eb-9069-da19d5966b55.png)

###### Extraer variantes con alta calidad
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_32_43](https://user-images.githubusercontent.com/80971762/123456585-01bca500-d5b1-11eb-9ac0-ac6afb921c05.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_33_13](https://user-images.githubusercontent.com/80971762/123456761-36306100-d5b1-11eb-8756-35d31c106dc9.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_33_29](https://user-images.githubusercontent.com/80971762/123456785-40525f80-d5b1-11eb-9d80-e094fa271fc2.png)

###### Análisis de variantes con vcftools
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_34_09](https://user-images.githubusercontent.com/80971762/123456916-6546d280-d5b1-11eb-839f-ec91328c97d7.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_34_57](https://user-images.githubusercontent.com/80971762/123457138-9c1ce880-d5b1-11eb-8034-4ab1469ec0df.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_35_53](https://user-images.githubusercontent.com/80971762/123457225-b35bd600-d5b1-11eb-8ea7-9d38a5ae8199.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_38_46](https://user-images.githubusercontent.com/80971762/123457347-d5edef00-d5b1-11eb-99fa-ecc06646acc0.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_39_06](https://user-images.githubusercontent.com/80971762/123457379-dbe3d000-d5b1-11eb-9555-18b74dae3cce.png)

##### Visualización de variantes con IGV
## ![paula valenzuela - paula valenzuela@200 54 220 141 - WinSCP 25-06-2021 11_40_16](https://user-images.githubusercontent.com/80971762/123457490-f7e77180-d5b1-11eb-86e5-a21bbe37e9e1.png)
## ![IGV 25-06-2021 11_42_32](https://user-images.githubusercontent.com/80971762/123457509-003fac80-d5b2-11eb-877a-1e412584439b.png)
## ![IGV 25-06-2021 11_48_22](https://user-images.githubusercontent.com/80971762/123457545-0766ba80-d5b2-11eb-921e-2c26fe62043f.png)





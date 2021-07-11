# ***Descripción genómica de la especie salmón del Atlántico (Salmo salar)***
##### - CURSO DBT 972 (GENÉTICA Y GENÓMICA EN PRODUCCIÓN ANIMAL)
#### Autor: 
- Paula Valenzuela Aviés
- Ingeniero en Biotecnología

### **Objetivos**
#### 1) Seleccionar una especie de interes comercial de la producción animal y buscar información de su genoma en Assembly, Refseq y Bioproyectos en SRA.
#### 2) Instalar y configurar el software para acceso remoto y transferencia de archivos.
#### 3) Instalación y configuración de software.
#### 4) Realizar el alineamiento de una muestra en formato .fastq a un genoma de referencia.
#### 5) Realizar el llamado de variantes de una secuencia de Salmo salar obtenida por secuenciación de extremos emparejados
#### 6) Realizar un analisis de genomica poblacional y ancestria en Salmo salar a partir de archivo de variantes VCF.
#### 7) Realizar un análisis de asociación genómico usando datos simulados de genotipos y fenotipos.


#### * Descripción del trabajo realizado*
##### Se Selecciono la especie de importancia económica en producción animal Salmón del Atlántico. En la primera etapa se buscó información de su genoma en Assembly y Refseq para resumir la información genómica de interés en REDME del repositorio Git: GenomicsEducation/PaulaValenzuela. Posteriomente se busco información del Bioproyectos en SRA que presenta el número de acceso **SRX1103127816S** que evalua el impacto de la alimetación en el microbioma intestinal de salmón del atlántico juvenil a través de la secuenciaón del 16S rRNA del instestino.<https://www.ncbi.nlm.nih.gov/sra/SRX11031278[accn]>. Por ultimo se descargo el metadata de las muestras en formato.txt archivada en ** Metadata 2 update**. En la segunda etapa se procedio a instalar y configurar el software para acceso remoto y transferencia de archivos.Está actividad fue realizada desde R-markdown a github con el objetivo de aprender a clonar el repositorio. La tercera etapa consitió en realizar un análisis de control de calidad de las secuencias NSG con fastqc, para esto el análisis se realizó desde la base de datos SRA del NCBI y corresponden lecturas crudas del salmón del Atlántico *Salmo salar* en formato fastq, obtenidas por secuenciación de extremos emparejados con un secuenciador Illumina HiSeq2000; Las descargas de las secuencias NGS se procesedió utilizando SRA toolkit, luego se comprobó la integridad de descarga de archivos usando md5sum o similar, posteriormente se realizó el análisis de control de calidad. Para finalizar esta etapa se realizó el filtrado y poda de secuencias utilizando el software trimmomatic y se transfirieron los archivos de control de calidad mediante protocolo FTP desde Servidor a Cliente. La cuarta etapa consistio en realizar un alinamiento de la muestra en formato .fastaq a un genoma de referencia que para este caso será con el genoma de la mitocondria del salmón del atlántico (dado su pequeño tamaño) para terminar con el análisis del alinamiento. En la quinta etapa se continuará utilizando las  secuencias filtradas o podadas pero ahora se encontrarán las variantes de las secuencias descargadas, esto comparandolas con el genoma de referencia DNA mitocondrial del salmón del  Atlantico utilizando el software  HaplotypeCaller de GATK, posteriormente el analisis de las variantes de realizará en Linux y vcftoolts, para terminar visualizandolas en IGV. La sexta etapa consitio el realizar un analisis de genoma poblacional y ancestria a partir de un archivo de variantes que contiene muestras provenientes de 3 poblaciones domesticadas de salmón del atlántico provenientes de Oceania, EE.UU, y Europa, para esto se estimaron algunas medidas de diversidad genetica, se realizó un filtrado por el equilibrio Hardy-weinberg, frecuencia del alelo menor, desequilibrio de ligamento, e individuos emparentados. Además en este analisis se se visualizó la subestructura de la población mediante graficas en R. La septima etapa consitió en realizar un análisis de asociación genomica (GWAs)

## ![Salmón del Atlántico](https://th.bing.com/th/id/OIP.yVdBR79JssLwOb82BdbHPgHaEK?pid=ImgDet&rs=1)

### _Actividades_

#### 1) Actividad 1. Selección de especie de interes e información en bases de datos públicas = https://github.com/GenomicsEducation/PaulaValenzuela/tree/main/Actividad%201.%20Bioproyecto
#### 2) Actividad 2. Instalación  y configurar el software para acceso remoto y transferencia de archivos= https://github.com/GenomicsEducation/PaulaValenzuela/tree/main/Actividad%202.%20%20Software%20de%20acceso%20remoto%20y%20transferencia%20de%20archivos
#### 3) Actividad 3. Instalación y configuración de software  = https://github.com/GenomicsEducation/PaulaValenzuela/tree/main/Actividad%203.%20Instalaci%C3%B3n%20y%20configuraci%C3%B3n%20de%20software
#### 4) Actividad 4. Alineamiento = https://github.com/GenomicsEducation/PaulaValenzuela/tree/main/Actividad%204.%20Alineamiento
#### 5) Actividad 5. Llamado de variantes = https://github.com/GenomicsEducation/PaulaValenzuela/tree/main/Actividad%205.%20Llamado%20de%20variantes
#### 6) Actividad 6. Genética poblacional y ancestría = https://github.com/GenomicsEducation/PaulaValenzuela/tree/main/Actividad%206.%20Gen%C3%A9tica%20poblacional%20y%20ancestr%C3%ADas
#### 7) Actividad 7. Asociación genómica GWAS y selección genómica = 

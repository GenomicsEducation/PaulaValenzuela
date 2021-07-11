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
### 6) Realizar un analisis de genomica poblacional y ancestria en Salmo salar a partir de archivo de variantes VCF.
### 7) Realizar un análisis de asociación genómico usando datos simulados de genotipos y fenotipos.


### * Descripción del trabajo realizado*
#### Se Selecciono la especie de importancia económica en producción animal Salmón del Atlántico. En la primera etapa se buscó información de su genoma en Assembly y Refseq para resumir la información genómica de interés en REDME del repositorio Git: GenomicsEducation/PaulaValenzuela. Posteriomente se busco información del Bioproyectos en SRA que presenta el número de acceso **SRX1103127816S** que evalua el impacto de la alimetación en el microbioma intestinal de salmón del atlántico juvenil a través de la secuenciaón del 16S rRNA del instestino.<https://www.ncbi.nlm.nih.gov/sra/SRX11031278[accn]>. Por ultimo se descargo el metadata de las muestras en formato.txt archivada en ** Metadata 2 update**. En la segunda etapa se procedio a instalar y configurar el software para acceso remoto y transferencia de archivos.Está actividad fue realizada desde R-markdown a github con el objetivo de aprender a clonar el repositorio. La tercera etapa consitió en realizar un análisis de control de calidad de las secuencias NSG con fastqc, para esto el análisis se realizó desde la base de datos SRA del NCBI y corresponden lecturas crudas del salmón del Atlántico *Salmo salar* en formato fastq, obtenidas por secuenciación de extremos emparejados con un secuenciador Illumina HiSeq2000; Las descargas de las secuencias NGS se procesedió utilizando SRA toolkit, luego se comprobó la integridad de descarga de archivos usando md5sum o similar, posteriormente se realizó el análisis de control de calidad. Para finalizar esta etapa se realizó el filtrado y poda de secuencias utilizando el software trimmomatic y se transfirieron los archivos de control de calidad mediante protocolo FTP desde Servidor a Cliente. La cuarta etapa consistio en realizar un alinamiento de la muestra en formato .fastaq a un genoma de referencia que para este caso será con el genoma de la mitocondria del salmón del atlántico (dado su pequeño tamaño) para terminar con el análisis del alinamiento. En la quinta etapa se continuará utilizando las  secuencias filtradas o podadas pero ahora se encontrarán las variantes de las secuencias descargadas, esto comparandolas con el genoma de referencia DNA mitocondrial del salmón del  Atlantico utilizando el software  HaplotypeCaller de GATK, posteriormente el analisis de las variantes de realizará en Linux y vcftoolts, para terminar visualizandolas en IGV. La sexta etapa consitio el realizar un analisis de genoma poblacional y ancestria a partir de un archivo de variantes que contiene muestras provenientes de 3 poblaciones domesticadas de salmón del atlántico provenientes de Oceania, EE.UU, y Europa, para esto se estimaron algunas medidas de diversidad genetica, se realizó un filtrado por el equilibrio Hardy-weinberg, frecuencia del alelo menor, desequilibrio de ligamento, e individuos emparentados. Además en este analisis se se visualizó la subestructura de la población mediante graficas en R. La septima etapa consitió en realizar un análisis de asociación genomica (GWAs)

## ![Salmón del Atlántico](https://th.bing.com/th/id/OIP.yVdBR79JssLwOb82BdbHPgHaEK?pid=ImgDet&rs=1)

### _Actividades_

#### 1) Actividad 1. Selección de especie de interes e información en bases de datos públicas = https://github.com/GenomicsEducation/PaulaValenzuela/commit/8ed79b801226f7d3d9f581d5b6720038f359086b
#### 2) Actividad 2. Instalación  y configurar el software para acceso remoto y transferencia de archivos= https://github.com/GenomicsEducation/PaulaValenzuela/commit/ce18f4877d11c538c01ca7b515f289a3c908bc03
#### 3) Actividad 3. Instalación y configuración de software = https://github.com/GenomicsEducation/PaulaValenzuela/commit/50f4f870b0a68fb6951fb394ef6789c770adc418
#### 4) Actividad 4. Alineamiento = https://github.com/GenomicsEducation/PaulaValenzuela/commit/000efdd5ccbc450a36c059b0d48c0ce9f9d169e8




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



###### 5.4) Comando HaplotypeCaller del sofatware GATK
## ![paula valenzuela@test-pomeo_~_variant_call 24-06-2021 13_36_52](https://user-images.githubusercontent.com/80971762/123454842-fd8f8800-d5ae-11eb-91d4-97d6a4721959.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_24_32](https://user-images.githubusercontent.com/80971762/123455834-2b290100-d5b0-11eb-98f9-680d1cb52b81.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_25_05](https://user-images.githubusercontent.com/80971762/123455922-4267ee80-d5b0-11eb-9514-7d78604b4308.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_25_52](https://user-images.githubusercontent.com/80971762/123455949-4a279300-d5b0-11eb-8d24-ecc5c889ea81.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_26_15](https://user-images.githubusercontent.com/80971762/123456012-5ad80900-d5b0-11eb-8957-a59dcf9ce294.png)

###### 5.5) Comando grep para contar el numero de lineas en el “vcf header”
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_27_10](https://user-images.githubusercontent.com/80971762/123456138-82c76c80-d5b0-11eb-9eac-ebf2f19c93e8.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_27_38](https://user-images.githubusercontent.com/80971762/123456189-8fe45b80-d5b0-11eb-930a-bc8fbde48fd6.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_27_38](https://user-images.githubusercontent.com/80971762/123456227-9bd01d80-d5b0-11eb-992e-b08746517d92.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_28_18](https://user-images.githubusercontent.com/80971762/123456261-a4c0ef00-d5b0-11eb-91ee-d45b42810a13.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_29_30](https://user-images.githubusercontent.com/80971762/123456286-ae4a5700-d5b0-11eb-940e-5a741e324c7b.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_30_02](https://user-images.githubusercontent.com/80971762/123456317-b73b2880-d5b0-11eb-9af8-c3d8cbafd18f.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_30_37](https://user-images.githubusercontent.com/80971762/123456356-bf936380-d5b0-11eb-976b-d7a8a1a8474c.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_30_37](https://user-images.githubusercontent.com/80971762/123456399-cb7f2580-d5b0-11eb-9e7f-e8db8f6eef91.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_30_58](https://user-images.githubusercontent.com/80971762/123456457-da65d800-d5b0-11eb-9069-da19d5966b55.png)

###### 5.6) Extracción de variantes con alta calidad
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_32_43](https://user-images.githubusercontent.com/80971762/123456585-01bca500-d5b1-11eb-9ac0-ac6afb921c05.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_33_13](https://user-images.githubusercontent.com/80971762/123456761-36306100-d5b1-11eb-8756-35d31c106dc9.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_33_29](https://user-images.githubusercontent.com/80971762/123456785-40525f80-d5b1-11eb-9d80-e094fa271fc2.png)

###### 5.7) Análisis de variantes con vcftools
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_34_09](https://user-images.githubusercontent.com/80971762/123456916-6546d280-d5b1-11eb-839f-ec91328c97d7.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_34_57](https://user-images.githubusercontent.com/80971762/123457138-9c1ce880-d5b1-11eb-8034-4ab1469ec0df.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_35_53](https://user-images.githubusercontent.com/80971762/123457225-b35bd600-d5b1-11eb-8ea7-9d38a5ae8199.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_38_46](https://user-images.githubusercontent.com/80971762/123457347-d5edef00-d5b1-11eb-99fa-ecc06646acc0.png)
## ![paula valenzuela@test-pomeo_~_variant_call 25-06-2021 11_39_06](https://user-images.githubusercontent.com/80971762/123457379-dbe3d000-d5b1-11eb-9555-18b74dae3cce.png)

##### 5.8) Visualización de variantes con IGV
## ![paula valenzuela - paula valenzuela@200 54 220 141 - WinSCP 25-06-2021 11_40_16](https://user-images.githubusercontent.com/80971762/123457490-f7e77180-d5b1-11eb-86e5-a21bbe37e9e1.png)
## ![IGV 25-06-2021 11_42_32](https://user-images.githubusercontent.com/80971762/123457509-003fac80-d5b2-11eb-877a-1e412584439b.png)
## ![IGV 25-06-2021 11_48_22](https://user-images.githubusercontent.com/80971762/123457545-0766ba80-d5b2-11eb-921e-2c26fe62043f.png)

#### 6) Genética poblacional y ancestría 

##### 6.1) Instalar programas para analisis y entrara a directorio population 
## ![paula valenzuela@test-pomeo_~ 01-07-2021 11_32_57](https://user-images.githubusercontent.com/80971762/124182905-7bf39a80-da85-11eb-9a9e-289365e0e5d6.png)
## ![paula valenzuela@test-pomeo_~ 01-07-2021 11_34_03](https://user-images.githubusercontent.com/80971762/124182939-86ae2f80-da85-11eb-9d6d-3ba82808b806.png)
## ![paula valenzuela@test-pomeo_~_population 01-07-2021 11_35_14](https://user-images.githubusercontent.com/80971762/124183037-ab0a0c00-da85-11eb-8db2-3b09a0902cc0.png)

##### 6.2) Análisis de diversidad 
## ![paula valenzuela@test-pomeo_~_population 01-07-2021 11_36_40](https://user-images.githubusercontent.com/80971762/124183101-c4ab5380-da85-11eb-91d7-7a5b44bcdd37.png)
## ![paula valenzuela@test-pomeo_~_population 01-07-2021 11_37_18](https://user-images.githubusercontent.com/80971762/124183117-cecd5200-da85-11eb-99ea-43a14c32c786.png)
## ![paula valenzuela@test-pomeo_~_population 01-07-2021 12_06_48](https://user-images.githubusercontent.com/80971762/124183158-db51aa80-da85-11eb-9443-6a9ddde18689.png)
## ![paula valenzuela@test-pomeo_~_population 01-07-2021 12_07_05](https://user-images.githubusercontent.com/80971762/124183192-e4427c00-da85-11eb-99c2-76e7f2c80fec.png)
## ![paula valenzuela@test-pomeo_~_population 01-07-2021 12_07_32](https://user-images.githubusercontent.com/80971762/124183227-edcbe400-da85-11eb-8f5b-5a70449337ad.png)
## ![paula valenzuela@test-pomeo_~_population 01-07-2021 12_07_46](https://user-images.githubusercontent.com/80971762/124183257-f6241f00-da85-11eb-819c-f2e97c674329.png)
## ![paula valenzuela@test-pomeo_~_population 01-07-2021 12_08_10](https://user-images.githubusercontent.com/80971762/124183278-fd4b2d00-da85-11eb-908a-8e7df029a215.png)
## ![paula valenzuela@test-pomeo_~_population 01-07-2021 12_10_51](https://user-images.githubusercontent.com/80971762/124183335-0f2cd000-da86-11eb-946c-994f439b8cba.png)
## ![paula valenzuela@test-pomeo_~_population 01-07-2021 12_11_15](https://user-images.githubusercontent.com/80971762/124183358-1653de00-da86-11eb-94d6-cf52e47c4c5c.png)
## ![paula valenzuela@test-pomeo_~_population 01-07-2021 12_12_24](https://user-images.githubusercontent.com/80971762/124183375-1d7aec00-da86-11eb-9ce4-a8ce9fa20e82.png)
## ![paula valenzuela@test-pomeo_~_population 01-07-2021 12_12_46](https://user-images.githubusercontent.com/80971762/124183394-253a9080-da86-11eb-9966-83f88be194f8.png)

###### 6.2.1) Para la poblacion de Europa
## ![paula valenzuela@test-pomeo_~_population 01-07-2021 12_16_50](https://user-images.githubusercontent.com/80971762/124183509-53b86b80-da86-11eb-8456-7153582c7bed.png)

###### 6.2.2) Para la poblacion de Oceania
## ![paula valenzuela@test-pomeo_~_population 01-07-2021 12_17_31](https://user-images.githubusercontent.com/80971762/124183569-6a5ec280-da86-11eb-97d9-dc1bac54eb43.png)

###### 6.2.3) Para la poblacion de Norteamerica
## ![paula valenzuela@test-pomeo_~_population 01-07-2021 12_18_00](https://user-images.githubusercontent.com/80971762/124183619-7c406580-da86-11eb-8829-09cb9c4de9c8.png)

##### 6.3) Desequilibrio de ligamiento (LD) de las tres poblaciones

###### 6.3.1) Para la poblacion de Europa
## ![paula valenzuela@test-pomeo_~_population 01-07-2021 12_19_22](https://user-images.githubusercontent.com/80971762/124183932-e6f1a100-da86-11eb-909c-5981e3dbfa94.png)

###### 6.3.2) Para la poblacion de Oceania
## ![paula valenzuela@test-pomeo_~_population 01-07-2021 12_19_41](https://user-images.githubusercontent.com/80971762/124184008-fbce3480-da86-11eb-9afb-1ef0cef1c722.png)
 
 ###### 6.3.3) Para la poblacion de Norteamerica
 ## ![paula valenzuela@test-pomeo_~_population 01-07-2021 12_20_03](https://user-images.githubusercontent.com/80971762/124184066-0e486e00-da87-11eb-9f6e-9230e6c7627b.png)

##### 6.4) El análisis de Heterogenicidad individual, diversidad de nucleotidos, desequilibrio de ligamento, gráficos de PCA y análisis visualizados en gráficos de ADMIXTURE para 2, 4 y 6 poblaciones; tambien se realizó en Rstudio el cual se podrá visualizar en el Archivo denominado Genética_poblacional.

##### 6.5) Analisis de estructura poblacional
## ![paula valenzuela@test-pomeo_~_population 01-07-2021 15_21_19](https://user-images.githubusercontent.com/80971762/124184220-3f28a300-da87-11eb-82b6-fcbdb3c95431.png)
## ![paula valenzuela@test-pomeo_~_population 01-07-2021 15_21_47](https://user-images.githubusercontent.com/80971762/124184252-4a7bce80-da87-11eb-8011-ab50bb25a7cc.png)

###### 6.5.1) Filtrar basado en equilibrio de Hardy-Weinberg y frecuencia del alelo menor
## ![paula valenzuela@test-pomeo_~_population 01-07-2021 15_23_26](https://user-images.githubusercontent.com/80971762/124185061-7186d000-da88-11eb-8e56-546f9a4e32e3.png)

###### 6.5.2) Filtrar y excluir marcadores por desequilibrio de ligamiento
## ![paula valenzuela@test-pomeo_~_population 01-07-2021 15_23_26](https://user-images.githubusercontent.com/80971762/124184913-3edcd780-da88-11eb-8477-35708d5ca821.png)
## ![paula valenzuela@test-pomeo_~_population 01-07-2021 15_24_06](https://user-images.githubusercontent.com/80971762/124184381-7bf49a00-da87-11eb-9da0-97bdfd7c3492.png)

###### 6.5.3) Filtrar para remover individuos relacionados
##  ![paula valenzuela@test-pomeo_~_population 01-07-2021 15_24_46](https://user-images.githubusercontent.com/80971762/124184428-8c0c7980-da87-11eb-8d86-6a92840ec28c.png)
## ![paula valenzuela@test-pomeo_~_population 01-07-2021 15_25_26](https://user-images.githubusercontent.com/80971762/124184464-9a5a9580-da87-11eb-96df-3f8abaca9457.png)

###### 6.5.4) PCA (Principal Component Analysis)
## ![paula valenzuela@test-pomeo_~_population 01-07-2021 15_25_49](https://user-images.githubusercontent.com/80971762/124184661-e574a880-da87-11eb-985f-b959503ca990.png)

#### 7) En análisis de asociación genómica se observa en el archivo adjunto: Practica de asociación genómica GWAS y selección genómica (realizada en Rstudio)

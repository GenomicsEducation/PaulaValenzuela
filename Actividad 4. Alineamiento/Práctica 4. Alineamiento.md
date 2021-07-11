#### 4) ETAPAS DE ALINEAMIENTO

##### 4.1) Alineamiento
###### El sotfware BWA es un algoritmo de alineación para alinear lecturas de secuencia o secuencias de consulta largas en este caso con el genoma de referencia del salmo salar (ICSAGS_V2), especificamente el mirocondrial (NC_001960.1). 
###### Por otra parte el sotfware Samtools, permite manipular alineaciones en los formatos SAM (Sequence Alignment Map), BAM y CRAM. Convierte entre los formatos, clasifica, fusiona e indexa, y puede recuperar lecturas en cualquier región rápidamente
## ![paula valenzuela@test-pomeo_~ 17-06-2021 12_16_51](https://user-images.githubusercontent.com/80971762/123139725-8332fc80-d424-11eb-98ef-244adadc6dd0.png)
## ![paula valenzuela@test-pomeo_~ 17-06-2021 12_16_59](https://user-images.githubusercontent.com/80971762/123139788-93e37280-d424-11eb-9ef3-c6d56f2b5ce7.png)
## ![paula valenzuela@test-pomeo_~ 17-06-2021 12_18_21](https://user-images.githubusercontent.com/80971762/123139837-9fcf3480-d424-11eb-9943-b91e6cbbe616.png)

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

## El arcchivo descomprimido se encuentra en la carpeta "archivos descomprimidos formato htlm"

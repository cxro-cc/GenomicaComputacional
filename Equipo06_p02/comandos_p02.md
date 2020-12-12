# Comandos de la Práctica 02
## Equipo 06
### Integrante 1: Carolina Caballero Cordero
### Integrante 2: Luis Angel Mancilla Galván 
### Integrante 3: Victor Alí Mancilla Gaytán

# Parte I. 

**Respuesta 1:**

![tabla](https://github.com/cxro-cc/Practica02_Equipo07/blob/main/tabla.jpg)

# Parte II.

**Respuesta 1:**

```
sed -n '1~4s/^@/>/p;2~4p' ERR486827_1.fastq > ERR486827_1.fasta
sed -n '1~4s/^@/>/p;2~4p' ERR486827_2.fastq > ERR486827_2.fasta
```

**Respuesta 2:**

```
grep -c '>' ERR486827_1.fasta
grep -c '>' ERR486827_2.fasta

```
ERR486827_1.fasta con 398827 secuencias.
ERR486827_1.fasta con 136550 secuencias.

**Respuesta 3:**

# Parte III.

**Respuesta 1:**
####Comandos para descomprimir y ejecutar fichero_ejecutable

```
λ unzip fastqc_v0.11.9.zip
λ chmod +x fastqc.

```
####Las secuencias que fueron ejecutables fueron 
ERR486827_1.fastq
ERR486827_2.fastq
ERR486828_1.fastq
ERR486828_2.fastq


**Respuesta 3:**

######Los datos de las secuencias tenian una calidad de secuencia por base, bastante buena, todas las lecturas aparecen en verde
######Ademas el heatmap es uniforme, y los valores de Phred son superiores a 38, con una certeza cercana al 99.99%, ademas de tener un contenido CG 
######con las amedias alineados aque correpaonden entre Cy G


**Respuesta 4:**

Las coverturas calculadas por 
```
covertura = (cantidad de lecturas*longitud de lecturas) / total del tamaño del genoma (bp)

```

fueron las siguientes:

ERR486827_1.fastq=73.323

ERR486827_2.fastq=73.323

ERR486828_1.fastq=75.544

ERR486828_2.fastq=75.544


# Parte IV.

**Respuesta 1:**

***Saccharomyces cerevisiae***

Es un hongo unicelular (levadura) del grupo de Ascomycota. Se encuentra sobre sustratos ricos de azúcares o en los exudados y savias dulces de algunas palntas. Se utiliza industrialmente en la fabricación de pan, cerveza y vino. Se reproduce de forma asexual por gemación. Es un organismo modelo para problemáticas biológicas por su rápido crecimeinto, la dispersión de las células y el sencillo sistema de transformación de DNA. 

![cerevisiae](https://github.com/cxro-cc/GenomicaComputacional/blob/main/Equipo06_p02/saccharomyces.jpeg)

No tiene un gran tamaño, por ello nos pareció un buen organismo a elegir además de que fue sencillo encontrar su secuencia en formato
fastq de [NCBI](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM2527046).

**Respuesta 2:**

Se utilizó la tecnología de [*Illumina MiSeq*](https://www.illumina.com/content/dam/illumina-marketing/documents/products/illumina_sequencing_introduction.pdf) que combina tecnología reconocida de secuenciación por síntesis, la cual ocupa una serie de cuatro pasos:
**Preparación de la libreria** La cual se prepara con una fragmentación aleatoria del DNA o de una muestra de cDNA, después los fragmentos son amplificados por PCR.
**Generación de cluster** Cada fragmento es amplificado con distintos clusters para así empezar la secuenciación. **Secuenciación** Basada en un método basado en terminadores que detecta cada base y las incorpora a un molde de la cadena del DNA. **Análisis de datos** Después de obtener la secuencia se pueden obtener diferentes variaciones en el análisis como análisis con SNP o identificación de inserciones y deleciones.
Las secuencias de .fastqc se tomaron del artículo [Comprehensive and quantitative mapping of RNA–protein interactions across a transcribed eukaryotic genome](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM2527046)


**Resepuesta 3:**

1.	Total de secuencias leídas 85046
2.	La longitud era de 75
3.	Y el tamaño del genoma es de 3.6 Mb
1.	Por lo tanto el genoma tiene una lectura de X1.772

**Resepuesta 4:**

1.	El archivo tiene el nombre GSM2527046_AG1GY_128nM_SAM_offset0_0_NeighborhoodMapping_R1_001_fastqc y esta en GitHub\GenomicaComputacional\Equipo06_p02
2.	El genoma si bien en la calidad se secuenciación de base, además de tener un heatmap bastante homogéneo, sim embargo, el contenido de secuencias por base 
	del inicio mostro un empalme entre los valores de las bases, por ello no se podía afirmar que base era la adecuada, otro problema que genero fue el tener 
	mas de un pico en lalos gráficos de GC, además de no coincidir las medias de las curvas, por ello asumimos que tuvo errores la lectura en bases.
3.	Las secuencias a evaluar no fueron redundantes, pues no tiene duplicación de secuencias, pero el grafico de sobrerrepresentadas mostro un aumento al final de las mismas. 


**Resepuesta 5:**

1.	El valor phred fue de 37, esto indicaba un acierto de 99.9%

**Resepuesta 6:**

1.	Recomendamos quitar las secuencias sobre representativas, pero de igual manera se recomienda si es posible hacer mas lecturas. Quizá con un mayor numero de secuencias los 
datos se inclinen por una u otra base. 







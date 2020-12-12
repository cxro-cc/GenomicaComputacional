# Comandos de la Práctica 02
## Equipo 06
### Integrante 1: Carolina Caballero Cordero
### Integrante 2: Nombre(s) Apellido(s)
### Integrante 3: Nombre(s) Apellido(s)

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


# Parte IV.

**Respuesta 1:**

***Saccharomyces cerevisiae***

Es un hongo unicelular (levadura) del grupo de Ascomycota. Se encuentra sobre sustratos ricos de azúcares o en los exudados y savias dulces de algunas palntas. Se utiliza industrialmente en la fabricación de pan, cerveza y vino. Se reproduce de forma asexual por gemación. Es un organismo modelo para problemáticas biológicas por su rápido crecimeinto, la dispersión de las células y el sencillo sistema de transformación de DNA. 

![cerevisiae](https://github.com/cxro-cc/GenomicaComputacional/blob/main/Equipo06_p02/saccharomyces.jpeg)

**Respuesta 2:**

Se utilizó la tecnología de Illumina MiSeq que combina tecnología reconocida de secuenciación por síntesis. Las secuencias de .fastqc se tomaron del artículo [Comprehensive and quantitative mapping of RNA–protein interactions across a transcribed eukaryotic genome](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM2527046)







# Comandos de la Práctica 01
## Carolina Caballero Cordero

#Parte I.

**Respuesta 1:**

/bin/bash

**Respuesta 2:**

mkdir data filtered raw_data meta scripts figures archive

**Respuesta 3:**

mv filtered/ data/
mv raw_data/ data/

**Respuesta 4:**

Para tener una mejor organizaciónd e los datos que se van a utilizar. el directorio data/ que contiene a ra/ y filtered/ pertenece a los datos crudos y a los filtrados que se ocuparon para el análisis genómico.
archive/ posee los scripts que no "sirvieron" pero que no queremos borrar. 
meta/ metadatos para detallar información o documentos para procesar los datos.
fugures/ solo posee los scripts que generan alguna figura. 
scripts/ posee los scripts que se necesitan para correr el análisis.

#Parte II.

cd scripts/ && touch delay.sh
nano delay.sh

#!/bin/bash
echo "Después de la Parte I. necesito un descanso de exactamente 30 segundos."

**Respuesta 1:**

chmod 777 delay.sh

**Respuesta 2:**

ls -lth
bash delay.sh

**Respuesta 3:** 

#!/bin/bash
echo "Después de la Parte I. necesito un descanso de exactamente 30 segundos."
sleep 30
echo "Ya puedo continuar!"

**Respuesta 4:**

bash delay.sh &
kill -9 10758

#Parte III.

cd meta/ && touch SarsCov-2.txt
nano SarsCov-2.txt

**Respuesta 1:**

~/GenomicaComputacional/ccaballero_p01/meta

**Respuesta 2:**

~/Descargas/ 
mv sequence.fasta sarscov2_genome.fasta
mv sequence.gff3 sarscov2_genome.gff3

mv sequence.fasta splike_c.faa
mv 'sequence (1).fasta' splike_b.faa
mv 'sequence (2).fasta' splike_a.faa

cd GenomicaComputacional/ccaballero_p01/meta/ && touch SarsCov-2_Spike.txt

mv sarscov2_genome.fasta  sarscov2_assembly.fasta.gz  sarscov2_genome.gff3  splike_a.faa  splike_b.faa  splike_c.faa  SRR10971381_R1.fastq.gz  SRR10971381_R2.fastq.gz ../GenomicaComputacional/ccaballero_p01/data/raw_data/

#Parte IV.

**Respuesta 1:**

cd ~/GenomicaComputacional/ccaballero_p01/data/filtered

ln -s ~/GenomicaComputacional/ccaballero_p01/data/raw_data/splike_c.faa
ln -s ~/GenomicaComputacional/ccaballero_p01/data/raw_data/splike_b.faa
ln -s ~/GenomicaComputacional/ccaballero_p01/data/raw_data/splike_a.faa 


**Respuesta 2:**

cd data/filtered && touch glycoproteins.faa

**Respuesta 3:**

head -1 splike_c.faa 
>pdb|6VXX|C Chain C, SARS-CoV-2 spike glycoprotein

head -1 splike_b.faa 
>pdb|6VXX|B Chain B, SARS-CoV-2 spike glycoprotein

head -1 splike_a.faa 
>pdb|6VXX|A Chain A, SARS-CoV-2 spike glycoprotein

**Respuesta 4:**

less splike_a.faa >> glycoproteins.faa
less splike_b.faa >> glycoproteins.faa
less splike_c.faa >> glycoproteins.faa 

**Respuesta 5:**

mv data/raw_data/splike_*.faa archive/
Se eliminarón las ligas porque la ruta de origen es distinta

**Respuesta 6:**

head -3 sarscov2_genome.fasta
>NC_045512.2 Severe acute respiratory syndrome coronavirus 2 isolate Wuhan-Hu-1, complete genome
ATTAAAGGTTTATACCTTCCCAGGTAACAAACCAACCAACTTTCGATCTCTTGTAGATCTGTTCTCTAAA
CGAACTTTAAAATCTGTGTGGCTGTCACTCGGCTGCATGCTTAGTGCACTCACGCAGTATAATTAATAAC

zless sarscov2_assembly.fasta.gz | head -3
>NODE_1_length_264_cov_161.042781
CACAAATCTTAACACTCTTCCCTACACGACGCTCTTCCGATCTACGCCGGGCCATTCGTA
CGAACCGATACCTGTGGTAAAGGGTCCTACTGTATGGTGGTACACGAGTAGTAGCAAATG

En el archivo fasta que no está comrpimido aparecen las secuencias sin divisiones entre ellas, en cambio en los archivos comprimidos aparece la secuencia dividida por "nodos"

**Respuesta 7:**

grep -c '>' sarscov2_genome.fasta 
zless sarscov2_assembly.fasta.gz | grep -c '>'

**Respuesta 8:**

zless SRR10971381_R2.fastq.gz
zless SRR10971381_R2.fastq.gz | head -12
@SRR10971381.512_2
CGTGGAGTATGGCTACATACTACTTATTTGATGAGTCTGGTGAGTTTAAAGTGGCTTCACATATGTATTGTTCTTTCTACCCTCCAGATGAGGATGAAGAAGAAGGTGATTGTGAAGAAGAAGAGTTTGAGCCATCAACTCAATATGAGT
+
/FFFA/A/FFFF66FFFFFF/FF/FFFFFFFFFFFFF/AFFF6FFFA6FFFFF/FFFFFFFFFFFFFFFFFF/FF/FFFFFA/FFF/FFF/A/AFA/FFFFF/=F/F/F/AFAFF//A/AFF//FFAF/FFF=FFAFFFA/A/6=///==
@SRR10971381.556_2
TTTGTAAAAATAAAATAAAAAAAATAAAAATAATATATTAAAAAAAGATAAATAAAAAAATGAACAATTAATAAAAAAAAAAAAAAAAAAAAATTAAAAAAAAAAAAAAAAAAAATAAAAAAAAAAAAAAATAAAAAAAAAATTATAAAA
+
6AFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFF/FFFAFFFFFF/FFA/FF=F//=FF/FFFFFFFFFFFFFA/FFFF/FF/FA//F/FFFFFFA/=FFFFF/FFFF/F=FFFAFF///FFFFA/FF/6//////=/
@SRR10971381.1428_2
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA
+
FFFFFFFFFFFFAFFFAFFFFFF6A//F//FFF

zless SRR10971381_R2.fastq.gz | grep -c '@'
130022

**Respuesta 9:**

Los archivos .faa hacen referencia a proteinas, tienen aminoacidos
.fastqc son archivos que contienen secuencias fasta con nucleotidos y los puntajes de calidad correspondientes.
.fasta son archivos con secuendias de nucleotidos

**Respuesta 10:**

Divide lo que esta en el archivo en columnas por tab

**Respuesta 11:**

grep 'gene' sarscov2_genome.gff3 | sort -k3  | cut -f3 | uniq -c

corresponde al tipo de molecula para el que codifican los datos. 13 CDS y 11 gen


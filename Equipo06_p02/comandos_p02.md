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

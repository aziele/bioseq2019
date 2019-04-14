### Zad. 1
Wejdź na stronę [NCBI](https://www.ncbi.nlm.nih.gov). Wybierz nukleotydową bazę danych (`Nucleotide`). Użyj zaawasowanego wyszukiwania (`Advanced`) i skonstruuj zapytanie:

```
insulin[Title] AND ("mus musculus"[Organism] OR "rattus norvegicus"[Organism]) AND "mrna"[Filter] AND "refseq"[Filter]
```

W wyniku otrzymano 53 sekwencje mRNA.

### Zad. 2
Wejdź na stronę [NCBI](https://www.ncbi.nlm.nih.gov). Wybierz nukleotydową bazę danych (`Protein`). Użyj zaawasowanego wyszukiwania (`Advanced`) i skonstruuj zapytanie:

```
alpha-globin[Title] AND "metazoa"[Organism] AND "pdb"[Filter]
```

W wyniku otrzymano 5 sekwencji białkowych.


### Zad. 3
Wejdź na stronę [NCBI](https://www.ncbi.nlm.nih.gov). Wybierz taksonomiczną bazę danych (`Taxonomy`). Odszukaj takson człowieka. W nowej karcie przeglądarki odszukaj takson myszy. Linia taksonomiczna człowieka i myszy jest wspólna od Eukaryota do nadrzędu Euarchontoglires.

Homo sapiens (taxid: `9606`):

```
Eukaryota; Metazoa; Chordata; Craniata; Vertebrata; Euteleostomi; Mammalia; Eutheria; Euarchontoglires;* Primates; Haplorrhini; Catarrhini; Hominidae; Homo
```

Mus musculus (taxid: `10090`)

```
Eukaryota; Metazoa; Chordata; Craniata; Vertebrata; Euteleostomi; Mammalia; Eutheria; Euarchontoglires;* Glires; Rodentia; Myomorpha; Muroidea; Muridae; Murinae; Mus; Mus
```

### Zad. 4
Wejdź na stronę bazy [UniProt](https://www.uniprot.org). Użyj zaawansowanego wyszukiwania.

1. Znaleziono: 12 610 białek.
2. Znaleziono: 24 tys. białek uwzględniając niższe jednostki taksonomiczne *Neisseria gonorrhoeae*. 


### Zad. 5
Wejdź na stronę bazy [UniProt](https://www.uniprot.org). Użyj zaawansowanego wyszukiwania, skonstruuj zapytanie: `existence:"Evidence at protein level [1]" length:[1 TO 10]`. W wyniku otrzymasz 1 144 białek z bazy SwissProt i 147 z bazy trEMBL.

1. Korzystając z zaawasnowanego wyszukiwania zmodyfikuj poprzednie zapytanie: `existence:"Evidence at protein level [1]" length:[1 TO 10] fragment:no`. W wyniku otrzymano 783 (SwissProt) i 65 (trEMBL) pełnej długości białka.
2. Korzystając z zaawansowanego wyszukiwania zmodyfikuj poprzednie zapytanie: `existence:"Evidence at protein level [1]" length:[1 TO 10] fragment:no AND organism:"Homo sapiens (Human) [9606]"`. W wyniku otrzymano 6 białek człowieka.

Zapisz sekwencje w formacie FASTA: przycisk `Download` > `Download all` > `Uncompressed` > Przycisk `GO`.

```
>sp|P0DPR3|TRDD1_HUMAN T cell receptor delta diversity 1 OS=Homo sapiens OX=9606 GN=TRDD1 PE=1 SV=1
EI
>sp|P22103|PNEU_HUMAN Pneumadin OS=Homo sapiens OX=9606 PE=1 SV=1
AGEPKLDAGV
>sp|P02728|GLEM_HUMAN Erythrocyte membrane glycopeptide OS=Homo sapiens OX=9606 PE=1 SV=1
CEGHSHDHGA
>sp|P02729|GLUR_HUMAN Urine glycopeptide OS=Homo sapiens OX=9606 PE=1 SV=1
CEHSHDGA
>sp|P01358|GAJU_HUMAN Gastric juice peptide 1 OS=Homo sapiens OX=9606 PE=1 SV=1
LAAGKVEDSD
>sp|P01858|TUFT_HUMAN Phagocytosis-stimulating peptide OS=Homo sapiens OX=9606 PE=1 SV=1
TKPR
```
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
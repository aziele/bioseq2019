### Zad. 1
Otwórz stronę [NCBI](https://www.ncbi.nlm.nih.gov). Z panelu `Popular Resources` wybierz nukleotydową bazę danych (`Nucleotide`). Użyj zaawasowanego wyszukiwania (`Advanced`) i skonstruuj poniższe zapytanie:

```
insulin[Title] AND ("mus musculus"[Organism] OR "rattus norvegicus"[Organism])
AND "mrna"[Filter] AND "refseq"[Filter]
```

W wyniku otrzymano **53** sekwencje mRNA myszy i szczura pochodzące z bazy RefSeq.
<br/><br/>


### Zad. 2
Otwórz stronę [NCBI](https://www.ncbi.nlm.nih.gov). Wybierz białkową bazę danych (`Protein`). Użyj zaawasowanego wyszukiwania (`Advanced`) i skonstruuj poniższe zapytanie:

```
alpha-globin[Title] AND "metazoa"[Organism] AND "pdb"[Filter]
```

W wyniku otrzymano **5** zwierzęcych sekwencji białek o rozwiązanej strukturze przestrzennej. 
<br/><br/>


### Zad. 3
Otwórz stronę [NCBI](https://www.ncbi.nlm.nih.gov). Wybierz taksonomiczną bazę danych (`Taxonomy`). Odszukaj takson człowieka wpisując w polu wyszukiwania `human` lub `homo sapiens`. W nowej karcie przeglądarki internetowej odszukaj takson myszy wpisując w polu wyszukiwania `mouse` lub `mus musculus`. 

Linia taksonomiczna (`Lineage`) człowieka i myszy jest wspólna od korzenia *Eukaryota* do nadrzędu *Euarchontoglires*.

#### Homo sapiens (taxId: 9606):

```
Eukaryota; Metazoa; Chordata; Craniata; Vertebrata; Euteleostomi; Mammalia; Eutheria;
Euarchontoglires;Primates; Haplorrhini; Catarrhini; Hominidae; Homo
```

#### Mus musculus (taxId: 10090)

```
Eukaryota; Metazoa; Chordata; Craniata; Vertebrata; Euteleostomi; Mammalia; Eutheria;
Euarchontoglires; Glires; Rodentia; Myomorpha; Muroidea; Muridae; Murinae; Mus; Mus
```
<br/><br/>

### Zad. 4
Otwórz stronę [NCBI](https://www.ncbi.nlm.nih.gov). Wybierz taksonomiczną bazę danych (`Taxonomy`). Odszukaj takson wilka workowatego wpisując w polu wyszukiwania `Thylacinus cynocephalus`. 

<img src="./images/ncbi-taxonomy-wolf.png" alt="ncbi-taxonomy-wolf">

Dla wilka workowatego dostępnych jest `82` sekwencji nukleotydowych i `717` sekwencji białkowych.
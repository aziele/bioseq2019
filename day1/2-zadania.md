### Zad. 1 - Znajdź białko BRCA2 człowieka
W serwisie [Uniprot](https://www.uniprot.org/) znajdź białko człowieka kodowane przez gen o nazwie (`Gene Name`) BRCA2. Odpowiedz na pytania:

1. Ile artykułów naukowych odnosi się do białka BRCA2?
2. Jaka mutacja w sekwencji białka BRCA2 powoduje raka trzustki (*pancreas cancer*)?
3. Podaj numer dostępu białka BRCA2 oraz jego mRNA w bazie *NCBI RefSeq*.
<br/><br/>

### Zad. 2 - Znajdź wszystkie białka bakterii dwoinki rzeżączki
W serwisie [Uniprot](https://www.uniprot.org/) znajdź wszystkie białka pochodzące z bakterii *Neisseria gonorrhoeae* (taxId: 485). 

1. Ile rekordów białek znaleziono?

Nad listą znalezionych białek naciśnij na link `"Expand search "Neisseria gonorrhoeae [485]" to include lower taxonomic ranks"`. 

2. Ile rekordów białek znaleziono w sumie dla wszystkich szczepów i podgatunków *Neisseria gonorrhoeae*?
<br><br>

### Zad. 3 - Czy w bazie UniProt znajdują się białka dinozaura?
W serwisie [UniProt](https://www.uniprot.org/) wyszukaj białka pochodzące z dinozaura *Tyrannosaurus rex*.

1. Ile rekordów znaleziono?
2. Jaką funkcję pełnią te białka w komórce?
3. Czy istnienie tych białek zostało potwierdzone doświadczalnie?
4. Co charakterystycznego znajduje się w sekwencjach tych białek?
<br/><br/>


### Zad. 4 - Znajdź najkrótsze sekwencje białkowe człowieka
Sprawdź, czy w bazie UniProt znajdują się doświadczalnie potwierdzone białka długości poniżej 10 aminokwasów?

1. Ile rekordów białek znaleziono?
2. Większość otrzymanych rekordów białek może być fragmentami innych, pełnej długości białek. Zawęź wyniki wyszukiwania do sekwencji nie będących fragmentami.
   * Ile białek znaleziono?
3. Ile z tych białek pochodzi z człowieka?

Zapisz otrzymane sekwencje w formacie FASTA.


### Zad. 5 - Analiza wzbogacenia terminów GO genów E. coli
W pliku [ecoli-genes.txt](./data/ecoli-genes.txt) znajduje się 218 genów, które ulegają różnicowej ekspresji w bakteriach *E.coli* wystawionych na działanie rtęci. Przeprowadź analizę wzbogacenia terminów GO tych genów wykorzystując serwis [AmiGO - Gene Ontology](http://amigo.geneontology.org/amigo).

1. Podaj dwa terminy GO związane z procesem biologicznym, które wykazują istotną nadreprezentację w zadanym zestawie genów.
2. Czy w zadanym zestawie występują istotnie nadreprezentowane terminy GO związane z funkcją molekularną?
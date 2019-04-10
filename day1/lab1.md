## Przeszukiwanie bazy Genbank i RefSeq


### Zad. 1 - Wyszukiwanie mRNA insuliny
Celem zadania jest wyszukanie wszystkich sekwencji mRNA insuliny człowieka.

#### Proste wyszukiwanie

1. W nukleotydowej bazie NCBI (`nucleotide`) wyszukaj wszystkie sekwencje insuliny.
2. Zawęź wyszukiwania do ogranizmu człowieka.
3. Zawęź wyszukiwania do sekwencji mRNA.

#### Zaawansowane wyszukiwanie

Skorzystaj z zaawansowanego wyszukiwania (`Advanced`) skonstruuj zapytanie do bazy danych tak, aby znaleźć wszystkie sekwencje insuliny:

<img src="./images/ncbi-advanced_search.png" />

4. człowieka
5. człowieka uzwględniając tylko sekwencje mRNA
6. człowieka uwzględniając tylko sekwencje mRNA i wykluczając frazy `insulin-like` i `partial`


### Zad. 2 - Od białka, przez mRNA, do genu
Znajdź sekwencję białkową genu o nazwie `BRCA2` człowieka pochodzącą z bazy RefSeq. Otwórz rekord znalezionej sekwencji.

1. Z ilu aminokwasów zbudowana jest to białko?
2. Jaki jest numer dostępu znalezionej sekwencji?
3. Jaki jest aktualny numer wersji rekordu?

Zapisz sekwencję białkową w formacie FASTA.

4. Jaki jest numer dostępu sekwencji mRNA tego białka?
5. Jaki jest identyfikator genu BRCA2 w bazie `Gene`?

Zapisz sekwencję mRNA w formacie FASTA. Przejdź do rekordu genu `BRCA2`.

6. Czy nazwa genu BRCA2 ma synonimy?
7. Z ilu egzonów zbudowany jest ten gen?
8. Podaj lokalizację genu BRCA2 na sekwencji genomowej.

Zapisz sekwencję genomową genu BRCA2 w formacie FASTA.

9. Wyświetl sekwencję genomową genu dodając 1000 nukleotydów *upstream* i *downstream*.
10. Ile wariantów splicingowych ma ten gen?


### Zad. 3 - Od genu, przez mRNA do białka
W bazie `Gene` wyszukaj ludzki gen o nazwie `HFE`.

1. Podaj identyfikator genu HFE w bazie `Gene`.
2. Ile wariantów splicingowych ma ten gen?
   > Ile wśród nich koduje białko?
3. Jakiej lokalizacji w wariantach transkrypcyjnych, sekwencjach kodujących (CDS) i białkach odpowiada pozycja `8671`genu?


### Zad. 3 - Zasoby sekwencyjne pojedynczego gatunku
Korzystając z bazy `Taxonomy` wyszukaj wszystkie typy sekwencji dostępne w NCBI dla myszy.

1. Ile struktur białkowych dostępnych jest dla tego organizmu?
2. Ile sekwencji całogenomowych dostępnych jest dla tego organizmu?


### Zad. 4 - Wyszukiwanie sekwencji dla dowonlnej jednostki taksonomicznej
Korzystając z bazy `Taxonomy` wyświel taksonomię rzędu gryzoni (*Rodentia*).

1. Wyświetl zasoby sekwencji gryzoni.
2. Wróć do drzewa taksonomicznego i wyświetl je maksymalnie do 6 poziomów zagnieżdżenia.
3. Ogranicz drzewo tylko do organizmów o znanych sekwencjach genomów.
4. Wyświetl na drzewie taksonomicznym liczbę białek dla każdej jednostki taksonomicznej.
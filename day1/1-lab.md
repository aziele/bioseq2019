## Przeszukiwanie bazy Genbank i RefSeq

### Zad. 1 - Wyszukiwanie rekordu sekwencji po numerze dostępu
W bazie nukleotdyowej znajdź rekord sekwencji o numerze dostępu `AB001981`.

1. Jaki jest typ znalezionej sekwencja (DNA / mRNA)?
2. Z genomu jakiego organizmu pochodzi ta sekwencja?
3. Ile genów zawiera rekord tej sekwencji?
4. Co oznaczają poniższe linie w rekordzie?

   ```
   CDS             join(1104..1192,1306..1510,1614..1742)
   CDS             join(4915..5009,5165..5369,5474..5602)
   ```

5. Ile publikacji dotyczy analizowanego rekordu?

* Wyświetl sekwencję w formacie FASTA.

6. Czy format FASTA zawiera informacje o genach alfa-globin?

* Wróć do formatu GenBank. 
* Zapisz do pliku sekwencję w formacie GenBank. 
* Otwórz sekwencję w edytorze tekstu.
* Wyświetl rekord sekwencji w formie graficznej (*Graphics*).
<br/><br/>

### Zad. 2 - Wyszukiwanie sekwencji dla wielu numerów dostępu
W pliku [accession_numbers.txt](./data/accession_numbers.txt) znajduje się 10 numerów dostępu mRNA kodujących kinazy. Z serwisu NCBI otwórz bazę `Nucleotide` i skorzystaj z funkcji `Batch Entrez` pozwalającej wyszukać wiele rekordów sekwencji jednocześnie. Zapisz otrzymane sekwencje w formacie FASTA.
<br/><br/>

### Zad. 3 - Wyszukiwanie mRNA insuliny człowieka
Celem zadania jest wyszukanie wszystkich sekwencji mRNA insuliny człowieka.

#### Proste wyszukiwanie

1. W nukleotydowej bazie NCBI (`Nucleotide`), w polu wyszukiwania wpisz `insulin`.
2. Korzystając z filtrów zawęź wyszukiwanie do ogranizmu człowieka.
3. Korzystając z filtrów zawęź wyszukiwanie do sekwencji mRNA.

#### Zaawansowane wyszukiwanie

Korzystając z zaawansowanego wyszukiwania (`Advanced`) skonstruuj zapytanie do bazy danych, aby znaleźć wszystkie sekwencje w bazie nukleotydowej, w których wyraz `insulin` znajduje się w tytule rekordu. Zawężaj dalej wyniki, aby otrzymać sekwencje:

4. człowieka
5. mRNA człowieka
6. mRNA człowieka, które nie są fragmentami (wykluczając frazy `insulin-like`, `partial`, `part`)
<br/><br/>

### Zad. 4 - Od rekordu białka, przez mRNA do rekordu genu
Korzystając z zaawansowanego wyszukiwania bazy białkowej NCBI skonstruuj zapytanie, aby znaleźć dokładnie jedną sekwencję białkową genu o nazwie `BRCA2` człowieka pochodzącą z bazy RefSeq.

#### Rekord sekwencji białka

1. Z ilu aminokwasów zbudowana jest to białko?
2. Jaki jest numer dostępu znalezionej sekwencji?
3. Jaki jest aktualny numer wersji rekordu?

* Zapisz sekwencję białkową w formacie FASTA.

4. Jaki jest numer dostępu sekwencji mRNA kodującej to białka?

#### Rekord sekwencji mRNA

Przejź do rekordu mRNA.

5. Z ilu nukleotydów złożone jest mRNA genu BRCA2?
6. Podaj identyfikator genu BRCA2 w bazie `Gene`?

* Zapisz sekwencję mRNA w formacie FASTA. 

#### Rekord genu
Przejdź do rekordu genu `BRCA2`.

7. Z ilu egzonów zbudowany jest ten gen?
8. Podaj lokalizację genu BRCA2 na sekwencji genomowej.
9. Ile wariantów splicingowych ma ten gen?

* Zapisz sekwencję genomową genu BRCA2 w formacie FASTA.

10. Wyświetl sekwencję genomową genu dodając 1000 nukleotydów *upstream* i *downstream*.
<br/><br/>

## Baza genów (NCBI Gene)

### Zad. 5 - Od rekordu genu, przez mRNA do rekordu białka
Korzystając z zaawansowanego wyszukiwania znajdź w bazie `Gene` ludzki gen o nazwie `HFE`.

1. Podaj identyfikator genu HFE w bazie `Gene`.
2. Ile wariantów splicingowych ma ten gen?
   * Ile wśród nich koduje białko?
3. Podaj pozycję w wariantach transkrypcyjnych, sekwencjach kodujących (CDS) oraz w białkach odpowiadającą pozycji `8671` genu?
<br/><br/>

### Zad. 6 - Wyświetlanie SNP danego genu
Korzystając z zaawansowanego wyszukiwania znajdź w bazie `Gene` ludzki gen o nazwie `BRCA1`. Następnie:
* Z panelu `Related information` po prawej stronie wybierz `Variation Viewer`. 
* Ustaw widok na egzon 10 i wyświetl listę SNP na tym egzonie związanych z chorobotwórczością.
* Wybierz jeden SNP i scharakteryzuj zmianę nukleotydu oraz wpływ tej zmiany na sekwencję białkową.
<br/><br/>

## Baza taksonomiczna (NCBI Taxonomy)


### Zad. 7 - Zasoby sekwencyjne pojedynczego gatunku
Korzystając z bazy `Taxonomy` wyszukaj wszystkie typy sekwencji dostępne dla myszy.

1. Podaj identyfikator taksonomiczny myszy.
2. Ile sekwencji nukleotydowych dostępnych jest dla myszy oraz wszystkich jej podgatunków?
   * Jakiego typu sekwencje nukleotydowe są dostępne?
<br/><br/>


### Zad. 8 - Zasoby sekwencji dowolnej jednostki taksonomicznej
Korzystając z bazy `Taxonomy` wyświel przynależność taksonomiczną rzędu gryzoni (*Rodentia*).

1. Wyświetl drzewo taksonomiczne ograniczając je do maksymalnie sześciu poziomów.
2. Do jakiej podrodziny należy rodzaj `Rattus`.
3. Ogranicz drzewo tylko do organizmów o znanych sekwencjach genomów.
   * Czy genom szczura (*Rattus norvegicus*) jest dostępny?
4. Dla każdej jednostki taksonomicznej na drzewie wyświetl liczbę sekwencji białkowych.
   * Ile sekwencji białkowych dostępnych jest dla szczura?
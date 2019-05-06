## Przeszukiwanie bazy Genbank i RefSeq

### Zad. 1 - Wyszukiwanie rekordu sekwencji po numerze dostępu
W bazie nukleotdyowej [serwisu NCBI](https://www.ncbi.nlm.nih.gov) znajdź rekord sekwencji o numerze dostępu `AB001981`.

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
* Zapisz do pliku rekord sekwencji w formacie GenBank. 
* Otwórz sekwencję w edytorze tekstu.
* Wyświetl rekord sekwencji w formie graficznej (*Graphics*).
<br/><br/>

### Zad. 2 - Wyszukiwanie sekwencji dla wielu numerów dostępu
W [serwisie NCBI](https://www.ncbi.nlm.nih.gov), w bazie `Nucleotide` wyszukaj rekordy sekwencji dla poniższych 10 numerów dostępu.

```
XM_009313067
NM_001275793
NM_116919
XM_007825334
NM_023057
NM_070001
NM_020791
NM_001180785
XM_004367964
NM_001326476
```
<br/>

### Zad. 3 - Wyszukiwanie mRNA insuliny człowieka
Celem zadania jest wyszukanie wszystkich sekwencji mRNA insuliny człowieka.

#### Proste wyszukiwanie

1. W nukleotydowej bazie NCBI (`Nucleotide`), w polu wyszukiwania wpisz `insulin`.
2. Korzystając z filtrów zawęź kryteria wyszukiwania do sekwencji pochodzących z człowieka.
3. Korzystając z filtrów zawęź kryteria wyszukiwania do sekwencji mRNA.

#### Zaawansowane wyszukiwanie

Korzystając z zaawansowanego wyszukiwania (`Advanced`) skonstruuj zapytanie do bazy danych, aby znaleźć wszystkie sekwencje w bazie nukleotydowej, w których wyraz `insulin` znajduje się w tytule rekordu. Następnie zawężaj dalej kryteria wyszukiwania, aby otrzymać sekwencje:

4. człowieka
5. mRNA człowieka
6. mRNA człowieka, które nie są fragmentami (tj. wykluczając frazy `insulin-like`, `partial`, `part`)
<br/><br/>

### Zad. 4 - Od rekordu białka, przez mRNA do rekordu genu
Korzystając z zaawansowanego wyszukiwania bazy białkowej [NCBI](https://www.ncbi.nlm.nih.gov) skonstruuj zapytanie, aby znaleźć dokładnie jedną sekwencję białkową genu o nazwie `BRCA2` człowieka pochodzącą z bazy RefSeq.

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
9. Ile wariantów transkrypcyjnych (splicingowych) ma ten gen?

* Zapisz sekwencję genomową genu BRCA2 w formacie FASTA.

10. Wyświetl sekwencję genomową genu dodając `1000` nukleotydów *upstream* i *downstream*.
<br/><br/>

## Baza genów (NCBI Gene)

### Zad. 5 - Od rekordu genu, przez mRNA do rekordu białka
Korzystając z zaawansowanego wyszukiwania znajdź w bazie `Gene` ludzki gen o nazwie `HFE`.

1. Podaj identyfikator genu HFE w bazie `Gene`.
2. Ile wariantów transkryptów ma ten gen?
   * Ile wśród nich koduje białko?
3. Podaj pozycję w wariantach transkrypcyjnych, sekwencjach kodujących (CDS) oraz w białkach odpowiadającą pozycji `8671` genu?
<br/><br/>


## Baza taksonomiczna (NCBI Taxonomy)


### Zad. 6 - Zasoby sekwencji pojedynczego gatunku
Korzystając z bazy `Taxonomy` serwisu [NCBI](https://www.ncbi.nlm.nih.gov) wyszukaj wszystkie typy sekwencji dostępne dla myszy.

1. Podaj identyfikator taksonomiczny myszy (*Mus musculus* lub *mouse*).
2. Ile sekwencji nukleotydowych dostępnych jest dla myszy oraz wszystkich jej podgatunków?
   * Jakiego typu sekwencje nukleotydowe są dostępne?
<br/><br/>


### Zad. 7 - Zasoby sekwencji dowolnej jednostki taksonomicznej
Korzystając z bazy `Taxonomy` serwisu [NCBI](https://www.ncbi.nlm.nih.gov) wyświetl przynależność taksonomiczną rzędu gryzoni (*Rodentia*).

1. Wyświetl drzewo taksonomiczne rozszerzając je do sześciu poziomów rozgałęzienia.
2. Do jakiej podrodziny należy rodzaj `Rattus`?
3. Ogranicz widok drzewa tylko do organizmów o znanych sekwencjach genomów.
   * Czy genom szczura (*Rattus norvegicus*) jest dostępny?
4. Dla każdej jednostki taksonomicznej na drzewie wyświetl liczbę genów, sekwencji białkowych i nukleotydowych.
   * Ile sekwencji białkowych dostępnych jest dla szczura?
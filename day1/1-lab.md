## Przeszukiwanie bazy Genbank i RefSeq

### Zad. 1 - Wyszukiwanie rekordu sekwencji po numerze dostępu
W bazie nukleotdyowej znajdź rekord sekwencji o numerze dostępu `AB001981`.

1. Jakiego typu jest znaleziona sekwencja (DNA / mRNA)?
2. Z genomu jakiego organizmu pochodzi ta sekwencja?
3. Ile genów zawiera rekord tej sekwencji?
4. Co oznaczają poniższe linie w rekordzie?

   ```
   CDS             join(1104..1192,1306..1510,1614..1742)
   CDS             join(4915..5009,5165..5369,5474..5602)
   ```

5. Ile publikacji dotyczy analizowanego rekordu?

Wyświetl sekwencję w formacie FASTA.

6. Czy format FASTA zawiera informacje o genach alfa-globin?

Wróć do formatu GenBank. Zapisz do pliku sekwencję w formacie GenBank. Otwórz sekwencję w edytorze tekstu. Wyświetl rekord sekwencji w formie graficznej (*Graphics*).


### Zad. 2 - Wyszukiwanie sekwencji dla wielu numerów dostępu jednocześnie
W pliku [accession_numbers.txt](./day1/data/accession_numbers.txt) znajduje się 10 numerów dostępu mRNA kodujących kinazy. Przejdź do bazy `Nucleotide` i skorzystaj z funkcji `Batch Entrez` pozwalającej wyszukać wszystkie rekordy sekwencji. Zapisz sekwencje w formacie FASTA.


### Zad. 3 - Wyszukiwanie mRNA insuliny
Celem zadania jest wyszukanie wszystkich sekwencji mRNA insuliny człowieka.

#### Proste wyszukiwanie

1. W nukleotydowej bazie NCBI (`Nucleotide`) wyszukaj wszystkie sekwencje insuliny.
2. Zawęź wyszukiwania do ogranizmu człowieka.
3. Zawęź wyszukiwania do sekwencji mRNA.

#### Zaawansowane wyszukiwanie

Skorzystaj z zaawansowanego wyszukiwania (`Advanced`) skonstruuj zapytanie do bazy danych tak, aby znaleźć wszystkie sekwencje w bazie, w których wyraz `insulin` znajduje się w tytule rekordu. Zawężaj dalej wyniki, aby otrzymać sekwencje:


4. człowieka
5. człowieka uzwględniając tylko sekwencje mRNA
6. człowieka uwzględniając tylko sekwencje mRNA i wykluczając frazy `insulin-like` i `partial`
i `part` z tytułu rekordów


### Zad. 4 - Od białka, przez mRNA, do genu
Korzystając z zaawansowanego wyszukiwania skonstruuj tak zapytanie aby znaleźć dokładnie jedną sekwencję białkową genu o nazwie `BRCA2` człowieka pochodzącą z bazy RefSeq.

#### Białko

1. Z ilu aminokwasów zbudowana jest to białko?
2. Jaki jest numer dostępu znalezionej sekwencji?
3. Jaki jest aktualny numer wersji rekordu?

Zapisz sekwencję białkową w formacie FASTA.

4. Jaki jest numer dostępu sekwencji mRNA kodującej to białka?

#### mRNA

Przejź do rekordu mRNA.

5. Z ilu nukleotydów zbudowane jest to mRNA?
6. Jaki jest identyfikator genu BRCA2 w bazie `Gene`?

Zapisz sekwencję mRNA w formacie FASTA. 

#### Gen
Przejdź do rekordu genu `BRCA2`.

7. Z ilu egzonów zbudowany jest ten gen?
8. Podaj lokalizację genu BRCA2 na sekwencji genomowej.
9. Ile wariantów splicingowych ma ten gen?

Zapisz sekwencję genomową genu BRCA2 w formacie FASTA.

10. Wyświetl sekwencję genomową genu dodając 1000 nukleotydów *upstream* i *downstream*.


## Baza genów (NCBI Gene)


### Zad. 5 - Od genu, przez mRNA do białka
Korzystając z zaawansowanego wyszukiwania znajdź w bazie `Gene` ludzki gen o nazwie `HFE`.

1. Podaj identyfikator genu HFE w bazie `Gene`.
2. Ile wariantów splicingowych ma ten gen?
   > Ile wśród nich koduje białko?
3. Jakiej lokalizacji w wariantach transkrypcyjnych, sekwencjach kodujących (CDS) oraz w białkach odpowiada pozycja `8671` genu?


### Zad. 6 - Wyświetlanie wszystkich SNP danego genu
Korzystając z zaawansowanego wyszukiwania znajdź w bazie `Gene` ludzki gen o nazwie `BRCA1`. Z panelu `Related information` po prawej stronie wybierz `Variation Viewer`. Ustaw widok na egzon 10 i wyświetl listę SNP na tym egzonie związanych z chorobotwórczością. Wybierz jeden SNP i scharakteryzuj zmianę nukleotydu oraz wpływ tej zmiany na sekwencję białkową.


## Baza taksonomiczna (NCBI Taxonomy)


### Zad. 7 - Zasoby sekwencyjne pojedynczego gatunku
Korzystając z bazy `Taxonomy` wyszukaj wszystkie typy sekwencji dostępne w NCBI dla myszy.

1. Podaj identyfikator taksonomiczny myszy.
2. Ile sekwencji nukleotydowych dostępnych jest dla myszy wraz z wszystkimi jej podgatunkami?
   * Jakiego typu sekwencje nukleotydowe są dostępne?


### Zad. 8 - Wyszukiwanie sekwencji dla dowonlnej jednostki taksonomicznej
Korzystając z bazy `Taxonomy` wyświel przynależność taksonomiczną rzędu gryzoni (*Rodentia*).

1. Wyświetl drzewo maksymalnie do 6 poziomów zagnieżdżenia.
2. Do jakiej podrodziny należy rodzaj `Rattus`.
3. Ogranicz drzewo tylko do organizmów o znanych sekwencjach genomów.
   * Czy genom szczura (*Rattus norvegicus*) jest dostępny?
4. Wyświetl na drzewie taksonomicznym liczbę sekwencji białek dla każdej jednostki taksonomicznej.
   * Ile sekwencji białkowych dostępnych jest dla szczura?


## UniProt


### Zad. 9 - Stosowanie filtrów podczas wyszukiwania
Wejdź na stronę [serwisu Uniprot](https://www.uniprot.org/). W polu wyszukiwania wpisz `human insulin`.

1. Ile rekordów znaleziono?
2. Czy na liście wyników jest szukane białko?

W panelu po lewej stronie, pod `Filter "human" as:` wybierz `organism`, a pod `Filter "insulin" as:` wybierz `protein name`.

3. Ile rekordów zostało?
   * Na którym miejscu na liście białek znajduje się szukana insunlina człowieka?

W polu wyszukiwania dodaj frazę `NOT name:protein-like`.

5. Ile rekordów zostało?
   * Na którym miejscu na liście białek się szukana insulina człowieka?

W podobny sposób ogranicz wyniki do białek, które nie są receptorami.

6. Ile rekordów zostało?
   * Na którym miejscu na liście białek się szukana insulina człowieka.


### Zad. 10 - rekord sekwencji UniProt
Przejdź do rekordu insuliny człowieka naciskając na numer dostępu tego białka (`P01308`).

1. Ile referencji literaturowych dotyczy insuliny?
2. Jaka jest lokalizacja komórkowa insuliny?
3. Czy sekwencja posiada peptydy sygnałowe? (`PTM / Processing`)
4. Czy znane są warianty sekwencji związane z chorobami?
5. Jaki jest numer dostępu tego białka i odpowiadającego mRNA w bazie RefSeq?


### Zad. 11 - zaawansowane wyszukiwanie
Znajdź wszystkie białka posiadające peptydy sygnałowe (Advanced > wybierz `PTM/Processing` > `Molecule Processing` > wybierz `Signal peptide` > naciśnij `Search`).

1. Ile białek znaleziono?
   * Jak wygląda zapytanie do bazy danych?
2. Zawęź wyniki wyszukiwania do białek zawierających peptydy sygnałowe o jakiejkolwiek doświadczalnie potwierdzonej funkcji. 
   * Ile białek znaleziono?
   * Jak wygląda zapuytanie do bazy danych?
3. Zawęź wyniki wyszukiwania do białek pochodzących tylko z człowieka.
   * Ile białek znaleziono?
   * Jak wygląda zapytanie do bazy danych?


### Zad. 12 - zaawansowane wyszukiwanie
1. Znajdź wszystkie białka w UniProt pochodzące z *Neisseria gonorrhoeae* (taxId: 485). Ile białek znaleziono?
2. Naciśnij `"Expand search "Neisseria gonorrhoeae [485]" to include lower taxonomic ranks"`. Ile białek w sumie znaleziono dla wszystkich szczepów i podgatunków Neisseria gonorrhoeae?
3. Czy w bazie UniProt znajdują się doświadczalnie potwierdzone peptydy długości poniżej 10 aminokwasów?
   * Większość otrzymanych białek może być fragmentami innych białek. Zawęź wyniki do sekwencji pełnej długości (`Advanced` > `Sequence` > `Fragment` > `Sequence complete`). Ile białek znalezionio?
   * Ile z tych białek pochodzi z człowieka?
   * Zapisz otrzymane sekwencje w formacie FASTA.
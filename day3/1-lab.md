## PSI-BLAST

### Zad. 1 - Wyszukiwanie odległych sekwencji homologicznych
> Celem zadania jest znalezienie najbardziej podobnej sekwencji białkowej (do sekwencji wejściowej), która posiada rozwiązaną strukturę przestrzenną.

Poniżej znajduje się nieznana sekwencja białkowa (`QUERY1`)

```
>QUERY1
MKDTDLSTLLSIIRLTELKESKRNALLSLIFQLSVAYFIALVIVSRFVRYVNYITYNNLV
EFIIVLSLIMLIIVTDIFIKKYISKFSNILLETLNLKINSDNNFRREIINASKNHNDKNK
LYDLINKTFEKDNIEIKQLGLFIISSVINNFAYIILLSIGFILLNEVYSNLFSSRYTTIS
IFTLIVSYMLFIRNKIISSEEEEQIEYEKVATSYISSLINRILNTKFTENTTTIGQDKQL
YDSFKTPKIQYGAKVPVKLEEIKEVAKNIEHIPSKAYFVLLAESGLRPGELLNVSIENID
LKARIIWINKETQTKRAYFSFFSRKTAEFLEKVYLPAREEFIRANEKNIAKLAAANENQE
IDLEKWKAKLFPYKDDVLRRKIYEAMDRALGKRFELYALRRHFATYMQLKKVPPLAINIL
QGRVGPNEFRILKENYTVFTIEDLRKLYDEAGLVVLE
```

#### Standardowe przeszukanie BLAST

Zidentyfikuj tę sekwencję wykorzystując program BLAST. Ogranicz przeszukiwanie do bazy `PDB (Protein Data Bank proteins)`.

1. Ile istotnych statystycznie wyników zostało znalezionych (`E-value` < 0.005)?

#### Przeszukanie PSI-BLAST
Wróć do strony BLAST. Ogranicz wyszukiwanie do bazy danych `nr` (*non-redundant protein sequences*) oraz wybierz algorytm PSI–BLAST (*Position-Specific Iterated BLAST*).

2. Ile istotnych statystycznie wyników zostało znalezionych?
   > *Wskazówka*: zaznacz wszystkie istotne statystycznie wyniki poprzez `Select`: `All` w sekcji `Sequences producing significant alignments with E-value BETTER than threshold`
3. Jakie wartości `Query cover` przyjmują znaleziono przyrównania? (pomijając wynik identyczny)
4. Czy wśród istotnych statystycznie wyników znajduja się wyniki pochodzące z bazy PDB?
   > *Wskazówka*: szukaj identyfikatora bazy PDB w kolumnie `Accession`. Identyfikator składa się z min. 4 znaków, w których pierwszy jest cyfrą np. `1XYZ_A`

#### Druga iteracja PSI-BLAST
Wykonaj drugie przeszukiwanie BLAST w celu przygotowania matrycy PSSM (*Position-Specific Scoring Matrix*).
> Wybierz przycisk Go przy Run PSI-Blast iteration 2 (znajdziesz go nad i pod tabelą wyników)

5. Ile istotnych statystycznie wyników zostało znalezionych?
6. Ile wynosi wartość `Query cover` pierwszych 20 trafień (z wyłączeniem sekwencji identycznej)?
7. Co oznaczają wiersze w tabeli wyróżnione żółtym kolorem?
8. Dlaczego w wynikach drugiego przeszukiwania PSI-BLAST znajduje się więcej istotnie statystycznych wyników?

#### Zapisanie i użycie profilu PSSM
* Zapisz matrycę PSSM stworzoną przez PSI-BLAST (`Download` > `PSSM to restart search` > `PSSM`). 
* Wykorzystaj pobraną matrycę PSSM do przeszukania bazy PDB. W tym celu:
  - Otwórz stronę `protein BLAST` w nowej karcie przeglądarki.
  - Ogranicz wyszukiwanie do bazy danych `PDB`
  - Wybierz algorytm `PSI–BLAST` (Position-Specific Iterated BLAST).
  - Rozwiń menu `Algorithm parameters` i w części `Upload PSSM` załaduj zapisany wcześniej plik z matrycą PSSM.
  - Uruchom program BLAST.

9. Ile statystycznie istotnych wyników pochodzi z bazy PDB?
10. Podaj identyfikatory PDB i wartości E-value dwóch najlepszych wyników przeszukiwania.
11. Podaj wartości `Query cover`, `Identities` oraz `Sequence Similarity (Positives)` dla dwóch najlepszych trafień.
12. Jaką funkcję pełnią te białka?

#### Trzecia iteracja PSI-BLAST
Przeprowadź jeszcze jedną iterację PSI-BLAST. W tym celu:
* Wróć do karty przeglądarki, w której znajdują się wyniki przeszukiwania bazy `nr`
* Naciśnij przycisk `Go` znajdujący się obok `Run PSI-Blast iteration 3`
* Zapisz profil PSSM na dysk i nadaj mu nazwę `PSSM-iteration3.asn`.
* Użyj programu PSI-BLAST do przeszukania bazy `PDB` przy użyciu pobranego profilu PSSM `PSSM-iteration3.asn`.

13. Odpowiedz na pytania 9-11.


### Zad. 2 - PSSM Viewer: identyfikacja kluczowych aminokwasów
> Celem tego zadania jest identyfikacja pozycji i aminokwasów w sekwencji `QUERY` (z poprzedniego zadania), które są krytyczne do utrzymania prawidłowej struktury i funkcjonowania białka. Umożliwia to wybranie najbardziej prawdopodobnych miejsc do przeprowadzenia mutagenezy.

Otwórz stronę programu [NCBI PSSM Viewer](https://www.ncbi.nlm.nih.gov/Class/Structure/pssm/pssm_viewer.cgi).
* Zaznacz opcję `Scoremat file` i załaduj plik z profilem PSSM z poprzedniego zadania (`PSSM-iteration3.asn`)
* Zaznacz opcję `FASTA file` i załaduj plik z sekwencją QUERY.
* Naciśnij przycisk `Matrix View`

<img src="ncbi-pssm-viewer1.png" alt="ncbi-pssm-viewer1.png">

1. Wybierz cztery pozycje w sekwencji, które są dobrymi kandytami do przeprowadzania mutagenezy. Dla ułatwienia, wybierz cztery propozycje z poniższych ośmiu propozycji:
   * H271
   * R287
   * E290
   * Y334
   * F371
   * R379
   * R400
   * Y436
2. Naciśnij na kolumnę `Query` w tabeli w celu posortowania jej według malejących wartości punktacji.
   * Czy możesz zaproponować pozycje bardziej kluczowe niż te podane w poprzednim punkcie.
3. W której pozycji sekwencji tryptofan (`W`) ma największą wartość punktacji?
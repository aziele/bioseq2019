## Wyszukiwanie sekwencji podobnych (BLAST)

### Zad. 1 - Opis wyników programu BLAST
Poniżej znajduje się sekwencja mRNA insuliny gryzonia koszatniczki pospolitej (*Octodon degus*).

```
>M57671.1 Octodon degus insulin mRNA, complete cds
GCATTCTGAGGCATTCTCTAACAGGTTCTCGACCCTCCGCCATGGCCCCGTGGATGCATCTCCTCACCGT
GCTGGCCCTGCTGGCCCTCTGGGGACCCAACTCTGTTCAGGCCTATTCCAGCCAGCACCTGTGCGGCTCC
AACCTAGTGGAGGCACTGTACATGACATGTGGACGGAGTGGCTTCTATAGACCCCACGACCGCCGAGAGC
TGGAGGACCTCCAGGTGGAGCAGGCAGAACTGGGTCTGGAGGCAGGCGGCCTGCAGCCTTCGGCCCTGGA
GATGATTCTGCAGAAGCGCGGCATTGTGGATCAGTGCTGTAATAACATTTGCACATTTAACCAGCTGCAG
AACTACTGCAATGTCCCTTAGACACCTGCCTTGGGCCTGGCCTGCTGCTCTGCCCTGGCAACCAATAAAC
CCCTTGAATGAG
```

Ze strony serwisu [NCBI](https://www.ncbi.nlm.nih.gov) otwórz stronę programu `BLAST`. Wybierz program `Nucleotide BLAST`. W formularzu:

* W polu `Enter Query Sequence` umieść powyższą sekwencje w formacie FASTA
* W panelu  `Program Selection` wybierz `Somewhat similar sequences (blastn)`
* Uruchom program BLAST.

#### Odczytywanie wyników
Z listy otrzymanych trafień (panel *Descriptions*) zwróć uwagę na sekwencję, która uzyskała najwyższą wartość punktacji (`Max score`). Odpowiedz na poniższe pytania dotyczące tej sekwencji:

1. Jaki jest numer dostępu sekwencji?
2. Ile wynosi wartość punktacji `Max score`?
   * O czym informuje ten parametr?
3. Ile wynosi wartość punktacji `Total score`?
   * O czym informauje ten parametr?
4. Ile wynosi procent identyczności między sekwencją zapytania?
5. Ile wynosi wartość `Query cover`?
   * O czym informuje ten parametr?
6. Ile wynosi wartość `E-value`?
   * O czym informuje ten parametr?
7. Ile przerw wprowadzono w tym przyrównaniu?
8. Ile wynosi długość przyrównania?

Na liście otrzymanych trafień znajdź najwyżej punktowaną sekwencję insuliny człowieka (*Homo sapiens*), która nie jest syntetycznym konstruktem.

9. Odpowiedz na te same pytania 1-8 na temat przyrównania z sekwencją człowieka.

### Zad. 2 - Wielkość bazy danych i E-value
Przeprowadź ponowne przeszukiwanie programem BLAST stosując jako zapytanie mRNA insuliny koszatniczki pospolitej `M57671.1`. W formularzu:

* Ogranicz przeszukiwanie do organizmu człowieka
* W panelu  `Program Selection` wybierz `Somewhat similar sequences (blastn)`
* Uruchom program BLAST.

1. Czy w wynikach znalezione zostałe sekwencje człowieka z poprzedniego zadania?
2. Czy wartości parametrów punktacji, identyczności, E-value są takie same jak w poprzednim zadaniu?
3. Jaka jest wielkość (w liczbie nukleotydów) przeszukiwanej bazy danych użytej w tym i poprzednim zadaniu? 
   > `Search summary` > `Number of letters`
4. Ile wynosi stosunek wielkości obu baz danych?
5. Ile wynosi stosunek E-value uzyskanych w dwóch przeszukiwaniach?
6. Jaka jest zależność między wielkością bazy danych a wartością E-value dla przyrównań o takiej samej wartości punktacji?


### Zad. 3 - Istotność statystyczna wyników BLAST

#### Sekwencje nukleotydowe
* Skorzystaj z serwisu internetowego [SeqGen](http://www.cbs.dtu.dk/biotools/SeqGen-1.0/) i wygeneruj trzy losowe sekwencje DNA o długości 25pz.
* Otwórz serwis **nucleotide BLAST**. Użyj wygenerowanych sekwencji umieszczając je w polu `Enter Query Sequence` formularza BLAST.
   * W panelu `Program Selection` wybierz program `Somewhat similar sequences (blastn)`
   * W panelu `Algorithm parameters` ustaw:
      - Odznacza opcję `Automatically adjust parameters for short input sequences`
      - `Expected threshold` = `50`
      <img src="./images/ncbi-blast-algorithm_parameters1.png" alt="ncbi-blast-algorithm_parameters1.png" width="400px">

1. Czy BLAST zidentyfikował sekwencje w bazie danych podobne do sekwencji zapytania?
2. Ile na ogół wynosi długość przyrównań?
3. Jaki zakres punktacji `Max Score` mają znalezione trafienia?
4. Jaki zakres wartości `E-value` mają znalezione trafienia?
5. Czy uzyskane wyniki są istotne biologiczne / czy dostarczają informacji biologicznej?

#### Sekwencje aminokwasowe
* Skorzystaj z serwisu internetowego [SeqGen](http://www.cbs.dtu.dk/biotools/SeqGen-1.0/) i wygeneruj trzy losowe sekwencje białkowe o długości 25 aminokwasów.
* Otwórz serwis **protein BLAST**. Użyj wygenerowanych sekwencji umieszczając je w polu `Enter Query Sequence` formularza BLAST.
   * W panelu `Algorithm parameters` ustaw:
      - Odznacza opcję `Automatically adjust parameters for short input sequences`
      - `Expected threshold` = `1000`
    * Uruchom program BLAST.

6. Odpowiedz na pytania 1-5.

#### Porównanie przeszukiwań nukleotydowych i aminokwasowych
7. Przy przeszukiwaniach BLAST którym typem sekwencji (DNA czy białko) istnieje większe ryzyko otrzymania wyników fałszywie pozytywnych (przyrównań, które wydają się znaczące, ale w rzeczywistości nie są spokrewnione)?

### Zad. 4 - Wiele lokalnych przyrównań w obrębie porównywanych sekwencji
<img align="right" src="./images/jurassic_park.png" alt="Jurassic Park">W książce Michaela Crichtona *Jurassic Park* na podstawie fragmentu sekwencji DNA dinozaura odtworzono cały organizm gada. Poniżej znajduje się ta sekwencja. 

```
>DinoDNA from JURASSIC PARK  p. 103 nt 1-1200
GCGTTGCTGGCGTTTTTCCATAGGCTCCGCCCCCCTGACGAGCATCACAAAAATCGACGC
GGTGGCGAAACCCGACAGGACTATAAAGATACCAGGCGTTTCCCCCTGGAAGCTCCCTCG
TGTTCCGACCCTGCCGCTTACCGGATACCTGTCCGCCTTTCTCCCTTCGGGAAGCGTGGC
TGCTCACGCTGTACCTATCTCAGTTCGGTGTAGGTCGTTCGCTCCAAGCTGGGCTGTGTG
CCGTTCAGCCCGACCGCTGCGCCTTATCCGGTAACTATCGTCTTGAGTCCAACCCGGTAA
AGTAGGACAGGTGCCGGCAGCGCTCTGGGTCATTTTCGGCGAGGACCGCTTTCGCTGGAG
ATCGGCCTGTCGCTTGCGGTATTCGGAATCTTGCACGCCCTCGCTCAAGCCTTCGTCACT
CCAAACGTTTCGGCGAGAAGCAGGCCATTATCGCCGGCATGGCGGCCGACGCGCTGGGCT
GGCGTTCGCGACGCGAGGCTGGATGGCCTTCCCCATTATGATTCTTCTCGCTTCCGGCGG
CCCGCGTTGCAGGCCATGCTGTCCAGGCAGGTAGATGACGACCATCAGGGACAGCTTCAA
CGGCTCTTACCAGCCTAACTTCGATCACTGGACCGCTGATCGTCACGGCGATTTATGCCG
CACATGGACGCGTTGCTGGCGTTTTTCCATAGGCTCCGCCCCCCTGACGAGCATCACAAA
CAAGTCAGAGGTGGCGAAACCCGACAGGACTATAAAGATACCAGGCGTTTCCCCCTGGAA
GCGCTCTCCTGTTCCGACCCTGCCGCTTACCGGATACCTGTCCGCCTTTCTCCCTTCGGG
CTTTCTCAATGCTCACGCTGTAGGTATCTCAGTTCGGTGTAGGTCGTTCGCTCCAAGCTG
ACGAACCCCCCGTTCAGCCCGACCGCTGCGCCTTATCCGGTAACTATCGTCTTGAGTCCA
ACACGACTTAACGGGTTGGCATGGATTGTAGGCGCCGCCCTATACCTTGTCTGCCTCCCC
GCGGTGCATGGAGCCGGGCCACCTCGACCTGAATGGAAGCCGGCGGCACCTCGCTAACGG
CCAAGAATTGGAGCCAATCAATTCTTGCGGAGAACTGTGAATGCGCAAACCAACCCTTGG
CCATCGCGTCCGCCATCTCCAGCAGCCGCACGCGGCGCATCTCGGGCAGCGTTGGGTCCT
```

Korzystając z programu `Nucleotide BLAST` i wybierając w nim algorytm `Highly similar sequences (megablast)` porównaj powyższą sekwencję z nukleotydową bazą sekwencji `Nucleotide collection (nr/nt)`. Następnie z listy trafień znajdź sekwencję, która najbardziej odpowiada sekwencji zapytania.

Odpowiedz na pytania:

1. Czy sekwencja rzeczywiście pochodzi z dinozaura?
2. Ile lokalnych przyrówań z sekwencją zapytania zostało zidentyfikowanych w tej sekwencji?
3. Ile wynosi wartość `Max score` i `Total score` dla tego przyrównania?
4. Spójrz na lokalne przyrównanie o najwyższej wartości `Max score`.
   * Podaj pozycję startu i końca tego przyrównania w sekwencji `Query` i `Subject`
   * Dlaczego pozycja startu w sekwencji `Subject` jest większa od pozycji końca?
5. Spójrz na pozostałe lokalne przyrównania z sekwencją `Subject`.
   * Jakie modyfikacje wprowadził Michael Crichron do sekwencji źródłowej?


### Zad. 5 - Blastx
<img align="right" src="./images/jp-lostworld.png" alt="Jurassic Park - Lost World"> Mark Boguski, pracownik NCBI, zauważył, że sekwencje ukazana w książce *Jurassic Park* nie była zbyt dobrze dobrana. Dlatego zaproponował, aby w filmie *Jurassic Park – The Lost World* umieścić inną, lepszą sekwencję, która znajduje się poniżej.

```
>DinoDNA from THE LOST WORLD  p. 135
GAATTCCGGAAGCGAGCAAGAGATAAGTCCTGGCATCAGATACAGTTGGAGATAAGGACG
GACGTGTGGCAGCTCCCGCAGAGGATTCACTGGAAGTGCATTACCTATCCCATGGGAGCC
ATGGAGTTCGTGGCGCTGGGGGGGCCGGATGCGGGCTCCCCCACTCCGTTCCCTGATGAA
GCCGGAGCCTTCCTGGGGCTGGGGGGGGGCGAGAGGACGGAGGCGGGGGGGCTGCTGGCC
TCCTACCCCCCCTCAGGCCGCGTGTCCCTGGTGCCGTGGGCAGACACGGGTACTTTGGGG
ACCCCCCAGTGGGTGCCGCCCGCCACCCAAATGGAGCCCCCCCACTACCTGGAGCTGCTG
CAACCCCCCCGGGGCAGCCCCCCCCATCCCTCCTCCGGGCCCCTACTGCCACTCAGCAGC
GGGCCCCCACCCTGCGAGGCCCGTGAGTGCGTCATGGCCAGGAAGAACTGCGGAGCGACG
GCAACGCCGCTGTGGCGCCGGGACGGCACCGGGCATTACCTGTGCAACTGGGCCTCAGCC
TGCGGGCTCTACCACCGCCTCAACGGCCAGAACCGCCCGCTCATCCGCCCCAAAAAGCGC
CTGCTGGTGAGTAAGCGCGCAGGCACAGTGTGCAGCCACGAGCGTGAAAACTGCCAGACA
TCCACCACCACTCTGTGGCGTCGCAGCCCCATGGGGGACCCCGTCTGCAACAACATTCAC
GCCTGCGGCCTCTACTACAAACTGCACCAAGTGAACCGCCCCCTCACGATGCGCAAAGAC
GGAATCCAAACCCGAAACCGCAAAGTTTCCTCCAAGGGTAAAAAGCGGCGCCCCCCGGGG
GGGGGAAACCCCTCCGCCACCGCGGGAGGGGGCGCTCCTATGGGGGGAGGGGGGGACCCC
TCTATGCCCCCCCCGCCGCCCCCCCCGGCCGCCGCCCCCCCTCAAAGCGACGCTCTGTAC
GCTCTCGGCCCCGTGGTCCTTTCGGGCCATTTTCTGCCCTTTGGAAACTCCGGAGGGTTT
TTTGGGGGGGGGGCGGGGGGTTACACGGCCCCCCCGGGGCTGAGCCCGCAGATTTAAATA
ATAACTCTGACGTGGGCAAGTGGGCCTTGCTGAGAAGACAGTGTAACATAATAATTTGCA
CCTCGGCAATTGCAGAGGGTCGATCTCCACTTTGGACACAACAGGGCTACTCGGTAGGAC
CAGATAAGCACTTTGCTCCCTGGACTGAAAAAGAAAGGATTTATCTGTTTGCTTCTTGCT
GACAAATCCCTGTGAAAGGTAAAAGTCGGACACAGCAATCGATTATTTCTCGCCTGTGTG
AAATTACTGTGAATATTGTAAATATATATATATATATATATATATCTGTATAGAACAGCC
TCGGAGGCGGCATGGACCCAGCGTAGATCATGCTGGATTTGTACTGCCGGAATTC
``` 

W zaproponowanej przez siebie sekwencji Mark ukrył pewną wiadomość, którą można odczytać na poziomie aminokwasów. W tym celu należy porównać sekwencję Marka z białkową bazą `nr` przy pomocy programu **blastx**.

1. Z jakiego organizmu pochodzi sekwencja Marka?
2. Spójrz na przyrównanie tych sekwencji. Jak brzmi ukryta wiadomość?
3. Co oznaczają fragmenty dopasowania oznaczone małymi szarymi literami?


### Zad. 6 - Ograniczanie wyników wyszukiwania BLAST
> Gen **FOXP2** u naczelnych warunkuje zdolność komunikacji werbalnej. Obecność zaledwie jednej uszkodzonej kopii tego genu u człowieka prowadzi do poważnych zaburzeń artykulacji wyrazów. 

Celem zadania jest sprawdzenie, czy gen *FOXP2* występuje również u zwierząt innych niż naczelne.

* W białkowej bazie NCBI znajdź sekwencję genu o nazwie *FOXP2* u człowieka. 
* Wejdź na stronę rekordu tego białka. Przejdź na stronę serwisu BLAST bezpośrednio z rekordu sekwencji - w panelu znajdującym się po prawej stronie rekordu, w części `Analyze this sequence` wybierz opcję `Run BLAST`.
W formularzu programu BLAST ustaw ograniczenia przeszukiwania do:
   - bazy danych RefSeq (**Database**)
   - organizmu zwierząt (*Metazoa*) z wykluczeniem sekwencji pochodzących z naczelnych (*Primaters*)
<img src="./images/ncbi-blast-foxp2-form.png" alt="ncbi-blast-foxp2-form" width="500px">

* Uruchom program BLAST.

Z listy otrzymanych trafień wybierz jedną sekwencję, która najbardziej odpowiada sekwencji *FOXP2*.

1. Z jakiego organizmu pochodzi ta sekwencja?
2. Ile wynosi E-value tego dopasowania?
3. Podaj procent identyczności i podobieństwa tego dopasowania.
4. Ile przerw znajduje się w tym dopasowaniu?

#### Raport taksonomiczny (Taxonomy reports)

Skorzystaj z zakładki `Taxonomy reports`.

5. Ile trafień znaleziono wśród ssaków?
6. Czy program BLAST znalazł trafienia wśród ptaków, gadów lub płazów?
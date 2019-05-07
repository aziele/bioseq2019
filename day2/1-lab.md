## Wykres Dot Plot

### Zad. 1 - Interpretacja wykresów dot plot
W pliku [dotplot.fasta](./day1/data/dotplot.fasta) znajduje się 10 sekwencji nukleotydowych. Przy wykorzystaniu programu *dotmatcher* (<a href="http://www.bioinformatics.nl/cgi-bin/emboss/dotmatcher">http://www.bioinformatics.nl/cgi-bin/emboss/dotmatcher</a>) wykonaj analizy dot-plot dla podanych poniżej par sekwencji. 
> W polu `Matrix file` wpisz nazwę macierzy `EDNASIMPLE` (`+1` dla par nukleotdów zgodnych, `0` dla niezgodnych). W panelu `Additional section` wpisz długość słowa i wartość graniczną odpowiednio `15` i `10`.

1. s1:s1
2. s1:s10
3. s2:s2
4. s4:s5
5. s7:s8
6. s4:s4

## BLAST - blastn i blastp

### Zad. 2 - Opis wyników programu BLAST
Poniżej znajduje się sekwencja mRNA insuliny gryzonia koszatniczki pospolitej (*Octodon degus*). Celem zadania jest znalezienie najbardziej podobnych sekwencji mRNA człowieka.

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

W serwisie [NCBI](https://www.ncbi.nlm.nih.gov) otwórz stronę programu `BLAST`. Wybierz program `Nucleotide BLAST`. W formularzu programu:

* Umieść powyższą sekwencję w formacie FASTA w polu `Enter Query Sequence`.
* W panelu  `Program Selection` wybierz `Somewhat similar sequences (blastn)`
* Uruchom program BLAST.

#### Odczytywanie wyników
Z listy otrzymanych trafień (panel `Descriptions`) zidentyfikuj sekwencję, która uzyskała najwyższą wartość punktacji (`Max score`). Odpowiedz na poniższe pytania dotyczące tej sekwencji i jej przyrównania z sekwencją zapytania.

1. Jaki jest numer dostępu zidentyfikowanej sekwencji?
2. Ile wynosi wartość punktacji `Max score`?
   * O czym informuje ten parametr?
3. Ile wynosi wartość punktacji `Total score`?
   * O czym informauje ten parametr?
4. Ile wynosi procent identyczności między sekwencją zapytania (`Query`) i sekwencją z bazy danych (`Subject`)?
5. Ile wynosi wartość `Query cover`?
   * O czym informuje ten parametr?
6. Ile wynosi wartość `E-value`?
   * O czym informuje ten parametr?
7. Ile przerw znajduje się w tym przyrównaniu?
8. Ile wynosi długość przyrównania?

Na liście otrzymanych trafień znajdź najwyżej punktowaną sekwencję insuliny człowieka (*Homo sapiens*) nie będącą syntetycznym konstruktem.

* Odpowiedz na te same pytania 1-8 na temat przyrównania z sekwencją człowieka.

9. Jaka jest wielkość przeszukiwanej bazy danych (wyrażona liczbą nukleotydów)?
<br/><br/>


### Zad. 3 - Wpływ wielkości bazy danych na wartość E-value
Przeprowadź ponowne przeszukiwanie programem BLAST stosując jako zapytanie mRNA insuliny koszatniczki pospolitej `M57671.1`. W formularzu programu BLAST:

* Ogranicz przeszukiwanie do organizmu człowieka
* W panelu `Program Selection` wybierz `Somewhat similar sequences (blastn)`
* Uruchom program BLAST.

1. Czy w wynikach znalezione zostałe sekwencje człowieka z poprzedniego zadania?
2. Czy wartości poniższych parametrów przyrównania sekwencji zapytania z sekwencjami człowieka są takie same, jak w poprzednim zadaniu?
   * punktacja (`Max score`)
   * identyczność
   * *E*-value
3. Jaka jest wielkość przeszukiwanej bazy danych (wyrażona liczbą nukleotydów)?
4. Ile wynosi stosunek wielkości baz danych użytych w poprzednim oraz obecnym zadaniu?
5. Ile wynosi stosunek *E*-value uzyskanych w poprzednim oraz obecnym przeszukiwaniu?
6. Jaka jest zależność między wielkością bazy danych a wartością *E*-value dla przyrównań o takiej samej wartości punktacji?
<br/><br/>

### Zad. 4 - Istotność statystyczna wyników BLAST

#### Sekwencje nukleotydowe
* Skorzystaj z serwisu internetowego [SeqGen](http://www.cbs.dtu.dk/biotools/SeqGen-1.0/) i wygeneruj trzy losowe sekwencje DNA o długości 25 pz.
* Otwórz serwis [NCBI BLAST](https://blast.ncbi.nlm.nih.gov/Blast.cgi) i wybierz program `Nucleotide BLAST`. 
   * Umieść wygenerowane sekwencje w polu `Enter Query Sequence`.
   * W panelu `Program Selection` wybierz program `Somewhat similar sequences (blastn)`
   * W panelu `Algorithm parameters`:
      - Odznacz opcję `Automatically adjust parameters for short input sequences`
      - Ustaw `Expected threshold` = `50`
   
   <img src="./images/ncbi-blast-algorithm_parameters1.png" alt="ncbi-blast-algorithm_parameters1.png" width="400px">

1. Czy BLAST zidentyfikował sekwencje w bazie danych podobne do trzech sekwencji zapytania?
2. Jaki zakres długości mają znalezione przyrównania?
3. Jaki zakres punktacji `Max Score` mają znalezione trafienia?
4. Jaki zakres wartości `E-value` mają znalezione trafienia?
5. Czy uzyskane wyniki są istotne biologiczne - czy dostarczają informacji biologicznej?

#### Sekwencje aminokwasowe
* Skorzystaj z serwisu internetowego [SeqGen](http://www.cbs.dtu.dk/biotools/SeqGen-1.0/) i wygeneruj trzy losowe sekwencje białkowe o długości 25 aminokwasów.
* Otwórz serwis [NCBI BLAST](https://blast.ncbi.nlm.nih.gov/Blast.cgi) i wybierz program `Protein BLAST`. Użyj wygenerowanych sekwencji umieszczając je w polu `Enter Query Sequence` formularza BLAST.
   * W panelu `Algorithm parameters`:
      - Odznacza opcję `Automatically adjust parameters for short input sequences`
      - Ustaw `Expected threshold` na `1000`
    * Uruchom program BLAST.

6. Odpowiedz na pytania 1-5.

#### Porównanie istotności przeszukiwań nukleotydowych i aminokwasowych
7. Który typ sekwencji (DNA czy białko) obarczony jest większym ryzykiem otrzymania trafień fałszywie pozytywnych (tj. przyrównań, które wydają się znaczące, ale w rzeczywistości obejmują sekwencje niespokrewnione)?
<br/><br/>


### Zad. 5 - Wpływ długości sekwencji zapytania na wartość E-value
Poniżej znajdują się trzy różnej długości fragmenty tej samej sekwencji tRNA. Użyj programu BLAST w celu przeszukania nukleotydowej bazy sekwencji `Nucleotide collection (nr/nt)` w oparciu o poniższe sekwencje.

```
>tRNA
TGGGGTATCGCCAAGCGGTAAGG
>tRNA
TGGGGTATCGCCAAGCGGTAAGGCACCGG
>tRNA
TGGGGTATCGCCAAGCGGTAAGGCACCGGTTTTTG
```

1. Z genomu jakiego organizmu pochodzą powyższe sekwencje?
2. Jak zmienia się wartość `E-value` w zależności od długości przyrównania?
3. Jaki aminokwas przyłącza analizowana cząsteczka tRNA?
<br/><br/>

### Zad. 6 - Wiele lokalnych przyrównań w obrębie porównywanych sekwencji
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

Korzystając z programu `Nucleotide BLAST` i algorytmu `Highly similar sequences (megablast)` porównaj powyższą sekwencję z nukleotydową bazą sekwencji `Nucleotide collection (nr/nt)`. Następnie z listy trafień znajdź sekwencję, która najbardziej odpowiada sekwencji zapytania.

Odpowiedz na pytania:

1. Czy sekwencja rzeczywiście pochodzi z dinozaura?
2. Ile lokalnych przyrówań z sekwencją zapytania zostało zidentyfikowanych w tej sekwencji?
3. Ile wynosi wartość `Max score` i `Total score` dla tego przyrównania?
4. Spójrz na lokalne przyrównanie o najwyższej wartości `Max score`.
   * Podaj pozycję startu i końca tego przyrównania w sekwencji `Query` i `Subject`
   * Dlaczego pozycja startu w sekwencji `Subject` jest większa od pozycji końca?

#### Blast Two Sequences (Dot Matrix)
* Otwórz rekord sekwencji wektora i wyświetl sekwencje w formacie FASTA.
* W nowej karcie przeglądarki otwórz stronę [NCBI BLAST](https://blast.ncbi.nlm.nih.gov/Blast.cgi) i wybierz program `Nucleotide BLAST`.
* W formularzu programu BLAST:
   - Zaznacz opcję: `Align two or more sequences`
   - Wybierz program: `Somewhat similar sequences (blastn)`
   - Umieść sekwencję zapytania w polu `Enter Query Sequence`
   - Umieść sekwencję wektora w polu `Enter Subject Sequence`
* Naciśnij przycisk `BLAST`


5. Spójrz na przyrównanie i wykres `Dot Matrix` obu sekwencji.
   * Jakie modyfikacje wprowadził Michael Crichron w sekwencji źródłowej?
<br/><br/>


### Zad. 7 - Wybór bazy danych dla programu BLAST
> Gen **FOXP2** u naczelnych warunkuje zdolność komunikacji werbalnej. Obecność zaledwie jednej uszkodzonej kopii tego genu u człowieka prowadzi do poważnych zaburzeń artykulacji wyrazów. 

Celem zadania jest sprawdzenie, czy gen *FOXP2* występuje również u zwierząt innych niż naczelne.

* W białkowej bazie serwisu [NCBI](https://www.ncbi.nlm.nih.gov) znajdź sekwencję genu o nazwie *FOXP2* u człowieka. 
* Otwórz stronę rekordu tego białka.
* Przejdź na stronę serwisu BLAST bezpośrednio z rekordu sekwencji - w panelu znajdującym się po prawej stronie rekordu, w części `Analyze this sequence` wybierz opcję `Run BLAST`.
* W formularzu programu BLAST ustaw ograniczenia przeszukiwania do:
   - bazy danych *RefSeq* (pole `Database`)
   - zwierząt (*Metazoa*) z wykluczeniem sekwencji pochodzących z naczelnych (*Primaters*)
   <img src="./images/ncbi-blast-foxp2-form.png" alt="ncbi-blast-foxp2-form" width="500px">
* Uruchom program BLAST.

Z listy otrzymanych trafień wybierz jedną sekwencję, która najbardziej odpowiada sekwencji *FOXP2*.

1. Z jakiego organizmu pochodzi ta sekwencja?
2. Ile wynosi *E*-value tego przyrównania?
3. Podaj procent identyczności i podobieństwa sekwencji w tym przyrównaniu.
4. Ile przerw znajduje się w tym przyrównaniu?

#### Raport taksonomiczny (Taxonomy reports)

Skorzystaj z zakładki `Taxonomy reports`.

5. Ile trafień znaleziono wśród ssaków?
6. Czy program BLAST znalazł znaczące trafienia wśród ptaków, gadów lub płazów?
<br/><br/>

### Zad. 8 - Przeszukiwanie pełnych sekwencji genomu
> Celem zadania jest zidentyfikowanie lokalizacji i struktury genu na podstawie fragmentu sekwencji genomowej człowieka.

Otwórz stronę serwisu [BLAST](https://blast.ncbi.nlm.nih.gov/Blast.cgi). W polu wyszukiwania zatytułowanym `BLAST Genomes` wpisz `human`. Z listy autouzupełnień wybierz `human (taxId: 9606)`. W formularzu programu BLAST:
* Umieść sekwencję zapytania w polu `Enter Query Sequence`
* W polu `Database` wybierz aktualne złożenie sekwencji genomu człowieka: `Genome (GRCh38.p12 reference, Annotation Release 109)`.
* Uruchom program BLAST.

```
TGGGCAACAAAGCGAGACTCTATCTCAAAAAAAAAAAAGTTCATAAATTCAAAGTTATGA
ATTATTTTTAAAATAATAATAATTTACAATAAAGATGAGGACAAAGTGTGAGTAAATGGT
GGTTTCTATCCAGCTCTGTTGAGCTGAAGTGGCATCTCCCTGCTGGGGCTTTTGGGGAAG
AAGGGTGTGTGTTGCTCTTCAGATCCCAAGCCTCATGCCCCTACTGGGCCCTGTGGGGTG
CTTCTCAGCCCACCAGGAGAGCCACCGTTGGAACACACACGTGGGGGACCTGGTGGGTGC
CGGTGTGGTGAATGGGGGCCACAGCCTGACTCCAGGAAGCCAGCAAACTCGGAGCTGGAG
GAGTCAGGACACCCCCGATGAGTCAAGAGTTGGTTTTGCTGCCAGTTGACATCTGATTGA
ACCATCTCTTCACTTCTCCGTGCCTCACTTTCCTTACCAGACAGGCTCTGCTGATGCTGT
CCCTCTCCTGTTCAGTCGTGCCCTCACCGTTAAAGAGAAAGAGCAAACTGCTGGGCAGCA
GCATTGATTTTTTTAATGAAGTGGAAAGAGAGCTGGGAATAACAAGTCGGGCCCACCTCA
CCTGCCTCACCTGGTGGGTTTATTTGTTTTGTTTTTTTTTTTTTGTTTTGAGACAGAGTT
TCACCCTGTCACCCAGGCTGGAGTGCAGTGGTGTAATCTCAGCTCACTGCAACCTCCACC
TGCCAGGTTCAATTGATTCTCCTGCCTCAGCCTCCCCAGTAGCTGGGATTACAGGCACCT
GCCACATGCCTGGCTAATTATTGTATTTTTAGTAGAGATGGGGTTTTACCATGTTGGCCA
GGCTGGTCTCGATCTCCTGACCTCAGGTGATCCACCCACCTCGGCCTCCCAAAGTGCTGA
GATCACAGGCGTGAGCCACCATGCCTGGCCGTCACCTGGTGGTGTTGAATATGAACTGCT
GCGGTGTTGGTAAATTAAGCAAGCAGATAGATGTAAATAACGCTTGGGCAGGAATATGGA
GCACGGGATGAGGATGGGCGGCCAACTGTTAGAGAGGGTAGCAGGGAGGCTGAGATCTGC
CTGCCATGAACTGGGAGGAGAGGCTCCTCTCTCTCTTCACCCCCACTCTGCCCCCCAACA
CTCCTCAGAACTTATCCTCTCCTCTTCTTTCCCCAGGTGAACTTTGAACCAGGATGGCTG
AGCCCCGCCAGGAGTTCGAAGTGATGGAAGATCACGCTGGGACGTACGGGTTGGGGGACA
GGAAAGATCAGGGGGGCTACACCATGCACCAAGACCAAGAGGGTGACACGGACGCTGGCC
TGAAAGGTTAGTGGACAGCCATGCACAGCAGGCCCAGATCACTGCAAGCCAAGGGGTGGC
GGGAACAGTTTGCATCCAGAATTGCAAAGAAATTTTAAATACATTATTGTCTTAGACTGT
CAGTAAAGTAAAGCCTCATTAATTTGAGTGGGCCAAGATAACTCAAGCAGTGAGATAATG
GCCAGACACGGTGGCTCACGCCTGTAATCCCAGCACTTTGGAAGGCCCAGGCAGGAGGAT
CCCTTGAGGCCAGGAATTTGAGACCGGCCTGGGCAACATAGCAAGACCCCGTCTCTAAAA
TAATTTAAAAATTAGCCAGGTGTTGTGGTGCATGTCTATAGTCCTAGCTACTCAGGATGC
TGAGGCAGAAGGATCACTTGAGCCCAGGAGTTCAAGGTTGCAGTAAGCTGTGATTATAAA
ACTGCACTCCAGCCTGAGCAACAGAGCAAGACCCTGTCAAAAAAAAAAGAAAAGAAAAAA
GAAAGAAAGAAATTTACCTTGAGTTACCCACATGAGTGAATGTAGGGACAGAGATTTTAG
GGCCTTAACAATCTCTCAAATACAGGGTACTTTTTGAGGCATTAGCCACACCTGTTAGCT
TATAAATCAGTGGTATTGATTAGCATGTAAAATATGTGACTTTAAACATTGCTTTTTATC
TCTTACTTAGATCAGGCCTGAGTGGCCTCTCTTTAGCAAGAGTTGGTTAGCCCTGGGATT
CTTACTGTAGCCACATTAATAAACAACATCGACTTCTAAACATTCTATAATACCATCTTT
TGGCCAAATTGACTTCGCCTCTTCCTCTCTCTTTCCAAATGAAATGTGTTTCATTTCACT
GTCAGACCACATGGTTGGGGACCCCACAGAGCACACAGCCCTCCCTCTGCCTTCCCATGC
TGGCCCTTCACCCACTGCTGGAGTGCCAGGTTGGTCCAAGGGTTGGACCAAGTTGTCTGA
GGTTGTCTCAAGGTTGGTCGAGGCTGTCTCCGCGCTGGGTTGTGCTACAAGGAGCCCTTC
TTTCCATGGGTGTGGCTGGCAGTGAGTGCTCACAGCAACAGCCCACAGTGCAGCCCGAGG
GCAGGATGGACTCAGTCCCTGCCTCCATACCCATTTCTAAGGAGGCAAAATGGCAAACAC
TCTACTTTTCTCTTTTAATGCTAAAAATAAGAAAACACCTTGCAGCCCAGGGTATGGGTA
GTGCATGGAAGCCGTGGAGTTGTGAGGTGGGAAGTGACCTCTGCTGGATATGTCTATTCA
GGAAGATTGCTGGAGTGGGTGGGGTCTCTGGGAGGTCCCCTGAGTGTGGGAAGCTGGGAC
CACCAGCTTTCTCGCACAGGGAGTGGCCATCCCAGCTTGGAGAGGTTCCAGGACTGGTTG
GGAGGCACGTTTCAGATTTCTATCTGTTGAATCAGCGAAGATATTGGATTATGAGGAATT
TGGGAATTAGGAAAGTGGGTGCAGGTGGGTTGGGGGTAGGTGAAGGAAGACATGGGCGTA
TTGGGGGAGCAGGGGCTGCTCAGAGGTGTTCCAGAAGCTCTGGGTGAGGAGGTGAGAGGG
ACCGGGGAATGCAGCTCGGCCCAGCCTCCCTGCCTGAGGTCAGCCATCACGTGGTGATGG
CAAGATGGAAATGTGCTTTCTGACTGCTCCAGCCAGTGCTGCCAGATTCAGCTCCCCAGG
GAGGGCACCTGAGAGGCTCCAAGCCAGGAGATCTGTTTTCTCCTTTGTTTTGTTTTTTTT
TGTTTTGTTTTGTTTTATTATACTTTAAGTTCTAGGGTACATGTGCACAACGTGCAGGTT
TGTTACATATGTATACATGTGCCATGTTGGTGTGCTGCACCCATCAACTTGTCATTTACA
TTAGGTATATCTCCTAATGCTATCCCTCCCCCCTCCCCCCACCCCCTGTTTTCTCCTTTG
AATCCTTCTTAGAGGCCGGGTGCGGTGGCTCACGCCTGTAATCCCAGCACTTTGGGAGGC
TGCGGCAGGAGGATTGCTTGAGCCCAGGAGTTCCAGACCAGCCTGGGCAACATAGTGAGA
CCTCGTCTCTACAGATAATAATTTTAAAAATTATCCGGGCATAGTGGCATGCACCTATAG
TCCCAGCTACTCAAGAGGCAGAGGCAGGAGGATCACTTGAGCCCAGGAGGCGGAGGTTGC
CGTGAGCCAAGATCCCACCACTGCACTCCAGCCTGGGCGACAGAGACCCCCATGTCAAAT
AATAATAATAATAAATAAATCCTTCTCAGTCCCTTCCTCACTGTGTCCCCCTCCACTGAA
TTTTTCCACCTCCTCTCCCACTTCCCCCACTCCCGCTTTCCCTCTCCTTCTCTCCCCACT
CCATCTTTTTCTTTCTCTGCTGTTTCTCGTCCCTCCCTCCTCTCCATCCCACAACACTGC
CTACCCTGTCCCTGCCCCACCCTGGTGCTCAGGATGTGTGAAGTGAGGGGTGGTAGCCCC
CAAGACCTCAACCCCGAAGGTTAGCCTGTTGAAACCACTTTCTCCCAGCTGCCCCCCTGG
CAGTTGGTGCTGCTGGGGGAAACTGGGATTGGGGGCCAGATTTTGCCTCTTTTCCTGACA
AAGAGAGATGAAGAGTTCTCTCACCAGGTGCCTGGGACTGGGGTGTGGGTGTCCCAGCCT
```

Podaj nazwę znalezionego genu oraz jego lokalizację w sekwencji genomowej człowieka.
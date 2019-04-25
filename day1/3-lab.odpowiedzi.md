### Zad. 1 - Format zapisu przyrównania sekwencji nukleotydowych

1. Długość przyrównania wynosi **10** pozycji.
   > Długość przyrównania uwzględnia również przerwy (`-`).
2. Nukleotydy są zgodne na **6** pozycjach, a niezgodne na **1** pozycji.
3. Identycznośc sekwencji wynosi: `60%`. 
   > 6/10 * 100 = 60
4. Wartość punktacji przyrównania (`score`) wynosi `5`.
   > 2 + 2 - 2 + 2 - 1 + 2 - 2 + 2 - 2 + 2 = 5

<br/><br/>


### Zad. 2 - Format zapisu przyrównania sekwencji aminokwasowych
1. Identyczności wynosi `40%`.
   > 2/5 * 100 = 40
2. Wartośc punktacji przyrównania (`score`) wynosi `4`.
   > Wartości punktacji dla zgodnych i niezgodnych aminokwasów należy odczytać z macierzy substytucji <a href="ftp://ftp.ncbi.nlm.nih.gov/blast/matrices/BLOSUM62" target="_blank">BLOSUM62</a>. Na przykład, wartość punktacji dopasowanie aminokwasów `M-M` wynosi `5`.
   
   Obliczenia wartości punktacji całego przyrównania: `5 + 4 + 0 - 5 = 4`.
3. Procent podobieństwa sekwencji wynosi `60%`
   > 3/5 * 100 = 60
<br/><br/>


## Programy Needle i Water

### Zad. 3 - Przyrównanie lokalne i semi-globalne sekwencji DNA
Otwórz programy Needle i Water w osobnych kartach przeglądarki internetowej. Ustaw typ porównywanych sekwencji (`Enter a pair of`) jako `DNA`. Umieść pierwszą sekwencję w formacie FASTA w pierwszym oknie i drugą sekwencję w drugim oknie. Wykonaj przyrównanie.

#### Przyrównanie semi-globalne (Needle)

```
########################################
# Program: needle
# Rundate: Sun 14 Apr 2019 12:05:20
# Commandline: needle
#    -auto
#    -stdout
#    -asequence emboss_needle-I20190414-120519-0694-86100052-p2m.asequence
#    -bsequence emboss_needle-I20190414-120519-0694-86100052-p2m.bsequence
#    -gapopen 10.0
#    -gapextend 0.5
#    -endopen 10.0
#    -endextend 0.5
#    -aformat3 pair
#    -snucleotide1
#    -snucleotide2
# Align_format: pair
# Report_file: stdout
########################################

#=======================================
#
# Aligned_sequences: 2
# 1: DNA
# 2: CDS
# Matrix: EDNAFULL
# Gap_penalty: 10.0
# Extend_penalty: 0.5
#
# Length: 2113
# Identity:     327/2113 (15.5%)
# Similarity:   327/2113 (15.5%)
# Gaps:        1786/2113 (84.5%)
# Score: 1239.0
# 
#
#=======================================

DNA                1 GGCCTAGCTAGGGCTGCTGTCCTGGGGTGGGCTGGGAATGGGCAGCCATC     50
                                                                       
CDS                1 --------------------------------------------------      0

DNA               51 AGGCAGGGGCCCCCTCACTCCCCTACCCCGACAACCTCGGCCCACCCATG    100
                                                                       
CDS                1 --------------------------------------------------      0

DNA              101 GGGGCATCTCGGGCAACCAGAGATAGAGGGCAGGGGTCTGGGGACAGCAG    150
                                                                       
CDS                1 --------------------------------------------------      0

DNA              151 CGTGAAGAGCCCCGCCCTGCAGCCTCCCGCACTCCTGGTCTAATGTGGAA    200
                                                                       
CDS                1 --------------------------------------------------      0

DNA              201 AGTGGCCCAGATGAGGGCTTTGCTCTCCTGGAGACATTTGCCCCCAGCTG    250
                                                                       
CDS                1 --------------------------------------------------      0

DNA              251 TGAGCAGGGACAGGACTGGCCACCAGCGCCTGGTTAAGACTCTAATGACC    300
                                                                       
CDS                1 --------------------------------------------------      0

DNA              301 ACCCCTCCCGGCCCTGAGGAAGAGGTGCTGACGACCAAGGAGATATTCCC    350
                                                                       
CDS                1 --------------------------------------------------      0

DNA              351 GCAGACCCAGCAGCCGGGAAATGATCTGGAAAGTGCAGCCTCAGCCCCCA    400
                                                                       
CDS                1 --------------------------------------------------      0

DNA              401 GCCATCTGCCAGCCCCTGCACCTCAGGCCCTAATGGGCCAGGCGGCAAGG    450
                                                                       
CDS                1 --------------------------------------------------      0

DNA              451 TTGGCAGGTAGGGGAGATGGGCTCTGGGCCTATAAAGCCAGCAGGGACCC    500
                                                                       
CDS                1 --------------------------------------------------      0

DNA              501 AGCAGCCCTCACGCCCGGGACCAGCTGCATCACAGGAGGCCAGCGAGCAG    550
                                                                       
CDS                1 --------------------------------------------------      0

DNA              551 GTCTGTTCCAAGGGCCTTCGAGCCAGTCTGGGCCCCAGGGCTGCCCCACT    600
                                                                       
CDS                1 --------------------------------------------------      0

DNA              601 CGGGGTTCCAGAGCAGTTGGACCCCAGGTCTCAGCGGGAGGGTGTGGCTG    650
                                                                       
CDS                1 --------------------------------------------------      0

DNA              651 GGCTCTGAAGCATTTGGGTGAGCCCAGGGGCTCAGGGCAGGGCACCTGCC    700
                                                                       
CDS                1 --------------------------------------------------      0

DNA              701 TTCAGCGGCCTCAGCCTGCCTGTCTCCCAGGTCTCTGTCCTTCCACCATG    750
                                                                    |||
CDS                1 -----------------------------------------------ATG      3

DNA              751 GCCCTGTGGATGCACCTCCTGCCCCTGCTGGCGCTGCTGGCCCTCTGGGG    800
                     ||||||||||||||||||||||||||||||||||||||||||||||||||
CDS                4 GCCCTGTGGATGCACCTCCTGCCCCTGCTGGCGCTGCTGGCCCTCTGGGG     53

DNA              801 ACCCGAGCCAGCCCCGGCCTTTGTGAACCAGCACCTGTGCGGCCCCCACC    850
                     ||||||||||||||||||||||||||||||||||||||||||||||||||
CDS               54 ACCCGAGCCAGCCCCGGCCTTTGTGAACCAGCACCTGTGCGGCCCCCACC    103

DNA              851 TGGTGGAAGCCCTCTACCTGGTGTGCGGGGAGCGAGGTTTCTTCTACGCA    900
                     ||||||||||||||||||||||||||||||||||||||||||||||||||
CDS              104 TGGTGGAAGCCCTCTACCTGGTGTGCGGGGAGCGAGGTTTCTTCTACGCA    153

DNA              901 CCCAAGACCCGCCGGGAGGCGGAGGACCTGCAGGGTGAGCCCCACCGCCC    950
                     |||||||||||||||||||||||||||||||||                 
CDS              154 CCCAAGACCCGCCGGGAGGCGGAGGACCTGCAG-----------------    186

DNA              951 CTCCGTGCCCCCGCCGCCCCCAGCCACCCCCACTCCCGCTGCTCCCACCC   1000
                                                                       
CDS              187 --------------------------------------------------    186

DNA             1001 AGCCTGGGCAGAAGGGGACAGGAGGCTGCTACCAGTAGGGAGACAGGTGG   1050
                                                                       
CDS              187 --------------------------------------------------    186

DNA             1051 ACTTTTTAAAAAGAAATGAAGTTCTCTTGGTCACATCCTGAAAGTGACCA   1100
                                                                       
CDS              187 --------------------------------------------------    186

DNA             1101 GCTCCCTGTGGCCCCGGCAGAATCTCAGCCTGAGGACGGTATTGGCTTCG   1150
                                                                       
CDS              187 --------------------------------------------------    186

DNA             1151 GCAGCTGAGCTCCGAGATACCTCGGAGGGCACGGCAGGGTAGGGTCCTCC   1200
                                                                       
CDS              187 --------------------------------------------------    186

DNA             1201 CTCCACGTGCCCCTCGAGCAAATGCCTCGCAGCCCACTTCTCCACCCTCA   1250
                                                                       
CDS              187 --------------------------------------------------    186

DNA             1251 CCTGAGGACCGCAGCTTCCAGTGTTTTGTTGAGTACATCAAGTCCTGGGT   1300
                                                                       
CDS              187 --------------------------------------------------    186

DNA             1301 GACCTGCGGTCACAGGGTGCCCCACGCTGCCTGCCTGTGGCAAATGCCCC   1350
                                                                       
CDS              187 --------------------------------------------------    186

DNA             1351 ATGGCACCCTGAGGAAGGCATGGCTGCTGCCACGGTGGGCCAGACCCCTG   1400
                                                                       
CDS              187 --------------------------------------------------    186

DNA             1401 TCCCCGGGCTTCATGACAGCCTCCATAGTCAGGAAATGGGGCAGGCACTG   1450
                                                                       
CDS              187 --------------------------------------------------    186

DNA             1451 GTGACAGGCCCTGGAAAGACGTACCGGGGGTACCCGTTCAGCCTCCTGCC   1500
                                                                       
CDS              187 --------------------------------------------------    186

DNA             1501 ATGGCACCACCCAGGGCATTGAAGTCCTGTATGTCCACACCCAGTGTGGG   1550
                                                                       
CDS              187 --------------------------------------------------    186

DNA             1551 GCACCCTTCCTCAACCTGGGCCCAGCTCGGCTGAGGGGGTGAGGGCGTGA   1600
                                                                       
CDS              187 --------------------------------------------------    186

DNA             1601 CCTGGGGCTGGCGGGCAGGCGGGCACCATCTCTCCCTGACTGTGCCATCC   1650
                                                                       
CDS              187 --------------------------------------------------    186

DNA             1651 TGCGTGCCTCTTCCTCGCCGCTGTTCCGGACCTGCTCTGCGTGGCTCGCC   1700
                                                                       
CDS              187 --------------------------------------------------    186

DNA             1701 CTGGCAGTGGGGCAGGTGGAGCTGGGTGGGGGCTCTATCACGGGCAGCCT   1750
                           ||||||||||||||||||||||||||||||||||||||||||||
CDS              187 ------GTGGGGCAGGTGGAGCTGGGTGGGGGCTCTATCACGGGCAGCCT    230

DNA             1751 GCCACCCTTGGAGGGTCCCATGCAGAAGCGTGGCGTCGTGGATCAGTGCT   1800
                     ||||||||||||||||||||||||||||||||||||||||||||||||||
CDS              231 GCCACCCTTGGAGGGTCCCATGCAGAAGCGTGGCGTCGTGGATCAGTGCT    280

DNA             1801 GCACCAGCATCTGCTCCCTCTACCAGCTGCAGAACTACTGCAACTAGACT   1850
                     |||||||||||||||||||||||||||||||||||||||||||||||   
CDS              281 GCACCAGCATCTGCTCCCTCTACCAGCTGCAGAACTACTGCAACTAG---    327

DNA             1851 GGGCCCACAGCGACCCCGTGCCCACTGCCACCTGCACCAGCACCTGCTCC   1900
                                                                       
CDS              328 --------------------------------------------------    327

DNA             1901 CTCTACCAGCTGGAGAACCACAGCTGGCTGCGGCCCACAGCAGGCCCAAA   1950
                                                                       
CDS              328 --------------------------------------------------    327

DNA             1951 TGCGGCCCTGCACCCTCCTCACCTGCACATGAGTGATGGAATAAAGCCTT   2000
                                                                       
CDS              328 --------------------------------------------------    327

DNA             2001 GAACCAGCTCTGCTGTGCTGTTTGCGTGTTTGGGGGGCCCTGGGCAGACC   2050
                                                                       
CDS              328 --------------------------------------------------    327

DNA             2051 CCGCCGTCCTGGCACTGTTATGAGCCCCTCCCAGCTCTCTCCAAGCTCTC   2100
                                                                       
CDS              328 --------------------------------------------------    327

DNA             2101 GCCCGGCCTGCAG   2113
                                  
CDS              328 -------------    327


#---------------------------------------
#---------------------------------------
```

#### Przyrównanie lokalne (Water)

```
########################################
# Program: water
# Rundate: Sun 14 Apr 2019 12:05:26
# Commandline: water
#    -auto
#    -stdout
#    -asequence emboss_water-I20190414-120523-0124-13440315-p2m.asequence
#    -bsequence emboss_water-I20190414-120523-0124-13440315-p2m.bsequence
#    -gapopen 10.0
#    -gapextend 0.5
#    -aformat3 pair
#    -snucleotide1
#    -snucleotide2
# Align_format: pair
# Report_file: stdout
########################################

#=======================================
#
# Aligned_sequences: 2
# 1: DNA
# 2: CDS
# Matrix: EDNAFULL
# Gap_penalty: 10.0
# Extend_penalty: 0.5
#
# Length: 1100
# Identity:     327/1100 (29.7%)
# Similarity:   327/1100 (29.7%)
# Gaps:         773/1100 (70.3%)
# Score: 1239.0
# 
#
#=======================================

DNA              748 ATGGCCCTGTGGATGCACCTCCTGCCCCTGCTGGCGCTGCTGGCCCTCTG    797
                     ||||||||||||||||||||||||||||||||||||||||||||||||||
CDS                1 ATGGCCCTGTGGATGCACCTCCTGCCCCTGCTGGCGCTGCTGGCCCTCTG     50

DNA              798 GGGACCCGAGCCAGCCCCGGCCTTTGTGAACCAGCACCTGTGCGGCCCCC    847
                     ||||||||||||||||||||||||||||||||||||||||||||||||||
CDS               51 GGGACCCGAGCCAGCCCCGGCCTTTGTGAACCAGCACCTGTGCGGCCCCC    100

DNA              848 ACCTGGTGGAAGCCCTCTACCTGGTGTGCGGGGAGCGAGGTTTCTTCTAC    897
                     ||||||||||||||||||||||||||||||||||||||||||||||||||
CDS              101 ACCTGGTGGAAGCCCTCTACCTGGTGTGCGGGGAGCGAGGTTTCTTCTAC    150

DNA              898 GCACCCAAGACCCGCCGGGAGGCGGAGGACCTGCAGGGTGAGCCCCACCG    947
                     ||||||||||||||||||||||||||||||||||||              
CDS              151 GCACCCAAGACCCGCCGGGAGGCGGAGGACCTGCAG--------------    186

DNA              948 CCCCTCCGTGCCCCCGCCGCCCCCAGCCACCCCCACTCCCGCTGCTCCCA    997
                                                                       
CDS              187 --------------------------------------------------    186

DNA              998 CCCAGCCTGGGCAGAAGGGGACAGGAGGCTGCTACCAGTAGGGAGACAGG   1047
                                                                       
CDS              187 --------------------------------------------------    186

DNA             1048 TGGACTTTTTAAAAAGAAATGAAGTTCTCTTGGTCACATCCTGAAAGTGA   1097
                                                                       
CDS              187 --------------------------------------------------    186

DNA             1098 CCAGCTCCCTGTGGCCCCGGCAGAATCTCAGCCTGAGGACGGTATTGGCT   1147
                                                                       
CDS              187 --------------------------------------------------    186

DNA             1148 TCGGCAGCTGAGCTCCGAGATACCTCGGAGGGCACGGCAGGGTAGGGTCC   1197
                                                                       
CDS              187 --------------------------------------------------    186

DNA             1198 TCCCTCCACGTGCCCCTCGAGCAAATGCCTCGCAGCCCACTTCTCCACCC   1247
                                                                       
CDS              187 --------------------------------------------------    186

DNA             1248 TCACCTGAGGACCGCAGCTTCCAGTGTTTTGTTGAGTACATCAAGTCCTG   1297
                                                                       
CDS              187 --------------------------------------------------    186

DNA             1298 GGTGACCTGCGGTCACAGGGTGCCCCACGCTGCCTGCCTGTGGCAAATGC   1347
                                                                       
CDS              187 --------------------------------------------------    186

DNA             1348 CCCATGGCACCCTGAGGAAGGCATGGCTGCTGCCACGGTGGGCCAGACCC   1397
                                                                       
CDS              187 --------------------------------------------------    186

DNA             1398 CTGTCCCCGGGCTTCATGACAGCCTCCATAGTCAGGAAATGGGGCAGGCA   1447
                                                                       
CDS              187 --------------------------------------------------    186

DNA             1448 CTGGTGACAGGCCCTGGAAAGACGTACCGGGGGTACCCGTTCAGCCTCCT   1497
                                                                       
CDS              187 --------------------------------------------------    186

DNA             1498 GCCATGGCACCACCCAGGGCATTGAAGTCCTGTATGTCCACACCCAGTGT   1547
                                                                       
CDS              187 --------------------------------------------------    186

DNA             1548 GGGGCACCCTTCCTCAACCTGGGCCCAGCTCGGCTGAGGGGGTGAGGGCG   1597
                                                                       
CDS              187 --------------------------------------------------    186

DNA             1598 TGACCTGGGGCTGGCGGGCAGGCGGGCACCATCTCTCCCTGACTGTGCCA   1647
                                                                       
CDS              187 --------------------------------------------------    186

DNA             1648 TCCTGCGTGCCTCTTCCTCGCCGCTGTTCCGGACCTGCTCTGCGTGGCTC   1697
                                                                       
CDS              187 --------------------------------------------------    186

DNA             1698 GCCCTGGCAGTGGGGCAGGTGGAGCTGGGTGGGGGCTCTATCACGGGCAG   1747
                              |||||||||||||||||||||||||||||||||||||||||
CDS              187 ---------GTGGGGCAGGTGGAGCTGGGTGGGGGCTCTATCACGGGCAG    227

DNA             1748 CCTGCCACCCTTGGAGGGTCCCATGCAGAAGCGTGGCGTCGTGGATCAGT   1797
                     ||||||||||||||||||||||||||||||||||||||||||||||||||
CDS              228 CCTGCCACCCTTGGAGGGTCCCATGCAGAAGCGTGGCGTCGTGGATCAGT    277

DNA             1798 GCTGCACCAGCATCTGCTCCCTCTACCAGCTGCAGAACTACTGCAACTAG   1847
                     ||||||||||||||||||||||||||||||||||||||||||||||||||
CDS              278 GCTGCACCAGCATCTGCTCCCTCTACCAGCTGCAGAACTACTGCAACTAG    327


#---------------------------------------
#---------------------------------------
```

1. Badany gen składa się z dwóch egzonów. Na obu przyrównaniach widoczne są dopasowania dwóch osobnych fragmentów.
2. Pierwszy egzon jest w pozycji od `748` do `933`, a drugi egzon jest pozycji `1707-1847`.
3. Procent identyczności w programie *Needle* to `15.5%`, a w *Water* `29.7%`.
   * Ponieważ *Needle* porównuje sekwencje na całej długości, otrzymane przyrównanie zawiera dużą liczbę przerw, które zmniejszają procent identyczności.
<br/><br/>


### Zad. 4 - Przyrównanie lokalne i semi-globalne sekwencji aminokwasowych
Zadanie na podstawie [DTU Course](http://teaching.healthtech.dtu.dk/36611/index.php/ExPairwiseAlignment).

#### Przyrównanie semi-globalne (Needle)

Otwórz stronę programu [Needle](https://www.ebi.ac.uk/Tools/psa/emboss_needle/). Ustaw typ porównywanych sekwencji (`Enter a pair of`) jako `PROTEIN`. Umieść dwie sekwencje w formacie FASTA w osobnych polach. Wykonaj przyrównanie.


```
# Length: 361
# Identity:     176/361 (48.8%)
# Similarity:   214/361 (59.3%)
# Gaps:          92/361 (25.5%)
# Score: 916.0
# 
#
#=======================================

P29600             1 --------------------------------------------------      0
                                                                       
P41363             1 MRQSLKVMVLSTVALLFMANPAAASEEKKEYLIVVEPEEVSAQSVEESYD     50

P29600             1 ------------------------------------------AQSVPWGI      8
                                                               :|:|||||
P41363            51 VDVIHEFEEIPVIHAELTKKELKKLKKDPNVKAIEKNAEVTISQTVPWGI    100

P29600             9 SRVQAPAAHNRGLTGSGVKVAVLDTGISTHPDLNIRGGASFVPGEPSTQD     58
                     |.:....|||||:.|:|.:||||||||::||||.|.|||||:..|||..|
P41363           101 SFINTQQAHNRGIFGNGARVAVLDTGIASHPDLRIAGGASFISSEPSYHD    150

P29600            59 GNGHGTHVAGTIAALNNSIGVLGVAPSAELYAVKVLGASGSGSVSSIAQG    108
                     .|||||||||||||||||||||||||||:|||||||..:||||::|:|||
P41363           151 NNGHGTHVAGTIAALNNSIGVLGVAPSADLYAVKVLDRNGSGSLASVAQG    200

P29600           109 LEWAGNNGMHVANLSLGSPSPSATLEQAVNSATSRGVLVVAASGNSGAGS    158
                     :|||.||.||:.|:||||.|.|:|||.|||.|.:.|:|:|.|:||:|...
P41363           201 IEWAINNNMHIINMSLGSTSGSSTLELAVNRANNAGILLVGAAGNTGRQG    250

P29600           159 ISYPARYANAMAVGATDQNNNRASFSQYGAGLDIVAPGVNVQSTYPGSTY    208
                     ::|||||:..|||.|.|||..|||||.||..::|.||||||.|||.|:.|
P41363           251 VNYPARYSGVMAVAAVDQNGQRASFSTYGPEIEISAPGVNVNSTYTGNRY    300

P29600           209 ASLNGTSMATPHVAGAAALVKQKNPSWSNVQIRNHLKNTATSLGSTNLYG    258
                     .||:|||||||||||.|||||.:.||::|.|||..:..|||.|||.:|||
P41363           301 VSLSGTSMATPHVAGVAALVKSRYPSYTNNQIRQRINQTATYLGSPSLYG    350

P29600           259 SGLVNAEAATR    269
                     :|||:|..||:
P41363           351 NGLVHAGRATQ    361
```

1. Wartość punktacji przyrównania (`score`) to `916` bitów.
2. Długość przyrównania wynosi `361` pozycji.
3. Procent identyczności sekwencji to `176/361 (48.8%)`.
4. Procent podobieństwa sekwencji to `214/361 (59.3%)`
   > **Procent podobieństwa** sekwencji aminokwasowych jest zawsze większy lub równy od procentu identyczności. Podobieństwo, oprócz identycznych reszt aminokwasowych, uwzględnia również substytucje aminokwasów podobnych (tj. takie substytucje aminokwasów, które są dodatnio punktowane w użytej macierzy substytucji, w tym przypadku macierzy `BLOSUM62`).


#### Przyrównanie lokalne (Water)

```
# Length: 269
# Identity:     176/269 (65.4%)
# Similarity:   214/269 (79.6%)
# Gaps:           0/269 ( 0.0%)
# Score: 916.0
# 
#
#=======================================

P29600             1 AQSVPWGISRVQAPAAHNRGLTGSGVKVAVLDTGISTHPDLNIRGGASFV     50
                     :|:||||||.:....|||||:.|:|.:||||||||::||||.|.|||||:
P41363            93 SQTVPWGISFINTQQAHNRGIFGNGARVAVLDTGIASHPDLRIAGGASFI    142

P29600            51 PGEPSTQDGNGHGTHVAGTIAALNNSIGVLGVAPSAELYAVKVLGASGSG    100
                     ..|||..|.|||||||||||||||||||||||||||:|||||||..:|||
P41363           143 SSEPSYHDNNGHGTHVAGTIAALNNSIGVLGVAPSADLYAVKVLDRNGSG    192

P29600           101 SVSSIAQGLEWAGNNGMHVANLSLGSPSPSATLEQAVNSATSRGVLVVAA    150
                     |::|:|||:|||.||.||:.|:||||.|.|:|||.|||.|.:.|:|:|.|
P41363           193 SLASVAQGIEWAINNNMHIINMSLGSTSGSSTLELAVNRANNAGILLVGA    242

P29600           151 SGNSGAGSISYPARYANAMAVGATDQNNNRASFSQYGAGLDIVAPGVNVQ    200
                     :||:|...::|||||:..|||.|.|||..|||||.||..::|.||||||.
P41363           243 AGNTGRQGVNYPARYSGVMAVAAVDQNGQRASFSTYGPEIEISAPGVNVN    292

P29600           201 STYPGSTYASLNGTSMATPHVAGAAALVKQKNPSWSNVQIRNHLKNTATS    250
                     |||.|:.|.||:|||||||||||.|||||.:.||::|.|||..:..|||.
P41363           293 STYTGNRYVSLSGTSMATPHVAGVAALVKSRYPSYTNNQIRQRINQTATY    342

P29600           251 LGSTNLYGSGLVNAEAATR    269
                     |||.:|||:|||:|..||:
P41363           343 LGSPSLYGNGLVHAGRATQ    361
```

5. Najlepsze przyrównania rozumiane jest jako przyrównanie, które w najlepszy sposób tłumaczy zmiany jakie zaszły w obu sekwencjach w toku ich ewolucji. Zatem przy wykonywaniu przyrównania zakłada się, że obie sekwencje wywodzą się od sekwencji wspólnego przodka. Trudno jest więc odpowiedzieć na pytanie, które z przyrównań jest lepsze, ponieważ ścieżka ewolucyjna obu sekwencji nie jest znana.

   Obie sekwencje są jednak różnej długości. Pod tym względem, bardziej sensowne jest użycie algorytmu lokalnego przyrównania (algorytm *Smitha-Watermana*). Przyrównanie lokalne umożliwia analizę podobieństw i różnic we fragmentach dwóch sekwencji, które są w ogóle porównywalne ze sobą. Z kolei, używając globalnego przyrównania można łatwo zaobserwować, że obie sekwencje są bardzo podobne do siebie, z wyjątkiem brakującego fragmentu z N-końca pierwszej sekwencji *Savinase* (`P29600`) długości ok. 90 reszt aminokwasowych. W tym przypadku wykonanie przyrównania globalne dostarczyło dodatkowej informacji na temat dwóch sekwencji.

   W przypadku gdy obie sekwencje są bardzo podobne - tak jak sekwencje `P29600` i  `P41363` - nie ma dużej różnicy pomiędzy lokalnym a globalnym przyrównaniem.

6. Otwórz stronę [serwisu UniProt](https://www.uniprot.org). Odszukaj dwa rekordy w oparciu o ich numery dostępu: [P29600](https://www.uniprot.org/uniprot/P29600) i [P41363](https://www.uniprot.org/uniprot/P41363). Lista publikacji w rekordach UniProt wskazuje, że sekwencję białka *Salvinase* (`P29600`) otrzymano ze struktury przestrzennej, natomiast sekwencję `P41363` otrzymano w wyniku translacji sekwencji DNA.

7. Panel `Subcellular location` w rekordzie UniProt wskazuje, że oba białka są wydzielane poza komórkę (`Secreted protein`).

8. Z informacji zawartych w panelu `PTM/Processing` wynika, że *Salivase* (`P29600`) jest sekwencją dojrzałego białka (pozbawioną sygnałów peptydowych), natomiast sekwencja `P41363` zawiera peptyd sygnałowy (w pozycji 1-24) oraz propeptyd (w pozycji 25-93). Oba peptydy sygnałowe są usuwane z dojrzałego białka. Różnica między dwoma białkami termostabilnej proteazy (`P29600` i `P41363`) polega na tym, że sekwencja `P41363` jest wynikiem tłumaczenie DNA i zawiera pełną informację o sekwencji kodującej, natomiast `P29600` powstała ze struktury przestrzennej, która dotyczy tylko dojrzałego białka.

9. Białko `P41363` prawdopodobnie mogłoby posłużyć jako składnik proszku do prania. Białko to, podobnie jak *Salvinase* jest proteazą serynową z rodziny S8. Jest ono również termostabilne. Sekwencje obu białek są również bardzo podobne (w ok. 80%). Potencjalnym problemem mogłoby być optymalne pH, lecz to mogłoby zostać zoptymalizowane w laboratorium.


### Zad. 5 - Przyrównanie daleko spokrewnionych sekwencji (wątpliwe przyrównania)

#### Przyrównanie semi-globalne (*Needle*):

```
# Length: 1289
# Identity:      73/1289 ( 5.7%)
# Similarity:   131/1289 (10.2%)
# Gaps:        1060/1289 (82.2%)
# Score: 158.5
```

#### Przyrównanie globalne (*Needle*, `END GAP PENALTY = true`)

```
# Length: 1255
# Identity:     110/1255 ( 8.8%)
# Similarity:   154/1255 (12.3%)
# Gaps:         992/1255 (79.0%)
# Score: -244.0
```

Włączona opcja `END GAP PENALTY` powoduje, że program *Needle* ujemnie punktuje również kary za przerwy na obu końcach przyrównania. Ponieważ sekwencja peptydazy człowieka jest 4 razy dłuższa od sekwencji peptydazy *Savinase*, przyrównanie globalne zawiera więcej przerw (`79%`) niż aminokwasów (`21%`). W wyniku, wartość punktacji przyrównania (`score`) jest ujemna i wynosi `-244.0`. 
> Domyślnie, w programie *Needle* opcja `END GAP PENALTY` jest wyłączona, a kary za przerwy na końcu przyrównania są ignorowane (jest to algorytm semi-globalny). Algorytm ten stanowi kompromis między globalnym i lokalnym przyrównaniem i często określany jest jako *algorytm "glokalny"*.

#### Przyrównanie lokalne (*Water*)

```
# Length: 296
# Identity:      71/296 (24.0%)
# Similarity:   129/296 (43.6%)
# Gaps:          73/296 (24.7%)
# Score: 173.0
#=======================================

P29600            23 GSGVKVAVLDTGISTHPDLNIRGGASFVPGEPSTQDGNGHGTHVAGTIAA     72
                     ||.....:|:..::.:.|.|:   .|.|      ..|..|||||| :|||
P29144           234 GSFGTAEMLNYSVNIYDDGNL---LSIV------TSGGAHGTHVA-SIAA    273

P29600            73 LNNSIGVL-------GVAPSAELYAVKV------LGASGSGSVSSIAQGL    109
                          |..       ||||.|::.::|:      ...:|:|.:.::.:.:
P29144           274 -----GHFPEEPERNGVAPGAQILSIKIGDTRLSTMETGTGLIRAMIEVI    318

P29600           110 EWAGNNGMHVANLSLGSPS---PSATLEQAVNSAT-SRGVLVVAASGNSG    155
                         |:...:.|.|.|..:   .|..:.:.:|.|. ...::.|:::||:|
P29144           319 ----NHKCDLVNYSYGEATHWPNSGRICEVINEAVWKHNIIYVSSAGNNG    364

P29600           156 --AGSISYP-ARYANAMAVGATDQNN--------------NRASFSQYGA    188
                       ..::..| ...::.:.|||....:              |:.::|..|.
P29144           365 PCLSTVGCPGGTTSSVIGVGAYVSPDMMVAEYSLREKLPANQYTWSSRGP    414

P29600           189 GLDIVAPGVNVQSTYPGSTYAS-----------LNGTSMATPHVAGAAAL    227
                     ..| .|.||::.:  ||...||           :|||||::|:..|..||
P29144           415 SAD-GALGVSISA--PGGAIASVPNWTLRGTQLMNGTSMSSPNACGGIAL    461

P29600           228 V----KQKNPSWSNVQIRNHLKNTATSLGSTNLY--GSGLVNAEAA    267
                     :    |..|..::...:|..|:|||....:..::  |.|::..:.|
P29144           462 ILSGLKANNIDYTVHSVRRALENTAVKADNIEVFAQGHGIIQVDKA    507
```
 
1. Przyrównanie lokalne i semi-globalne wskazują, że sekwencja prokariotycznej proteazy wykazuje podobieństwo jedynie do fragmentu sekwencji białkowej człowieka. Nie jest to natomiast widoczne opierając się na wynikach przyrównania globalnego, w którym wiele krótkich fragmentów sekwencji prokariotycznej rozciąga się wzdłuż całej sekwencji człowieka. 
   

   W przypadku porównywania sekwencji odlegle spokrewnionych zaleca się używanie algorytmu lokalnego. Wskazuje on regiony między sekwencjami, które są ze sobą porównywalne.


2. Nie, w oparciu o otrzymane przyrównania nie można odpowiedzieć na pytanie, czy sekwencja prokariotyczna *Salvinase* jest spokrewnione z sekwencją peptydazy człowieka. Kiedy wykonujemy przyrównanie dwóch lub większej liczby sekwencji zakładamy, że mają one wspólne pochodzenie (tj. wywodzą się od sekwencji obecnej u wspólnego przodka). 
   
   W przypadku analizowanych w tym zadaniu sekwencji peptydaz *B. subtilis* i człowieka NIE mamy pewności, czy te sekwencje są ze sobą w ogóle spokrewnione. Bardzo często zdarza się, że niespokrewnione ze sobą sekwencje uzyskują pewne przyrównania. Wartość punktacji (`score`) takich przyrównań będzie niska. Wartość punktacji lokalnego przyrównania `P29600` i `P29144` wynosi `174`. Aby móc interpretować tę wartość należy poznać zakres wartości punktacji, którzy można oczekiwać przy przyrównywaniu niespokrewnionych sekwencji.

   Aby odpowiedzieć na to pytanie, można dokonać losowego ułożenia aminokwasów w jednej sekwencji. Wówczas jakakolwiek informacja o ewolucyjnym pokrewieństwie tej sekwencji zostałaby utracona, a taka sekwencja nie będzie spokrewniona z żadną inna sekwencją białkową (ale będzie miała taką samą długość i zawartość aminokwasów).

#### Istotność przyrównania

3. Zakres wyników przyrównania sekwencji `P29600` z losowo wygenerowaną sekwencją `P29144` będzie się różnił, ale najprawdopodobniej będzie on mieścił się w poniższym zakresie:

   ```
   # Length: 100-300 
   # Identity: 20% -30%  
   # Similarity: 30% -40%  
   # Gaps #: 25% -40%  
   # Score: 40-70 
   ```

   Zatem takich właśnie wartości można spodziewać się podczas porównywania dwóch niespokrewnionych sekwencji o określonej długości i zawartości aminokwasów. 
   > Wykonywanie wielu przyrównań *Savinase* (`P29600`) z losową sekwencją człowieka dostarcza "modelu null", który następnie można porównać z prawdziwym przyrównaniem *Savinase*-peptydaza człowieka (`P29600-P29144`). Gdyby wykonać procedurę randomizacji sekwencji człowieka 100 razy, zamiast 3, można by wyznaczyć przedział ufności dla uzyskanej wartości punktacji oraz jej istotność statystyczną (więcej na temat istotności statystycznej podczas omawiania programu BLAST).

4. Porównując przyrównanie rzeczywistych sekwencji *Savinase / Human peptidase alignment* (score: `173`) z "celowo kiepskim" przyrównaniem *Savinase / losowa sekwencja*, oryginalne przyrównanie nie wydaje się już tak "kiepskie". Wartośc punktacji jest przynajmniej dwukrotnie wyższa od tych, które uzyskano w przyrównaniu zawierającym losową sekwencję. Warto zwrócić uwagę, że przy interpretacji wyników należy porównywać wartość punktacji aby zaobserwować wyraźną różnicę; inne wartości (identyczność, podobieństwo) mogą być podobne między oryginalnym przyrównaniem a przyrównaniem z losową sekwencją.
<br/><br/>

## Wpływ parametrów na przyrównanie sekwencji

### Zad. 6 - Kara za stosowanie przerw

#### 1. Zmniejszenie kary za przewy
Ponieważ kara za przerwę jest mała (niewielkie wartości ujemne), algorytm częściej wprowadza przerwy do przyrównania, ponieważ nie mają one tak dużego wpływu na końcową wartość punktacji przyrównania. Większy wpływ na obniżenie punktacji przyrównania mają substytucje aminokwasów. W rezultacie, otrzymane przyrównanie zawiera więcej przerw niż niedopasowań dwóch aminokwasów. Z biologicznego punktu widzenia, takie przyrównanie jest mało wiarygodne.

```
# Gap_penalty: 1.0
# Extend_penalty: 0.2
#
# Length: 1252
# Identity:     192/1252 (15.3%)
# Similarity:   228/1252 (18.2%)
# Gaps:        1006/1252 (80.4%)
# Score: 727.4
# 
#
#=======================================

P29600             1 A-QSVPW---GISRVQAP-----AA--------HN-RG-----L-T----     22
                     | :. |:   |:  :  |     ||        :: ||     | |    
P29144             5 ATEE-PFPFHGL--L--PKKETGAASFLCRYPEYDGRGVLIAVLDTGVDP     49

P29600            23 GS-G--V------KVA-VLDT---G-IST----HP-D----------L--     41
                     |: |  |      |:. ::||   | ::|    .| |          |  
P29144            50 GAPGMQVTTDGKPKIVDIIDTTGSGDVNTATEVEPKDGEIVGLSGRVLKI     99

P29600            42 -----N--------IR-G--------------------------------     45
                          |        |: |                                
P29144           100 PASWTNPSGKYHIGIKNGYDFYPKALKERIQKERKEKIWDPVHRVALAEA    149

P29600            46 ------------G---A----------------SF------VPGEP----     54
                                 |   |                ||       || |    
P29144           150 CRKQEEFDVANNGSSQANKLIKEELQSQVELLNSFEKKYSD-PG-PVYDC    197

P29600            55 -----------------------ST--------Q----------------     57
                                            ||        |                
P29144           198 LVWHDGEVWRACIDSNEDGDLSKSTVLRNYKEAQEYGSFGTAEMLNYSVN    247

P29600            58 ---DGN--------G-HGTHVAGTIAA--L-----NNSIGVLGVAPSAE-     87
                        |||        | |||||| :|||  .     .|     ||||.|: 
P29144           248 IYDDGNLLSIVTSGGAHGTHVA-SIAAGHFPEEPERN-----GVAPGAQI    291

P29600            88 LYAVKVLG-A--S----GSG---------S-----VS-SI--A-----QG    108
                     | ::|: | .  |    |:|         :     |: |.  |     .|
P29144           292 L-SIKI-GDTRLSTMETGTGLIRAMIEVINHKCDLVNYSYGEATHWPNSG    339

P29600           109 -----L-E--W---------AGNNG-------------------------    116
                          : |  |         |||||                         
P29144           340 RICEVINEAVWKHNIIYVSSAGNNGPCLSTVGCPGGTTSSVIGVGAYVSP    389

P29600           117 --MHVA----------N--------------L--SL----G---S-P---    127
                       | ||          |              |  |:    |   | |   
P29144           390 DMM-VAEYSLREKLPANQYTWSSRGPSADGALGVSISAPGGAIASVPNWT    438

P29600           128 -------------SP----------S---A-----T-------LE-----    134
                                  ||          |   |     |       ||     
P29144           439 LRGTQLMNGTSMSSPNACGGIALILSGLKANNIDYTVHSVRRALENTAVK    488

P29600           135 --------------Q---A----V-N-S-A-------T---SRGV-L---    146
                                   |   |    | | | |       |   :||: |   
P29144           489 ADNIEVFAQGHGIIQVDKAYDYLVQNTSFANKLGFTVTVGNNRGIYLRDP    538

P29600           147 V-VAA-S----G----------NS---G-----A----GS-I---SY---    161
                     | ||| |    |          ||   .     |    .| :   |:   
P29144           539 VQVAAPSDHGVGIEPVFPENTENSEKISLQLHLALTSNSSWVQCPSHLEL    588

P29600           162 ------------PAR-------------Y--A--NA--M------AV-GA    173
                                 | |             |  |  ||  :      || .|
P29144           589 MNQCRHINIRVDP-RGLREGLHYTEVCGYDIASPNAGPLFRVPITAVIAA    637

P29600           174 ------------TD------Q-NNNR-----------A-----------S    182
                                 ||      | .  |           |           |
P29144           638 KVNESSHYDLAFTDVHFKPGQIR--RHFIEVPEGATWAEVTVCSCSSEVS    685

P29600           183 --F--------------S-Q-Y--------G----A-----G--------    189
                       |              | : |        |    |     |        
P29144           686 AKFVLHAVQLVKQRAYRSHEFYKFCSLPEKGTLTEAFPVLGGKAIEFCIA    735

P29600           190 -----L-----D-------IV--AP--------GVN---VQST--Y----    203
                          |     |       ||  ||        |:|   |||:  |    
P29144           736 RWWASLSDVNIDYTISFHGIVCTAPQLNIHASEGINRFDVQSSLKYEDLA    785

P29600           204 --------------------P-GS---------------TYASLN-----    212
                                         | ||               ||   |     
P29144           786 PCITLKNWVQTLRPVSAKTKPLGSRDVLPNNRQLYEMVLTY---NFHQPK    832

P29600           213 -G--T----------------S------------M----A----------    217
                      |  |                |            |    |          
P29144           833 SGEVTPSCPLLCELLYESEFDSQLWIIFDQNKRQMGSGDAYPHQYSLKLE    882

P29600           218 ----T-------------------P----H---------V------A---    222
                         |                   |    |         :      |   
P29144           883 KGDYTIRLQIRHEQISDLERLKDLPFIVSHRLSNTLSLDIHENHSFALLG    932

P29600           223 -----------------------------GA------A------------    225
                                                  ||      |            
P29144           933 KKKSSNLTLPPKYNQPFFVTSLPDDKIPKGAGPGCYLAGSLTLSKTELGK    982

P29600           226 -A--------LV----KQKN-------PS--------------------W    235
                      |        |:    |.||       .|                    |
P29144           983 KADVIPVHYYLIPPPTKTKNGSKDKEKDSEKEKDLKEEFTEALRDLKIQW   1032

P29600           236 ------S-----------N-----V----QI--------R--------N-    242
                           |           |     |    |:        |        | 
P29144          1033 MTKLDSSDIYNELKETYPNYLPLYVARLHQLDAEKERMKRLNEIVDAANA   1082

P29600           243 ---H-----L-----------------KN-------T------------A    248
                        |     |                 ||       |            |
P29144          1083 VISHIDQTALAVYIAMKTDPRPDAATIKNDMDKQKSTLVDALCRKGCALA   1132

P29600           249 -----T-------SL--------G-----S-----------T----N---    255
                          |       |.        |     |           |    |   
P29144          1133 DHLLHTQAQDGAISTDAEGKEEEGESPLDSLAETFWETTKWTDLFDNKVL   1182

P29600           256 -------L----YGSG------LV----------NA-E----------AA    267
                            |    ||.|      ||          |. :          |:
P29144          1183 TFAYKHALVNKMYGRGLKFATKLVEEKPTKENWKNCIQLMKLLGWTHCAS   1232

P29600           268 -T    268
                      |
P29144          1233 FT   1234
```

W wyniku zmniejszenia kary za wprowadzenie przerw (otwarcie przerwy = `1` i wydłużenie przerwy = `0.2`) otrzymane przyrównanie składa się w 80% z samych przerw.

#### 2. Zwiększenie kary za przerwę
Ponieważ kara za przerwę jest duża (duże wartości ujemne), algorytm rzadko wprowadza przerwy do przyrównania, ponieważ zaniżają one końcową wartość punktacji przyrównania. Algorytm częściej wprowadza do przyrównania substytucje aminokwasów. W rezultacie, otrzymane przyrównanie zawiera niewielką liczbę przerw.

```
# Gap_penalty: 20.0
# Extend_penalty: 1.0
#
# Length: 54
# Identity:      17/54 (31.5%)
# Similarity:    29/54 (53.7%)
# Gaps:           4/54 ( 7.4%)
# Score: 69.0
# 
#
#=======================================

EMBOSS_001       211 LNGTSMATPHVAGAAALV----KQKNPSWSNVQIRNHLKNTATSLGSTNL    256
                     :|||||::|:..|..||:    |..|..::...:|..|:|||....:..:
TPP2_HUMAN       445 MNGTSMSSPNACGGIALILSGLKANNIDYTVHSVRRALENTAVKADNIEV    494

EMBOSS_001       257 YGSG    260
                     :..|
TPP2_HUMAN       495 FAQG    498


#---------------------------------------
#---------------------------------------
```

W wyniku zwiększenie kary za wprowadzenie przerw (otwarcie przerwy = `20`, wydłużenie przerwy = `1`) otrzymane przyrównanie jest krótkie (54 pozycji) i składa się w 7% z przerw.
<br/><br/>

### Zad. 7 - Macierze substytucji
Macierz substytucji (np. BLOSUM62) dostarcza informacji na temat wartości punktowania aminokwasów zgodnych i niezgodnych. Algorytmy służące do przyrównywania sekwencji (np. algorytm Smitha-Watermana) wykorzystują wartości w macierzach substytucji podczas wyznaczania przyrównania. Macierz substytucji ma zatem wpływ na wynik przyrównania (na wszystkie wartości przyrównania: punktacja, identyczność, podobieństwo, długość oraz liczba przerw).

#### BLOSUM30

```
# Matrix: EBLOSUM30
# Gap_penalty: 10.0
# Extend_penalty: 0.5
#
# Length: 326
# Identity:      76/326 (23.3%)
# Similarity:   149/326 (45.7%)
# Gaps:          88/326 (27.0%)
# Score: 342.5
# 
#
#=======================================

P29600             6 WGISRVQAPAAHNRGLT--------------GSGVKVAVLDTGISTHPDL     41
                     |   |:...:..:..|:              ||...:..|:..:....|.
P29144           206 W---RACIDSNEDGDLSKSTVLRNYKEAQEYGSFGTAEMLNYSVNIYDDG    252

P29600            42 NIRGGASFVPGEPSTQDGNGHGTHVAGTIAALNNSIGVL-------GVAP     84
                     |:...::         .|..|||||| :|||     |.:       ||||
P29144           253 NLLSIVT---------SGGAHGTHVA-SIAA-----GHFPEEPERNGVAP    287

P29600            85 SAELYAVKV------LGASGSGSVSSIAQGLEWAGNNGMHVANLSLGSPS    128
                     .|:::::|:      ...:|:|.:.::.:    :.|....::|:|:|..:
P29144           288 GAQILSIKIGDTRLSTMETGTGLIRAMIE----VINHKCDLVNYSYGEAT    333

P29600           129 --P-SATLEQAVNSAT-SRGVLVVAASGNSG--AGSISYPAR-YANAMAV    171
                       | |..:::::|.|: ...:::|:::||.|  ..::..|.. .:.::.|
P29144           334 HWPNSGRICEVINEAVWKHNIIYVSSAGNNGPCLSTVGCPGGTTSSVIGV    383

P29600           172 GA-TDQNNNRASFS--------QY----------GA-GLDIVAPGVNVQS    201
                     || :..:...|.:|        ||          || |:.|.|||..::|
P29144           384 GAYVSPDMMVAEYSLREKLPANQYTWSSRGPSADGALGVSISAPGGAIAS    433

P29600           202 ----TYPGSTYASLNGTSMATPHVAGAAALV----KQKNPSWSNVQIRNH    243
                         |:.|:.:  :|||||::|.:.|..||:    |:.|..::...:|..
P29144           434 VPNWTLRGTQL--MNGTSMSSPNACGGIALILSGLKANNIDYTVHSVRRA    481

P29600           244 LKNTATSLGSTNLY--GSGLVNAEAA    267
                     |:|||:......::  |.|::.::.|
P29144           482 LENTAVKADNIEVFAQGHGIIQVDKA    507
```

#### BLOSUM62

```
# Matrix: EBLOSUM62
# Gap_penalty: 10.0
# Extend_penalty: 0.5
#
# Length: 296
# Identity:      71/296 (24.0%)
# Similarity:   129/296 (43.6%)
# Gaps:          73/296 (24.7%)
# Score: 173.0
# 
#
#=======================================

P29600            23 GSGVKVAVLDTGISTHPDLNIRGGASFVPGEPSTQDGNGHGTHVAGTIAA     72
                     ||.....:|:..::.:.|.|:   .|.|      ..|..|||||| :|||
P29144           234 GSFGTAEMLNYSVNIYDDGNL---LSIV------TSGGAHGTHVA-SIAA    273

P29600            73 LNNSIGVL-------GVAPSAELYAVKV------LGASGSGSVSSIAQGL    109
                          |..       ||||.|::.::|:      ...:|:|.:.::.:.:
P29144           274 -----GHFPEEPERNGVAPGAQILSIKIGDTRLSTMETGTGLIRAMIEVI    318

P29600           110 EWAGNNGMHVANLSLGSPS---PSATLEQAVNSAT-SRGVLVVAASGNSG    155
                         |:...:.|.|.|..:   .|..:.:.:|.|. ...::.|:::||:|
P29144           319 ----NHKCDLVNYSYGEATHWPNSGRICEVINEAVWKHNIIYVSSAGNNG    364

P29600           156 --AGSISYP-ARYANAMAVGATDQNN--------------NRASFSQYGA    188
                       ..::..| ...::.:.|||....:              |:.::|..|.
P29144           365 PCLSTVGCPGGTTSSVIGVGAYVSPDMMVAEYSLREKLPANQYTWSSRGP    414

P29600           189 GLDIVAPGVNVQSTYPGSTYAS-----------LNGTSMATPHVAGAAAL    227
                     ..| .|.||::.:  ||...||           :|||||::|:..|..||
P29144           415 SAD-GALGVSISA--PGGAIASVPNWTLRGTQLMNGTSMSSPNACGGIAL    461

P29600           228 V----KQKNPSWSNVQIRNHLKNTATSLGSTNLY--GSGLVNAEAA    267
                     :    |..|..::...:|..|:|||....:..::  |.|::..:.|
P29144           462 ILSGLKANNIDYTVHSVRRALENTAVKADNIEVFAQGHGIIQVDKA    507
```

#### BLOSUM90

```
# Matrix: EBLOSUM90
# Gap_penalty: 10.0
# Extend_penalty: 0.5
#
# Length: 279
# Identity:      73/279 (26.2%)
# Similarity:   107/279 (38.4%)
# Gaps:          91/279 (32.6%)
# Score: 147.5
# 
#
#=======================================

P29600            58 DGN---------GHGTHVAGTIAA--------LNNSIGVLGVAPSAELYA     90
                     |||         .|||||| :|||        .|      ||||.|::.:
P29144           251 DGNLLSIVTSGGAHGTHVA-SIAAGHFPEEPERN------GVAPGAQILS    293

P29600            91 VKVLGASGSGSVSSIAQGLEWAG---------NNGMHVANLSLGSPS--P    129
                     :|:    |....|::..|   .|         |......|.|.|..:  |
P29144           294 IKI----GDTRLSTMETG---TGLIRAMIEVINHKCDLVNYSYGEATHWP    336

P29600           130 -SATLEQAVNSAT-SRGVLVVAASGNSG---------AGSISYPARYANA    168
                      |..:.:.:|.|. ...::.|:::||.|         .|:.|      ..
P29144           337 NSGRICEVINEAVWKHNIIYVSSAGNNGPCLSTVGCPGGTTS------SV    380

P29600           169 MAVGA-TDQNNNRASFS--------QY----------GA-GLDIVAPGVN    198
                     :.||| ...:...|.:|        ||          || |..|.|||..
P29144           381 IGVGAYVSPDMMVAEYSLREKLPANQYTWSSRGPSADGALGVSISAPGGA    430

P29600           199 VQS----TYPGSTYASLNGTSMATPHVAGAAALV----KQKNPSWSNVQI    240
                     :.|    |..|:..  :|||||::|...|..||:    |..|..::...:
P29144           431 IASVPNWTLRGTQL--MNGTSMSSPNACGGIALILSGLKANNIDYTVHSV    478

P29600           241 RNHLKNTATSLGSTNLY--GSGLVNAEAA    267
                     |..|.|||........:  |.|::..:.|
P29144           479 RRALENTAVKADNIEVFAQGHGIIQVDKA    507
```

Wraz ze wzrastającym indeksem BLOSUM (od 30 do 90), procent identyczności przyrównania wzrasta, natomiast maleje długość przyrównania.
<br/><br/>

## Porównanie sekwencji: wykres Dot plot

### Zad. 8

#### s1:s1
Ciągła linia przekątna wskazuje na dopasowanie sekwencji na całej długości. Porównywane sekwencje są zatem identyczne lub bardzo podobne (poziom zgodności to przynajmniej 10 na 15 nukleotydów)

<img src="./images/dotmatcher_s1-s1.png" alt="dotmatcher_s1-s1.png" width="450px">

#### s1:s10
Linia przekątna jest przerwana w trzech miejscach - są to regiony w sekwencjach, w których nie ma zgodności.

<img src="./images/dotmatcher_s1-s10.png" alt="dotmatcher_s1-s10.png" width="450px">

#### s2:s2
Ciągła linia przekątna wskazuje na dopasowanie sekwencji na całej długości. Dodatkowo, w sekwencjach występuje region (długości ok. 50 nukleotydów) dwukrotnie powtórzony w sekwencji w pozycji ok. 70, i 200 nukleotydu.

<img src="./images/dotmatcher_s2-s2.png" alt="dotmatcher_s2-s2.png" width="450px">

#### s4:s5
Brak linii przekątnej wskazuje na brak podobieństwa sekwencji na całej długości. W obu sekwencjach występują wielokrotne powtórzenia krótkich fragmentów sekwencji (ok. 20-25 nukleotydów). Tego typu wielokrotne powtórzenia występujące blisko siebie w sekwencji nazywają się **powtórzeniami tandemowymi** (np. czterokrotne powtórzenie podsekwencji `AT` w sekwencji `ATATATAT`). Liczba linii na wykresie dot-plot odpowiada liczbie powtórzonych fragmentów. Długość linii oznacza długość fragmentu podlegającego powtórzeniu. Odległość między liniami na wykresie oznacza odległości między tymi powtórzeniami w sekwencji.

<img src="./images/dotmatcher_s4-s5.png" alt="dotmatcher_s4-s5.png" width="450px">


#### s7:s8
Przemieszczenie się linii przekątnej oznacza zajście insercji w jednej sekwencji lub delecji w drugiej sekwencji. W tym przypadku, sekwencja `s7` jest dłuższa i zawiera fragment w pozycji `200-220`, który nie występuje w sekwencji `s8`. Zatem, fragment uległ insercji w sekwencji `s7` lub delecji w sekwencji `s8`.

<img src="./images/dotmatcher_s7-s8.png" alt="dotmatcher_s7-s8.png" width="450px">

#### s4:s4
Sekwencja `s4` na N-końcu (w pozycji 75-100) zawiera liczne powtórzenia tandemowe.

<img src="./images/dotmatcher_s4-s4.png" alt="dotmatcher_s4-s4.png" width="450px">
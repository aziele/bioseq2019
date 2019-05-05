## BLAST - blastx, tblastn

### Zad. 1 - Proste przeszukiwanie blastx
<img align="right" src="./images/jp-lostworld.png" alt="Jurassic Park - Lost World"> Mark Boguski, pracownik NCBI, zauważył, że sekwencja przedstawiona w książce *Jurassic Park* nie była zbyt dobrze dobrana. Dlatego zaproponował, aby w filmie *Jurassic Park – The Lost World* umieścić inną, bardziej odpowiednią sekwencję.

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
2. W której ramce odczytu została przetłumaczona sekwencja zapytania?
3. Podaj pozycję startu i końca przyrównania w sekwencji zapytania i sekwencji trafienia.
   * Dlaczego te długości nie odpowiadają sobie?
3. Spójrz na przyrównanie tych sekwencji. Jak brzmi ukryta wiadomość?
   * Podaj pozycję w sekwencji zapytania pierwszego wyrazu wiadomości. 
4. Co oznaczają fragmenty dopasowania oznaczone małymi szarymi literami?
<br/><br/>


### Zad. 2 - Złożone przeszukiwanie blastx
W bazie nukleotydowej [NCBI](https://www.ncbi.nlm.nih.gov) wyszukaj rekord sekwencji *EST* węża koralowego o numerze dostępu `FL590802`. W panelu `Analyze this sequence` po prawej stronie rekordu naciśnij `Run BLAST`. Wybierz program `blastx`, bazę sekwencji `UniProtKB/Swiss-Prot(swissprot)` i rozpocznij przeszukiwanie.

1. Czy sekwencja zapytania została dopasowana na całej długości do sekwencji białek?
2. Jakiego typu sekwencje białkowe zostały przyrównane do sekwencji zapytania?

#### Najwyżej punktowane przyrównanie

Z listy otrzymanych trafień zidentyfikuj sekwencję, która uzyskała najwyższą wartość punktacji (`Max score`). Odpowiedz na poniższe pytania dotyczące tej sekwencji:

3. W której ramce odczytu została przetłumaczona sekwencja zapytania?
4. Podaj długość pełnej sekwencji zapytania oraz jej początek i koniec w przyrównaniu.
5. Podaj długość pełnej sekwencji trafienia oraz jej początek i koniec w przyrównaniu.
6. Dlaczego aminokwasowa sekwencja trafienia nie została przyrównana przez program blastx w pozycji `1-18`?
7. Czy liczba reszt cysteiny w sekwencji zapytania odpowiada liczbie cystein w sekwencji trafienia?
<br/><br/>


### Zad. 3 - Proste przeszukiwanie tblastn
Czynnik transkrypcyjny LIM z rodziny homeobox (*LIM homeobox transcription factor 1-beta*) jest białkiem zaangażowanym w rozwój kończyn u zwierząt, w tym u człowieka. Celem zadania jest wyszukanie sekwencji u gąbek, wykazujących podobieństwo do białka LIM człowieka o numerze dostępu `NP_001167617`.

Otwórz stronę serwisu [NCBI BLAST](https://blast.ncbi.nlm.nih.gov/Blast.cgi). Wybierz program **tblastn** i w jego formularzu:
* Ustaw bazę danych `Expressed sequence tags (est)`
* Ustaw organizm: `Porifera`.
* Rozpocznij przeszukiwanie.

1. Podaj nazwę organizmu, z którego pochodzi najwięcej sekwencji trafienia.

#### Najwyżej punktowane przyrównanie

Z listy otrzymanych trafień zidentyfikuj sekwencję, która uzyskała najwyższą wartość punktacji (`Max score`). Odpowiedz na poniższe pytania dotyczące tej sekwencji:

2. W której ramce odczytu została przetłumaczona sekwencja trafienia?
3. Podaj długość pełnej sekwencji zapytania oraz jej początek i koniec w przyrównaniu.
4. Podaj długość pełnej sekwencji trafienia oraz jej początek i koniec w przyrównaniu.
<br/><br/>

### Zad. 4 - Wyznaczanie lokalizacji egzonów (blastn)
Transkrypt genu GABRG2 człowieka (`NM_198904`) składa się z 10 egzonów długości od 24 do ponad 2400 nukleotydów. W serwisie [NCBI BLAST](https://blast.ncbi.nlm.nih.gov/Blast.cgi), wybierz programu **blastn** i przeszukaj genomowe sekwencje człowieka (`RefSeq Genomic Sequences`) w celu zlokalizowania pozycji egzonów genu *GABRG2* w genomie człowieka.

Z listy otrzymanych trafień zidentyfikuj sekwencję, która uzyskała najwyższą wartość punktacji (`Max score`). Odpowiedz na poniższe pytania:

1. Na którym chromosomie człowieka znajduje się gen *GABRG2*?
2. Czy sekwencja transkryptu *GABRG2* została przyrównana przez program *blastn* na całej swojej długości do sekwencji tego genomowej genu *GABRG2*?
3. Ile przyrównań wyznaczył program *blastn* między sekwencją mRNA a sekwencją genomową genu *GABRG2*?
4. Czy wszystkie przyrównania są w tej samej orientacji nici DNA (np. `plus/plus`)?
5. Czy kolejność zidentyfikowanych przyrównań odpowiada kolejności ułożenia egzonów w genie *GABRG2*?
6. Poniżej znajdują się prawidłowe pozycje 10 egzonów genu GABRG2 na podstawie rekordu mRNA ([NM_198904](https://www.ncbi.nlm.nih.gov/nuccore/NM_198904)).

    ```
       1   465
     466   617
     618   685
     686   906
     907   989
     990   1127
    1128   1280
    1281   1486
    1487   1510
    1511   3957
    ```
    
    Które z powyższych lokalizacji zostały prawidłowe zidentyfikowane przez program *blastn*?
7. Dlaczego niektóre przyrównania nie mają 100% identyczności, skoro porównywane sekwencje są identyczne? 

   Na przykład, w przyrównaniu dotyczącym piątego egzonu występuje niezgodność jednego nukleotydu.

    ```
     Score = 155 bits (171),  Expect = 8e-34
     Identities = 87/88 (99%), Gaps = 0/88 (0%)
     Strand=Plus/Plus

    Query  902    CTAAGGTTGACAATTGATGCTGAGTGCCAATTACAATTGCACAACTTTCCAATGGATGAA  961
                  || |||||||||||||||||||||||||||||||||||||||||||||||||||||||||
    Sbjct  38589  CTTAGGTTGACAATTGATGCTGAGTGCCAATTACAATTGCACAACTTTCCAATGGATGAA  38648

    Query  962    CACTCCTGCCCCTTGGAGTTCTCCAGTT  989
                  ||||||||||||||||||||||||||||
    Sbjct  38649  CACTCCTGCCCCTTGGAGTTCTCCAGTT  38676
    ```

8. Dlaczego program *blastn* zidentyfikował dodatkowe przyrównanie, które nie jest egzonem i zawiera dużą liczbę niezgodnych nukleotydów?

    ```
     Score = 45.5 bits (49),  Expect = 1.0
     Identities = 32/37 (86%), Gaps = 0/37 (0%)
     Strand=Plus/Plus

    Query  2786   TAGCACCTTGCATAGTGCCTGGCATATAGTTGGTGCT  2822
                  ||||| || || |||||||||||| ||||| ||||||
    Sbjct  59042  TAGCAACTAGCTTAGTGCCTGGCACATAGTAGGTGCT  59078
    ```

#### NCBI Splign
Użyj serwisu [NCBI Splign](https://www.ncbi.nlm.nih.gov/sutils/splign/) w celu wyznaczenia pozycji egzonów transkryptu GABRG2 (`NM_198904`) w sekwencji genomowej tego genu (`NG_009290`).

9. Czy pozycje egzonów w transkrypcie GABRG2 zostały prawidłowo zidentyfikowane?
<br/><br/>

### Zad. 5 - Wyznaczanie lokalizacji ortologicznych egzonów kodujących (blastn i tblastn)

#### blastn
Użyj programu *blastn* stosując jako zapytanie numer dostępu sekwencji transkryptu GABRG2 (`NM_198904`) oraz bazę danych sekwencji genomowych (`RefSeq Genomic Sequences`) gibona *Nomascus leucogenys*  w celu lokalizacji egzonów GABRG2 w genomie gibona.

1. Na którym chromosomie gibona znajduje się gen GABRG2?
2. Czy sekwencja transkryptu GABRG2 została przyrównana przez program *blastn* na całej swojej długości do sekwencji genomowej gibona?
3. Ile przyrównań wyznaczył program *blastn* między sekwencją mRNA a sekwencją genomową genu GABRG2?
4. Czy wszystkie przyrównania są w tej samej orientacji nici DNA (np. `plus/plus`)?

#### tblastn
Użyj programu `tblastn` stosując jako zapytanie numer dostępu sekwencji białkowej GABRG2 człowieka (`NP_944494`) oraz bazę danych sekwencji genomowych (`RefSeq Genomic Sequences`) gibona *Nomascus leucogenys* w celu lokalizacji egzonów GABRG2 w genomie gibona.

Z listy otrzymanych trafień zidentyfikuj sekwencję, która uzyskała najwyższą wartość punktacji (`Max score`) w poprzednim przeszukiwaniu *blastn*.

5. Czy sekwencja białka GABRG2 człowieka została przyrównana przez program *tblastn* na całej swojej długości do sekwencji genomowej gibona?
6. Ile przyrównań wyznaczył program *tblastn* między sekwencją białka a sekwencją genomową genu GABRG2?
7. Zidentyfikowane przyrównania obejmują translację sekwencji genomowej w sześciu ramkach odczytu. Które ramki odczytu powinno brać się pod uwagę podczas wyznaczania pozycji egzonów.

8. Poniżej znajduja się sekwencja białkowa GABRG2 gibona rozmieszczona na 10 egzonach.

    ```
      1–36   MSSPNIWSTGSSVYSTPVFSQKMTVWILLLLSLYPG
     37–87   FTSQKSDDDYEDYASNKTWVLTPKVPEGDVTVILNNLLEGYDNKLRPDIGV
     88–109  KPTLIHTDMYVNSIGPVNAINM
    110–183  EYTIDIFFAQTWYDRRLKFNSTIKVLRLNSNMVGKIWIPDTFFRNSKKADAHWITTPNRMLRIWNDGRVLYTLR
    184–211  LTIDAECQLQLHNFPMDEHSCPLEFSSY
    212–257  GYPREEIVYQWKRSSVEVGDTRSWRLYQFSFVGLRNTTEVVKTTSG
    258–308  DYVVMSVYFDLSRRMGYFTIQTYIPCTLIVVLSWVSFWINKDAVPARTSLG
    309–376  ITTVLTMTTLSTIARKSLPKVSYVTAMDLFVSVCFIFVFSALVEYGTLHYFVSNRKPSKDKDKKKKNP
    377–384  LLRMFSFK
    385–475  APTIDIRPRSATIQMNNATHLQERDEEYGYECLDGKDCASFFCCFEDCRTGAWRHGRIHIRIAKMDSYARIFFPTAFCLFNLVYWVSYLYL
    ```

    Czy program *tblastn* zidentyfikował poprawnie niektóre powyższe fragmenty?
<br/><br/>

### Zad. 6 - Identyfikacja ortologów (*Reciprocal BLAST*)
> Celem zadania jest znalezienie sekwencji białkowej rekina, ortologicznej do białka opsyny-5 człowieka (`NP_859528`).

Opsyny są światłoczułymi białkami występującymi u zwierząt i pełnią kluczowe funkcje w procesie widzenia. Białka te absorbują światła o różnej długości fali (np. czerwone, niebieskie, zielone); mutacje w genach kodujących opsyny wywołują ślepotę różnych kolorów. Rodzina białek opsynowych składa się z wielu białek o podobnych nazwach: u człowieka występuje pięć grup opsyn (1-5), rodopsyna i peropsyna. Nazwy tych białek niekoniecznie odpowiadają nazwom opsyn u innych gatunków. Dlatego identyfikacja ortologów tych genów u odgrywa kluczową rolę w ich klasyfikacji.

#### BLAST w jednym kierunku
W serwisie [NCBI BLAST](https://blast.ncbi.nlm.nih.gov/) przeszukaj wszystkie białkowe sekwencje rekina *Scyliorhinus canicula* stosując jako zapytanie numer dostępu opsyny-5 człowieka (`NP_859528`).

1. Czy zidentyfikowana sekwencja białkowa rekina jest opsyną-5?

#### BLAST w drugim kierunku
Przeprowadź wyszukiwania BLAST stosując jako zapytanie zidentyfikowaną sekwencję rekina i bazę danych sekwencji człowieka pochodzących z bazy *RefSeq*.

2. Czy zidentyfikowana sekwencja białkowa rekina jest opsyną-5?



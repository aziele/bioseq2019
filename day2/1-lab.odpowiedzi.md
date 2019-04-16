## Wyszukiwanie sekwencji podobnych (BLAST)

### Zad. 1
Celem zadania jest znalezienie sekwencji mRNA insuliny najbardziej podobnych do wejściowej sekwencji zapytania z koszatniczki pospolitej.

#### Odczytywanie wyników

##### *Octodon degus*

<img src="./images/insulin_blast1-table1.png" alt="insulin_blast1-table1.png">

1. Numer dostępu sekwencji w bazie danych wykazującej największej podobieństwo do sekwencji zapytania to `M57671.1`. Jest to ta sama sekwencja, która została użyta w zapytaniu.
2. Wartość punktacji `Max score` tego przyrównania wynosi `780`. Parametr `Max score` określa wartość punktacji najwyżej punktowanego lokalnego przyrównania między sekwencją zapytania a sekwencją z bazy danych. Jeżeli w obrębie przyrównania dwóch sekwencji BLAST zidentyfikowałby kilka lokalnych przyrównań, to `Max score` jest wartością o najwyższej punktacji.
3. Wartośc punktacji `Total score` tego przyrównania wynosi `780`. Parametr `Total score` jest sumą wartości punktacji wszystkich znalezionych lokalnych przeyrównań między dwiema sekwencjami. Ponieważ w obrębie sekwencji `M57671.1` porównanej do samej siebie, BLAST zidentyfikował jedno lokalne przyrównanie, parametr `Total score` ma taką samą wartość co parametr `Max score`.
4. Procent identyczności wynosi `100`.
5. Wartość `Query cover` wynosi `100%`. Parametr ten określa procentowy udział długości sekwencji zapytania w przyrównaniu. W tym przypadku, przyrównaniem objęta jest pełnej długości sekwencja zapytania.
6. Wartość `E-value` wynosi `0` (precyzyjniej, bardzo niska liczba zaokrąglona do zera). 
   > Parametr `E-value` określa liczbę przypadkowych sekwencji w przeszukiwanej bazie danych, które uzyskałby taką lub wyższą wartość punktacji z sekwencją zapytania.
7. W przyrównaniu nie ma przerw.
8. Długość przyrównania wynosi 432 nukleotydy.

##### *Homo sapiens*

<img src="./images/insulin-blast1-table2.png" alt="insulin-blast1-table2">

1. Numery dostępu sekwencji człowieka: `NM_001291897.1`, `JQ951950.1`, `NM_001185098.1`, `NM_001185097.1`, `NM_000207.2`, `BC005255.1`. Te sekwencje uzysały taką samą wartość punktacji (`Max score`), więc są równie dobre.
2. Wartość punktacji `Max score` to `205`.
3. Wartość punktacji `Total score` to `205`
4. Procent identyczności wynosi `74.49`.
5. Wartość `Query cover` wynosi `76%`.
6. Wartość `E-value` wynosi `1e-48`.
7. Przyrównanie zawiera `15` przerw, co stanowi 4% całego przyrównania.
8. Długość przyrównania wynosi `341` nukleotydów.

### Zad. 2
Wynik programu BLAST przy zastosowaniu sekwencji zapytania mRNA insuliny koszatniczki i ograniczeniu wyników do organizmu człowieka.

<img src="./images/insulin-blast2-table1.png" alt="insulin-blast2-table1.png">

1. Tak, w wynikach znajdują się sekwencje człowieka z poprzedniego zadania (np. `NM_001291897.1`).
2. Nie, zmianie uległa wartość E-value. W poprzednim przeszukaniu wartość E-value dla tych samych sekwencji wynosiła `1e-48`, teraz wynosi `5e-50`.
3. Wielkość bazy NR z poprzedniego zadania to `204,700,810,597` znaków, wielkość bazy NR z ograniczeniem do organizmy człowieka to `7,199,154,007` znaków.
4. Stosunek wielkości dwóch baz danych `204,700,810,597` / `7,199,154,007` = `28`.
5. Stosunek E-value w dwóch przeszukiwaniach wynosi `5e-50` / `1e-48` = `20`.
6. Wartość E-value jest wprost proporcjonalna do wielkości bazy. Wartość E-value wzrasta wraz ze wzrostem bazy danych.
   > Przyrównanie o punktacji = 205 bitów jest badziej znaczące podczas przesukiwania mniejszej bazy danych. W większej bazie danych jest większ szansa znalezienia przypadkowych przyrównań.


### Zad. 3
W programie BLAST istnieje ryzyko otrzymania wyników fałszywie pozytywnych (trafień do sekwencji zapytania, które nie są spokrewnione). W tym zadaniu zbadamy co stanie się kiedy jako sekwencje zapytania w programie BLAST podamy wygenerowane losowe sekwenje.

#### Sekwencje nukleotydowe
* Otwórz serwis internetowy [SeqGen](http://www.cbs.dtu.dk/biotools/SeqGen-1.0/) i ustaw:
    - `Sequence type`: `nucleotide`
    - `Sequence length`: `25`
    - `Number of sequences`: 3
* Umieść wygenerowane sekwencje jako zapytanie w nukleotydowym programie BLAST:
    ```
    >seq1
    GCTCGGGCCTGCCTCCTACCACGAC
    >seq2
    ACTTAAAAAGCGTAATACAGATAGA
    >seq3
    ATATCTGGAAGCGTGAACATTTATG
    ```
  W formularzu programu BLAST ustaw:
  - w panelu `Program Selection` wybierz program `Somewhat similar sequences (blastn)`
  - W panelu `Algorithm parameters` ustaw:
      - Odznacza opcję `Automatically adjust parameters for short input sequences`
      - `Expected threshold` = `50`
  <img src="./images/ncbi-blast-algorithm_parameters1.png" alt="ncbi-blast-algorithm_parameters1.png" width="400px">
* Uruchom program BLAST.

Wyniki programu BLAST dla trzech różnych przeszukiwań można przeglądać korzystając z rozwijanego menu .**Results for**.

<img src="./images/ncbi-browsing-results.png" alt="ncbi-browsing-results" width="400px">


1. Tak, wiele trafień wykazuje 90-100% identyczność do losowo wygenerowanych sekwencji zapytania. Na przykład:

```
>XM_004482443.3 PREDICTED: Dasypus novemcinctus Fanconi anemia complementation 
group F (FANCF), mRNA
Length=2393

 Score = 35.6 bits (38),  Expect = 12
 Identities = 22/24 (92%), Gaps = 0/24 (0%)
 Strand=Plus/Plus

Query  2    CTCGGGCCTGCCTCCTACCACGAC  25
            |||||||||||| |||||||| ||
Sbjct  771  CTCGGGCCTGCCGCCTACCACCAC  794
```

2. Długość przyrównań wynosi na ogół 17-22 nukleotydów.
3. Trafienia przyjmują wartości `Max Score` w zakresie `33-36` *half bitów*.
4. Trafienia przyjmują wartości `E-value` w zakresie `12-42`.
   > W tych przeszukiwaniach najwyższą dopuszczalną wartośćią `E-value` jest `50`. Domyślnie w programie BLAST, `E-value` ma wartość `10`.
5. Otrzymane wyniki nie mają absolutnie żadnego sensu biologicznego(!). Sekwencje znalezione w bazie danych są prawdziwymi sekwencjami występującymi w organizmach. Natomiast, sekwencje zapytania są całkowicie losowe i pozbawione jakiejkolwiek pokrewieństwa z sekwencjami znajdującymi się w bazie danych. Jedynym powodem, dla którego otrzymaliśmy trafienia, jest przypadkowe podobieństwo do znanych sekwencji w bazie danych.

   Ponieważ sekwencje zapytania są krótkie (zaledwie 25 nt) bardzo często mogą wystąpić przez przypadek. Parametr E-value określa ich istotność statyczną - trafienia uzyskały wartości tego parametru w zakresie 12-42, co oznacza, że w bazie danych znajduje się od 12 do 42 przypadkowych sekwencji, które uzyskałyby równie dobre przyrównanie.

#### Sekwencje aminokwasowe
* Otwórz serwis internetowy [SeqGen](http://www.cbs.dtu.dk/biotools/SeqGen-1.0/) i ustaw:
    - `Sequence type`: `peptide`
    - `Sequence length`: `25`
    - `Number of sequences`: 3
* Wygenerowane sekwencje białkowe:
    ```
    >seq1
    LGPIYMVYWWEGECRCQSFASAKTT
    >seq2
    CTENAMFTPMHRGYSSNSDTMTQKP
    >seq3
    GSDHFLKQGSWKANKEKLWDIDLPP
    ```
* Umieść wygenerowane sekwencje jako zapytanie w programie **protein BLAST**. W formularzu programu BLAST ustaw:
  - W panelu `Algorithm parameters` ustaw:
      - Odznacza opcję `Automatically adjust parameters for short input sequences`
      - `Expected threshold` = `1000`

6. Tak, występują trafienia. Na przykład:

```
>WP_133225980.1 type I-C CRISPR-associated protein Cas7/Csd2 [Paenibacillus sp. 
MS74]

 Score = 30.4 bits (67),  Expect = 39, Method: Composition-based stats.
 Identities = 9/20 (45%), Positives = 14/20 (70%), Gaps = 0/20 (0%)

Query  4    IYMVYWWEGECRCQSFASAK  23
            ++ VYWWE  C+   ++SAK
Sbjct  229  VHTVYWWEHNCKLGQYSSAK  248
```

6. Uzyskano wyniki:
   * Długość przyrównań wynosi na ogół 15-22. W przyrównaniach jest niewiele przerw, najczęściej kilkanaście substytucji.
   * Trafienia przyjmują wartości `Max Score` w zakresie `33-36` *half bitów*.
   * Trafienia przyjmują wartości `E-value` w zakresie `40-1000`.
7. Większym ryzykiem uzyskania sekwencji fałszywie pozytywnych obarczone są sekwencje DNA. W przeszukiwaniu bazy nukleotydowej wystarczyło ustawić maksymalnie dopuszczane E-value 50, natomiast podczas przeszukiwania sekwencji aminokwasowych zastosowano E-value <= 1000.

### Zad. 4
1. Sekwencja użyta w książce *Jurassic Park* nie pochodzi z dinozaura. Sekwencja najprawdopodobniej pochodzi z sekwencji wektora `Cloning vector pAgaL6, complete sequence` o numerze dostępu [MH621333](https://www.ncbi.nlm.nih.gov/nuccore/MH621333.1).
2. Przyrównanie programem BLAST sekwencji zapytania i sekwencji wektora składa się z czterech lokalnych przyrównań (**HSP**, *High Scoring Pairs*).
3. Wartośc parametru `Max Score` = `435`, a `Total Score` = `1431`.
4. Najwyżej punktowane przyrównanie lokalne między sekwencją zapytania a wektorem jest w pozycji `302-661` w sekwencji zapytania i w pozycji `6179-5770` sekwencji wektora. W sekwencji wektora, pozycja startu jest większa od pozycji końca przyrównania, ponieważ odnosi się do sekwencji komplementarnej. W tym przyrównaniu sekwencja zapytania jest na nici `plus`, natomiast sekwencja wektora na nici `minus`.
5. Michaela Crichtona z sekwencji wektora wyciął cztery fragmenty. Z każdego fragmentu wyciął kilka krótszych fragmentów. Połączył cztery fragmenty ze sobą.


### Zad. 5
Otwórz serwis [BLAST](https://blast.ncbi.nlm.nih.gov/Blast.cgi). Wybierz program **blastx**. Umieść sekwencję zapytania, użyj domyślnych ustawień programu. Uruchom program BLAST.

> Program blastx przyjmuje jako zapytanie sekwencję DNA i przeszukuje bazę sekwencji białek. Przed przeprowadzeniem porównań blastx dokonuje translacji sekwencji w sześciu ramkach odczytu (trzy ramki odczytu na nici plus i trzy ramki odczytu na nici minus).

1. Sekwencja z bazy danych, która wykazuje największe podobieństwo do sekwencji zapytania jest czynnikiem transkrypcyjnym kurczaka (*Gallus gallus*) o numerze dostępu [NP_990795.1](https://www.ncbi.nlm.nih.gov/protein/NP_990795.1).
2. Przyrównanie sekwencji Marka i sekwencji `NP_990795.1`.

<img src="./images/ncbi-blast-mark.png" alt="ncbi-blast-mark">

Ukryta wiadomość to `MARK WAS HERE`. Mark użył sekwencji kodującej czynnik transkrypcyjny. Umieścił w niej odpowiednie kodony tak, aby po przetłumaczeniu sekwencji DNA na białko powstała wiadomość.

3. Fragmenty przyrównania oznaczone małymi szarymi literami oznaczają regiony sekwencji o niskiej złożoności (*low complexity*) aminokwasowej. Są to regiony bogate w powtórzenia kilka aminokwasów (np. `pppppppaaapp`). Regiony te nie są brane pod uwagę podczas wyznaczania przyrównania przez program BLAST (są "maskowane"), ponieważ mogłyby one fałszywie zawyżyć wartość punktacji `score`.
> Program BLAST domyślnie maskuje te regiony, ale możliwe jest wyłączenie opcji maskowania w formularzu prorgamu BLAST (w panelu `Algorithm parameters`, w części `Filters and Masking`, zaznaczyć/odznaczyć `Filter low complexity regions`).

### Zad. 6
W bazie białkowej NCBI skorzystaj z zaawansowanego wyszukiwania i utwórz zapytanie do bazy danych:

```
FOXP2[Gene Name] AND Homo sapiens[Organism] 
```

Wybierz rekord *forkhead box protein P2 isoform I [Homo sapiens]* o numerze dostępu [NP_055306](https://www.ncbi.nlm.nih.gov/protein/NP_055306.1). W panelu `Analyze this sequence` po prawej stronie w rekordzie sekwencji, naciśnij link `Run BLAST`.

Formularz programu BLAST:

<img src="./images/ncbi-blast-foxp2-form.png" alt="ncbi-blast-foxp2-form" width="500px">

1. Sekwencją, która najbardziej odpowiada sekwenji FOXP2 człowieka, jest przewidziane białko *forkhead box protein P2* z gwiazdonosa amerykańskiego (Condylura cristata).
2. E-value najlepiej punktowanego przyrównania wynosi `0`.
3. Procent identyczności i podobieństwa tych dwóch sekwencji to `99%`.
4. W przyrównaniu jest jedna przerwa, w sekwencji trafienia.

<img src="./images/ncbi-blast-foxp2-hit.png" alt="ncbi-blast-foxp2-hit" width="500px">

#### Taxonomy reports

5. Wśród ssaków BLAST znalazł `81` trafień.
6. Tak, BLAST zwrócił trafienia wśród ptaków (np. *Parus major*), gadów (np. *Crocodylus porosus*) i płazów (np. jaszczurka *Anolis carolinensis*).

<img src="./images/ncbi-blast-foxp2-taxonomy.png" alt="ncbi-blast-foxp2-taxonomy" width="500px">
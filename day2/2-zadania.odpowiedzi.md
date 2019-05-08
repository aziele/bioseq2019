### Zad. 1 - blastp: identyfikacja sekwencji białka
Otwórz stronę serwisu [NCBI BLAST](https://blast.ncbi.nlm.nih.gov/) i wybierz program *protein blast*. Ogranicz wyszukiwania do bazy danych `UniProtKB/Swiss-Prot`.

<img src="./images/blastp-swissprot-exon5.png" alt="blastp-swissprot-exon5">

Najwyżej punktowane trafienia należą do mitochondrialnej aminotransferazy asparaginianowej.
<br/><br/>

### Zad. 2 - blastp: powtórzony fragment sekwencji
Otwórz stronę serwisu [NCBI BLAST](https://blast.ncbi.nlm.nih.gov/) i wybierz program `Protein BLAST`. W formularzu programu ogranicz wyszukiwania do organizmu *Arabidopsis thaliana*.

<img src="./images/blastp-rrm.png" alt="blastp-rrm" width="500px">

Między białkową sekwencją zapytania cyjanobakterii a sekwencją trafienia `NP_199836.1` *A. thaliana* program *blastp* zidentyfikował dwa przyrównania. Fragment sekwencji zapytania (w pozycji `3-83`) wykazuje podobieństwo do dwóch odrębnych miejsc w sekwencji trafienia (w pozycji `209-289` i pozycji `115-195`).

```
>NP_199836.1 chloroplast RNA-binding protein 31B [Arabidopsis thaliana]
Length=289

 Score = 77.4 bits (189),  Expect = 5e-18, Method: Compositional matrix adjust.
 Identities = 40/81 (49%), Positives = 52/81 (64%), Gaps = 0/81 (0%)

Query  3    IYVGNLSYDVSEADLTAVFAEYGSVKRVQLPTDRETGRMRGFGFVELEADAEETAAIEAL  62
            IYVGNL +DV    L  +F+E+G V   ++ +DRETGR RGFGFV++  + E   AI AL
Sbjct  209  IYVGNLPWDVDSGRLERLFSEHGKVVDARVVSDRETGRSRGFGFVQMSNENEVNVAIAAL  268

Query  63   DGAEWMGRDLKVNKAKPRENR  83
            DG    GR +KVN A+ R  R
Sbjct  269  DGQNLEGRAIKVNVAEERTRR  289


 Score = 62.4 bits (150),  Expect = 2e-12, Method: Compositional matrix adjust.
 Identities = 32/81 (40%), Positives = 48/81 (59%), Gaps = 0/81 (0%)

Query  3    IYVGNLSYDVSEADLTAVFAEYGSVKRVQLPTDRETGRMRGFGFVELEADAEETAAIEAL  62
            ++VGNL YDV    L  +F + G+V+  ++  +R+T + RGFGFV +    E   A+E  
Sbjct  115  LFVGNLPYDVDSQALAMLFEQAGTVEISEVIYNRDTDQSRGFGFVTMSTVEEAEKAVEKF  174

Query  63   DGAEWMGRDLKVNKAKPRENR  83
            +  E  GR L VN+A PR +R
Sbjct  175  NSFEVNGRRLTVNRAAPRGSR  195
```

Przyrównany fragment sekwencji zapytania (w pozycji `3-83`) odpowiada domenie wiążącej RNA (domena RRM). Występuje ona jako pojedyczna domena w sekwencji zapytania, natomiast w sekwencji trafienia *A. thaliana* występuje dwukrotnie. Sekwencja domeny RRM białka zapytania wykazuje większe podobieństwo do domeny RRM z C-końca białka trafienia (`score = 77.4`), niż do N-końcowej domeny RRM (`score = 62.4`).
<br/><br/>

### Zad. 3 - blastp: wyszukiwanie krótkich peptydów
Otwórz stronę serwisu [NCBI BLAST](https://blast.ncbi.nlm.nih.gov) i wybierz **Protein BLAST**. Umieść sekwencje w formacie FASTA w polu `Enter Query Sequence` formularza programu.

```
>s1
GANDALF
>s2
GARFIELDTHECAT
>s3
ELVISLIVES
>s4
CAPTAINCRICK
```

#### GANDALF

```
>WP_008191551.1 DUF642 domain-containing protein [Labrenzia alexandrii]
 EEE44441.1 VCBS repeat protein [Labrenzia alexandrii DFL-11]
Length=3363

 Score = 24.4 bits (50),  Expect = 1421
 Identities = 7/7 (100%), Positives = 7/7 (100%), Gaps = 0/7 (0%)

Query  1     GANDALF  7
             GANDALF
Sbjct  3224  GANDALF  3230
```

#### GARFIELDTHECAT

```
Score   Expect  Identities  Positives   Gaps
32.9 bits(70)   5.7 10/12(83%)  10/12(83%)  1/12(8%)

Query  4    FIELDTHE-CAT  14
            FIELD HE CAT
Sbjct  164  FIELDSHEICAT  175
```

#### ELVISLIVES

```
Alignment statistics for match #1
Score   Expect  Identities  Positives   Gaps
29.1 bits(61)   59  8/9(89%)    9/9(100%)   0/9(0%)
Query  1     ELVISLIVE  9
             ELVISLI+E
Sbjct  1264  ELVISLIIE  1272
```

#### CAPTAINCRICK

```
Alignment statistics for match #1
Score   Expect  Identities  Positives   Gaps
30.3 bits(64)   32  8/10(80%)   9/10(90%)   0/10(0%)
Query  1   CAPTAINCRI  10
           C PTAI+CRI
Sbjct  26  CDPTAIDCRI  35
```
<br/>

### Zad. 4 - blastp: identyfikacja ortologów

1. Otwórz [serwis NCBI](https://www.ncbi.nlm.nih.gov), wybierz białkową bazę danych i skonstruuj poniższe zapytanie:

   ```
   major urinary protein 3[Title] AND Mus musculus[Organism] AND refseq[Filter]
   ```

   W wyniku powyższego zapytania otrzymano 1 rekord: [NP_001034633](https://www.ncbi.nlm.nih.gov/protein/NP_001034633). Ze strony rekordu, w prawym panelu `Analyze this record` wybierz `Run BLAST`. W formularzu programu BLAST wybierz bazę danych `nr` i ogranicz wyszukiwania do organizmu *Monodelphis domestica*.

2. W wynikach programu BLAST, najwyżej ocenioną sekwencją oposa jest `XP_007475409`.

   ```
    >XP_007475409.1 PREDICTED: trichosurin-like [Monodelphis domestica]
    Length=181

     Score = 112 bits (281),  Expect = 2e-31, Method: Compositional matrix adjust.
     Identities = 59/161 (37%), Positives = 94/161 (58%), Gaps = 0/161 (0%)

    Query  19   CIHAEESSSMERNFNVEQISGYWFSIAEASDEREKIEEHGSMRAFVENITVLENSLVFKF  78
                 +HA  +   +   NV Q+SG W SI  AS++ ++I + G M   + NITV E+++ F  
    Sbjct  16   ALHAHRTRPEKHLENVNQLSGPWHSIYLASNDMDRISKGGDMNISIHNITVNESTVTFNV  75

    Query  79   HLIVNEECTEMTAIGEQTEKAGIYYMNYDGFNTFSILKTDYDNYIMIHLINKKDGKTFQL  138
                +L  NEEC  ++ + ++TEK  ++ +NY G N   + +     Y +    N ++GK   L
    Sbjct  76   NLWQNEECIPISMVAKKTEKNNVFKLNYGGENYIYLEELKPKEYAIFCTHNHQNGKETLL  135

    Query  139  MELYGREPDLSLDIKEKFAKLCEEHGIIRENIIDLTNVNRC  179
                MELYG  P L   +K+ F  LC+++GI +ENIID+T V+ C
    Sbjct  136  MELYGWTPILKEKVKKTFKDLCQKYGIDKENIIDMTKVDHC  176
    ```

3. W wynikach programu BLAST w drugim kierunku otrzymano białko użyte w pierwszym zapytaniu.

    ```
    >NP_001034633.1 major urinary protein 3 precursor [Mus musculus]
    Length=184

     Score = 113 bits (282),  Expect = 2e-31, Method: Compositional matrix adjust.
     Identities = 59/160 (37%), Positives = 94/160 (59%), Gaps = 0/160 (0%)

    Query  17   LHAHRTRPEKHLENVNQLSGPWHSIYLASNDMDRISKGGDMNISIHNITVNESTVTFNVN  76
                +HA  +   +   NV Q+SG W SI  AS++ ++I + G M   + NITV E+++ F  +
    Sbjct  20   IHAEESSSMERNFNVEQISGYWFSIAEASDEREKIEEHGSMRAFVENITVLENSLVFKFH  79

    Query  77   LWQNEECIPISMVAKKTEKNNVFKLNYGGENYIYLEELKPKEYAIFCTHNHQNGKETLLM  136
                L  NEEC  ++ + ++TEK  ++ +NY G N   + +     Y +    N ++GK   LM
    Sbjct  80   LIVNEECTEMTAIGEQTEKAGIYYMNYDGFNTFSILKTDYDNYIMIHLINKKDGKTFQLM  139

    Query  137  ELYGWTPILKEKVKKTFKDLCQKYGIDKENIIDMTKVDHC  176
                ELYG  P L   +K+ F  LC+++GI +ENIID+T V+ C
    Sbjct  140  ELYGREPDLSLDIKEKFAKLCEEHGIIRENIIDLTNVNRC  179
    ```
4. Sekwencja białka `XP_007475409` oposa jest prawdopodobnym ortologiem białka MUP3 (`NP_001034633`) myszy.
<br/><br/>

### Zad. 5 - blastx: identyfikacja przesunięcia ramki odczytu
Otwórz stronę serwisu [NCBI BLAST](https://blast.ncbi.nlm.nih.gov/Blast.cgi). Ponieważ sekwencja koduje białko wybierz program **blastx**. W formularzu programu BLAST umieść sekwencję zapytania i przeprowadź przeszukiwanie.

Sekwencja jest najbardziej podobna do białka otoczki wirusa HIV (*HIV1 envelope glycoprotein*) o numerze dostępu `AAL71628.1` (E-value: `1e-104`).

Przesunięcie ramki odczytu widoczne jest na graficznej prezentacji trafień jako mała czarna pionowa linia znajdująca się na trafieniu.

<img src="./images/blastx-hiv.png" alt="blastx-hiv">

Sekwencja trafienia `AAL71628.1` składa się z dwóch przyrównań z sekwencją zapytania. Każde przyrównanie pochodzi z translacji w dwóch różnych ramkach odczytu. Drugie przyrównanie dotyczy początku sekwencji zapytania (`2-268`, ramka oczytu: `+2`) i sekwencji trafienia w pozycji `1-89` (pozycje wyrażone w aminokwasach). Z kolei pierwsze przyrównanie dotyczy drugiej części sekwencij zapytania (`268-600`) i sekwencji trafienia `90-201` (ramka odczytu: `+1`). Przesunięcie ramki odczytu jest więc spowodowane delecją jednego nukleotydu w sekwencji zapytania w pobliżu pozycji `268`.

```
>AAL71628.1 envelope glycoprotein, partial [Human immunodeficiency virus 1]
Length=201

 Score = 226 bits (576),  Expect(2) = 1e-104, Method: Compositional matrix adjust.
 Identities = 110/112 (98%), Positives = 110/112 (98%), Gaps = 1/112 (1%)
 Frame = +1

Query  268  TIAFNQSSGGDPEIVMHSFNCGGEFFYCNTTQLFNSTWPTNK-KSTNKTGTITLPCRIKQ  444
            TIAFNQSSGGDPEIVMHSFNCGGEFFYCNTTQLFNSTWPTN  KSTNKTGTITLPCRIKQ
Sbjct  90   TIAFNQSSGGDPEIVMHSFNCGGEFFYCNTTQLFNSTWPTNNTKSTNKTGTITLPCRIKQ  149

Query  445  IINRWQEVGKAMYAPPIKGQIRCSSNITGIFLTRDGGNASDETETFRPGGGN  600
            IINRWQEVGKAMYAPPIKGQIRCSSNITGIFLTRDGGNASDETETFRPGGGN
Sbjct  150  IINRWQEVGKAMYAPPIKGQIRCSSNITGIFLTRDGGNASDETETFRPGGGN  201


 Score = 182 bits (461),  Expect(2) = 1e-104, Method: Compositional matrix adjust.
 Identities = 89/89 (100%), Positives = 89/89 (100%), Gaps = 0/89 (0%)
 Frame = +2

Query  2    EEDIVIRSENFTNNAKTIIVQLKESIKINCTRPNNNTRKSIPIATGGAIYATGDIIGDIR  181
            EEDIVIRSENFTNNAKTIIVQLKESIKINCTRPNNNTRKSIPIATGGAIYATGDIIGDIR
Sbjct  1    EEDIVIRSENFTNNAKTIIVQLKESIKINCTRPNNNTRKSIPIATGGAIYATGDIIGDIR  60

Query  182  QAHCNLSRDQWDNTLSQLVTKLREQFGNK  268
            QAHCNLSRDQWDNTLSQLVTKLREQFGNK
Sbjct  61   QAHCNLSRDQWDNTLSQLVTKLREQFGNK  89
```
<br/>



### Zad. 6 - Identyfikacja polimorfizmów w genomach wirusów HIV
Otwórz stronę serwisu [NCBI BLAST](https://blast.ncbi.nlm.nih.gov/Blast.cgi). Wybierz program `Nucleotide BLAST` i algorytm `blastn`. W wynikach programu BLAST ustaw `Formatting Options` > `Alignment view` > `Flat query-anchored with dots for identities`).

<img src="./images/blastn-snp.png" alt="blastn-snp">

W pozycji 6 przyrównań występują warianty `A/G`.
<br/><br/>

### Zad. 7 - blastn: ograniczanie bazy sekwencji BLAST przez zapytanie Entrez
Otwórz stronę serwisu [NCBI BLAST](https://blast.ncbi.nlm.nih.gov/Blast.cgi). Wybierz program **nucleotide BLAST**, algorytm `blastn`. Umieść sekwencję i w polu `Entrez Query` umieść poniższe zapytanie:

```
1:100[SLEN]
```

Wynik programu BLAST:

```
>LK006556.1 TPA: Enterobacter sp. 638 tRNA-Arg-ACG-1-1 gene
 LK006557.1 TPA: Enterobacter sp. 638 tRNA-Arg-ACG-1-2 gene
 LK006558.1 TPA: Enterobacter sp. 638 tRNA-Arg-ACG-1-3 gene
 LK006559.1 TPA: Enterobacter sp. 638 tRNA-Arg-ACG-1-4 gene
 LK006749.1 TPA: Escherichia coli 536 tRNA-Arg-ACG-1-1 gene
 LK006750.1 TPA: Escherichia coli 536 tRNA-Arg-ACG-1-2 gene
 LK006751.1 TPA: Escherichia coli 536 tRNA-Arg-ACG-1-3 gene
 LK006752.1 TPA: Escherichia coli 536 tRNA-Arg-ACG-1-4 gene
 LK006833.1 TPA: Escherichia coli APEC O1 tRNA-Arg-ACG-1-1 gene
 LK006834.1 TPA: Escherichia coli APEC O1 tRNA-Arg-ACG-1-2 gene
 LK006835.1 TPA: Escherichia coli APEC O1 tRNA-Arg-ACG-1-3 gene
 LK006836.1 TPA: Escherichia coli APEC O1 tRNA-Arg-ACG-1-4 gene
 LK006927.1 TPA: Escherichia coli CFT073 tRNA-Arg-ACG-1-1 gene
 LK006928.1 TPA: Escherichia coli CFT073 tRNA-Arg-ACG-1-2 gene
 LK006929.1 TPA: Escherichia coli CFT073 tRNA-Arg-ACG-1-3 gene
 LK006930.1 TPA: Escherichia coli CFT073 tRNA-Arg-ACG-1-4 gene
 LK006931.1 TPA: Escherichia coli CFT073 tRNA-Arg-ACG-1-5 gene
 LK007017.1 TPA: Escherichia coli str. K-12 substr. DH10B tRNA-Arg-ACG-1-1 
gene
 LK007018.1 TPA: Escherichia coli str. K-12 substr. DH10B tRNA-Arg-ACG-1-2 
gene
 LK007019.1 TPA: Escherichia coli str. K-12 substr. DH10B tRNA-Arg-ACG-1-3 
gene
 LK007104.1 TPA: Escherichia coli E24377A tRNA-Arg-ACG-1-1 gene
 LK007105.1 TPA: Escherichia coli E24377A tRNA-Arg-ACG-1-2 gene
 LK007106.1 TPA: Escherichia coli E24377A tRNA-Arg-ACG-1-3 gene
 LK015261.1 TPA: Salmonella enterica subsp. enterica serovar Paratyphi B 
str. SPB7 tRNA-Arg-ACG-1-1 gene
 LK015262.1 TPA: Salmonella enterica subsp. enterica serovar Paratyphi B 
str. SPB7 tRNA-Arg-ACG-1-2 gene
 LK015263.1 TPA: Salmonella enterica subsp. enterica serovar Paratyphi B 
str. SPB7 tRNA-Arg-ACG-1-3 gene
 LK015264.1 TPA: Salmonella enterica subsp. enterica serovar Paratyphi B 
str. SPB7 tRNA-Arg-ACG-1-4 gene
 LK016441.1 TPA: Shigella boydii CDC 3083-94 tRNA-Arg-ACG-1-1 gene
 LK016442.1 TPA: Shigella boydii CDC 3083-94 tRNA-Arg-ACG-1-2 gene
 LK016443.1 TPA: Shigella boydii CDC 3083-94 tRNA-Arg-ACG-1-3 gene
 LK016542.1 TPA: Shigella boydii Sb227 tRNA-Arg-ACG-1-1 gene
 LK016543.1 TPA: Shigella boydii Sb227 tRNA-Arg-ACG-1-2 gene
 LK016544.1 TPA: Shigella boydii Sb227 tRNA-Arg-ACG-1-3 gene
 LK016631.1 TPA: Shigella flexneri 2a str. 2457T tRNA-Arg-ACG-1-1 gene
 LK016632.1 TPA: Shigella flexneri 2a str. 2457T tRNA-Arg-ACG-1-2 gene
 LK016633.1 TPA: Shigella flexneri 2a str. 2457T tRNA-Arg-ACG-1-3 gene
 LK016727.1 TPA: Shigella flexneri 5 str. 8401 tRNA-Arg-ACG-1-1 gene
 LK016728.1 TPA: Shigella flexneri 5 str. 8401 tRNA-Arg-ACG-1-2 gene
 LK016729.1 TPA: Shigella flexneri 5 str. 8401 tRNA-Arg-ACG-1-3 gene
 LK016827.1 TPA: Shigella sonnei Ss046 tRNA-Arg-ACG-1-1 gene
 LK016828.1 TPA: Shigella sonnei Ss046 tRNA-Arg-ACG-1-2 gene
 LK016829.1 TPA: Shigella sonnei Ss046 tRNA-Arg-ACG-1-3 gene
 LK016830.1 TPA: Shigella sonnei Ss046 tRNA-Arg-ACG-1-4 gene
 LK016979.1 TPA: Sodalis glossinidius str. 'morsitans' tRNA-Arg-ACG-1-1 gene
 LK007195.1 TPA: Escherichia coli HS tRNA-Arg-ACG-1-1 gene
 LK007196.1 TPA: Escherichia coli HS tRNA-Arg-ACG-1-2 gene
 LK007197.1 TPA: Escherichia coli HS tRNA-Arg-ACG-1-3 gene
 LK007198.1 TPA: Escherichia coli HS tRNA-Arg-ACG-1-4 gene
 LK007283.1 TPA: Escherichia coli UTI89 tRNA-Arg-ACG-1-1 gene
 LK007284.1 TPA: Escherichia coli UTI89 tRNA-Arg-ACG-1-2 gene
 LK007285.1 TPA: Escherichia coli UTI89 tRNA-Arg-ACG-1-3 gene
 LK009359.1 TPA: Klebsiella pneumoniae subsp. pneumoniae MGH 78578 tRNA-Arg-ACG-1-1 
gene
 LK009360.1 TPA: Klebsiella pneumoniae subsp. pneumoniae MGH 78578 tRNA-Arg-ACG-1-2 
gene
 LK009361.1 TPA: Klebsiella pneumoniae subsp. pneumoniae MGH 78578 tRNA-Arg-ACG-1-3 
gene
 LK009362.1 TPA: Klebsiella pneumoniae subsp. pneumoniae MGH 78578 tRNA-Arg-ACG-1-4 
gene
Length=77

 Score = 140 bits (154),  Expect = 5e-34
 Identities = 77/77 (100%), Gaps = 0/77 (0%)
 Strand=Plus/Plus

Query  1   GCATCCGTAGCTCAGCTGGATAGAGTACTCGGCTACGAACCGAGCGGTCGGAGGTTCGAA  60
           ||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||
Sbjct  1   GCATCCGTAGCTCAGCTGGATAGAGTACTCGGCTACGAACCGAGCGGTCGGAGGTTCGAA  60

Query  61  TCCTCCCGGATGCACCA  77
           |||||||||||||||||
Sbjct  61  TCCTCCCGGATGCACCA  77
```

Przeszukiwana baza danych BLAST obejmuje `585 748` sekwencji.
> `Search Summary` > `Database` > `Number of sequences`

<br/>



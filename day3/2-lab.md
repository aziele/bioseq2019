## Motywy i domeny białkowe

### Zad. 1 - serwis Pfam
Wykorzystaj serwis [Pfam](https://pfam.xfam.org) i zidentyfikuj domeny białkowe obecne w poniższej sekwencji: 

```
>sequence
NNRNQDNYVSWSDSEDDDEDEEIEEKEKPETNFPSPFTNILCGIIFVERRYTAVVLNRLI
KEAGKQDPELAYISSNFITGHGIGKNQPRNKQMEAEFRKQEEVLRKFRAHETNLLIATSI
VEEGVDIPKCNLVVRFDLPTEYRSYVQSKGRARAPISNYIMLADTDKIKSFEEDLKTYKA
IEKILRNKCSKSVDTGETDIDPVMDDDDVFPPYVLRPDDGGPRVTINTAIGHINRYCARL
PSDPFTHLAPKCRTRELPDGTFYSTLYLPINSPLRASIVGPPMSCVRLAERVVALICCEK
LHKIGELDDHLMPVGKETVKYEEELDLHDEEETSVPGRPGSTKRRQCYPKAIPECLRDSY
PRPDQPCYLYVIGMVLTTPLPDELNFRRRKLYPPEDTTRCFGILTAKPIPQIPHFPVYTR
SGEVTISIELKKSGFMLSLQMLELITRLHQYIFSHILRLEKPALEFKPTDADSAYCVLPL
NVVNDSSTLDIDFKFMEDIEKSEARIGIPSTKYTKETPFVFKLEDYQDAVIIPRYRNFDQ
PHRFYVADVYTDLTPLSKFPSPEYETFAEYYKTKYNLDLTNLNQPLLDVDHTSSRLNLLT
PRHLNQKGKALPLSSAEKRKAKWESLQNKQILVPELCAIHPIPASLWRKAVCLPSILYRL
HCLLTAEELRAQTASDAGVGVRSLPADFRYPNLDFGWKKSIDSKSFISISNSSSAENDNY
CKHSTIVPENAAHQGANRTSSLENHDQMSVNCRTLLSESPGKLHVEVSADLTAINGLSYN
QNLANGSYDLANRDFCQGNQLNYYKQEIPVQPTTSYSIQNLYSYENQPQPSDECTLLSNK
YLDGNANKSTSDGSPVMAVMPGTTDTIQVLKGRMDSEQSPSIGYSSRTLGPNPGLILQAL
TLSNASDGFNLERLEMLGDSFLKHAITTYLFCTYPDAHEGRLSYMRSKKVSNCNLYRLGK
KKGLPSRMVVSIFDPPVNWLPPGYVVNQDKSNTDKWEKDEMTKDCMLANGKLDEDYEEED
EEEESLMWRAPKEEADYEDDFLEYDQEHIRFIDNMLMGSGAFVKKISLSPFSTTDSAYEW
KMPKKSSLGSMPFSSDFEDFDYSSWDAMCYLDPSKAVEEDDFVVGFWNPSEENCGVDTGK
QSISYDLHTEQCIADKSIADCVEALLGCYLTSCGERAAQLFLCSLGLKVLPVIKRTDREK
ALCPTRENFNSQQKNLSVSCAAASVASSRSSVLKDSEYGCLKIPPRCMFDHPDADKTLNH
LISGFENFEKKINYRFKNKAYLLQAFTHASYHYNTITDCYQRLEFLGDAILDYLITKHLY
EDPRQHSPGVLTDLRSALVNNTIFASLAVKYDYHKYFKAVSPELFHVIDDFVQFQLEKNE
MQGMDSELRRSEEDEEKEEDIEVPKAMGDIFESLAGAIYMDSGMSLETVWQVYYPMMRPL
IEKFSANVPRSPVRELLEMEPETAKFSPAERTYDGKVRVTVEVVGKGKFKGVGRSYRIAK
SAAARRALRSLKANQPQVPNS
```

1. Ile łącznie domen lub rodzin domen zostało zidentyfikowanych w analizowanej sekwencji?
2. W jakiej pozycji w sekwnecji znajduje się domena `Dicer_dimer`?
3. Podaj wartość `E-value` przyrównania domeny `Dicer_dimer` z modelem HMM?

Wejdź do rekordu domeny `Dicer_dimer`.

4. Podaj numer dostępu tej domeny w bazie Pfam.
5. Jaką funkcję pełni ta domena (krótko)?
6. Ile gatunków posiada tę domenę białkową?

Wejdź w zakładkę `Species`.

7. Czy domena występuje u organizmów prokariotycznych?
8. W ilu gatunkach owadów występuje ta domena?

Będąc w zakladce `Species`, kliknij na kartę `Tree`.

9. Ile sekwencji białek człowieka posiada tę domenę?
10. Ile sekwencji białek człowiekowatych (*Hominidae*) posiada tę domenę. Podaj numery dostępu tych białek.

Przejdź do zakładki `HMM logo`.

11. Ile wynosi długość sekwencji domeny `Dicer_dimer`?
12. Jakie dwa aminokwasy są najbardziej zachowane w pozycji 8 sekwencji domeny?

Przejdź do zakładki `Domain organization`.

13. Podaj najczęściej występujący układ domen w białkach, w którym występuje domena `Dicer_domain`.


### Zad. 2 - serwis PROSITE
Użyj sekwencji z zad. 1 i serwisu [PROSITE](https://prosite.expasy.org/prosite.html) w celu identyfikacji domen i motywów białkowych.

1. Podaj nazwę domeny, której nie zidentyfikowano wcześniej w seriwsie Pfam.
   * Jaką funkcję pełni ta domena?
2. Podaj numer dostępu domeny typu Dicer.
3. Czy lokalizacja domeny Dicer w sekwencji jest taka sama, jak w przewidywaniach Pfam?

Wejdź w rekord domeny Dicer w bazie PROSITE.

4. Podaj długość profilu domeny Dicer w bazie PROSITE.
5. Czy w logo domeny Dicer aminokwasy `Y` i `F` są najbardziej zachowanymi aminokwasami?
6. Wejdź w `Taxonomic distribution` domeny Dicer.
   * Czy domena występuje u organizmów prokariotycznych?


### Zad. 3 - metaserwis InterPro
Użyj sekwencji z zad. 1 i serwisu [InterPro](http://www.ebi.ac.uk/interpro/) w celu identyfikacji domen białkowych.

1. Ile domen białkowych zidentyfikowano?
2. Podaj numer dostępu domeny typu Dicer.
3. Podaj lokalizacaję domeny Dicer w sekwencji.
4. W oparciu o jakie bazy danych domen białkowych, domena Dicer została zidentyfikowana?

Wejdź w rekord domeny Dicer.

5. Ile sekwencji białkowych zawieraj domenę Dicer?
   > Ile z tych białek należy do *Eukaryota* i *Prokaryota*?
6. Ile jest różnych układów domen (`Domain architectures`), w których występuje domena Dicer?
7. Wymień szlaki biochemiczne, w które zaangażowana jest domena Dicer.


### Zad. 4 - Informacje o domenach w rekordach UniProt
Użyj programu BLAST na stronie serwisu [UniProt](*https://www.uniprot.org/) w celu zidentyfikowania sekwencji białkowej z zadania 1.

1. Podaj numer dostępu oraz nazwę znalezionej sekwencji.

Przejdź do rekordu sekwencji.

2. Czy w rekordzie UniProt zawarte są informacje o domenach występujących w tym białku?


### Zad. 5 - InterProt: powiązania między domenami
Korzystając z serwisu InterPro przeanalizuj poniższą sekwencję:

```
>seq1
MELRVLLCWASLAAALEETLLNTKLETADLKWVTFPQVDGQWEELSGLDEEQHSVRTYEV
CDVQRAPGQAHWLRTGWVPRRGAVHVYATLRFTMLECLSLPRAGRSCKETFTVFYYESDA
DTATALTPAWMENPYIKVDTVAAEHLTRKRPGAEATGKVNVKTLRLGPLSKAGFYLAFQD
QGACMALLSLHLFYKKCAQLTVNLTRFPETVPRELVVPVAGSCVVDAVPAPGPSPSLYCR
EDGQWAEQPVTGCSCAPGFEAAEGNTKCRACAQGTFKPLSGEGSCQPCPANSHSNTIGSA
VCQCRVGYFRARTDPRGAPCTTPPSAPRSVVSRLNGSSLHLEWSAPLESGGREDLTYALR
CRECRPGGSCAPCGGDLTFDPGPRDLVEPWVVVRGLRPDFTYTFEVTALNGVSSLATGPV
PFEPVNVTTDREVPPAVSDIRVTRSSPSSLSLAWAVPRAPSGAVLDYEVKYHEKGAEGPS
SVRFLKTSENRAELRGLKRGASYLVQVRARSEAGYGPFGQEHHSQTQLDESEGWREQLAL
IAGTAVVGVVLVLVVIVVAVLCLRKQSNGREAEYSDKHGQYLIGHGTKVYIDPFTYEDPN
EAVREFAKEIDVSYVKIEEVIGAGEFGEVCRGRLKAPGKKESCVAIKTLKGGYTERQRRE
FLSEASIMGQFEHPNIIRLEGVVTNSMPVMILTEFMENGALDSFLRLNDGQFTVIQLVGM
LRGIASGMRYLAEMSYVHRDLAARNILVNSNLVCKVSDFGLSRFLEENSSDPTYTSSLGG
KIPIRWTAPEAIAFRKFTSASDAWSYGIVMWEVMSFGERPYWDMSNQDVINAIEQDYRLP
PPPDCPTSLHQLMLDCWQKDRNARPRFPQVVSALDKMIRNPASLKIVARENGGASHPLLD
QRQPHYSAFGSVGEWLRAIKMGRYEESFAAAGFGSFELVSQISAEDLLRIGVTLAGHQKK
ILASVQHMKSQAKPGTPGGTGGPAPQY
```

1. Do jakiej rodziny białkowej zostało zaklasyfikowane to białko?
2. Ile domen białkowych zostało zidentyfikowanych w sekwencji zapytania?
3. Podaj lokalizację domeny kinazowej `Protein kinase domain (IPR000719)`.
4. Czy domena kinazowa zawiera miejsce wiązanie ATP i centrum aktywne?

Wejdź do rekordu domeny kinazowej `IPR000719`.

5. Wymień bazy domen, na podstawie których tworzony jest ten rekord (`Contributing signatures`).
6. Czy w obrębie domeny kinazowej można wyróżnić bardziej specyficzne domeny kinazowe? (`Domain relationships`)
7. Podaj nazwę nadrodziny, w skład której wchodzi domena kinazowa.


### Zad. 6 - InterPro: mutacja w obrębie domeny
Poniżej znajduje się sekwencja białkowa `seq2` odpowiadająca sekwencji `seq1` z poprzedniego zadania, ale pochodząca od pacjenta chorującego na pewne schorzenie.

```
>seq2
MELRVLLCWASLAAALEETLLNTKLETADLKWVTFPQVDGQWEELSGLDEEQHSVRTYEV
CDVQRAPGQAHWLRTGWVPRRGAVHVYATLRFTMLECLSLPRAGRSCKETFTVFYYESDA
DTATALTPAWMENPYIKVDTVAAEHLTRKRPGAEATGKVNVKTLRLGPLSKAGFYLAFQD
QGACMALLSLHLFYKKCAQLTVNLTRFPETVPRELVVPVAGSCVVDAVPAPGPSPSLYCR
EDGQWAEQPVTGCSCAPGFEAAEGNTKCRACAQGTFKPLSGEGSCQPCPANSHSNTIGSA
VCQCRVGYFRARTDPRGAPCTTPPSAPRSVVSRLNGSSLHLEWSAPLESGGREDLTYALR
CRECRPGGSCAPCGGDLTFDPGPRDLVEPWVVVRGLRPDFTYTFEVTALNGVSSLATGPV
PFEPVNVTTDREVPPAVSDIRVTRSSPSSLSLAWAVPRAPSGAVLDYEVKYHEKGAEGPS
SVRFLKTSENRAELRGLKRGASYLVQVRARSEAGYGPFGQEHHSQTQLDESEGWREQLAL
IAGTAVVGVVLVLVVIVVAVLCLRKQSNGREAEYSDKHGQYLIGHGTKVYIDPFTYEDPN
EAVREFAKEIDVSYVKIEEVIGAGEFGEVCRGRLKAPGKKESCVAISTLKGGYTERQRRE
FLSEASIMGQFEHPNIIRLEGVVTNSMPVMILTEFMENGALDSFLRLNDGQFTVIQLVGM
LRGIASGMRYLAEMSYVHRDLAARNILVNSNLVCKVSDFGLSRFLEENSSDPTYTSSLGG
KIPIRWTAPEAIAFRKFTSASDAWSYGIVMWEVMSFGERPYWDMSNQDVINAIEQDYRLP
PPPDCPTSLHQLMLDCWQKDRNARPRFPQVVSALDKMIRNPASLKIVARENGGASHPLLD
QRQPHYSAFGSVGEWLRAIKMGRYEESFAAAGFGSFELVSQISAEDLLRIGVTLAGHQKK
ILASVQHMKSQAKPGTPGGTGGPAPQY
```

Przeprowadź globalne przyrównanie obu sekwencji. 

1. Jakie zmiany w sekwencji tego białka występują u chorego pacjenta?

Przeanalizuj białko pacjenta przy użyciu serwisu InterPro i porównaj z wynikami InterPro osoby zdrowej. 

2. W obrębie, której domeny doszło do mutacji u pacjenta?


### Zad. 7 - InterPro: wszystkie białka zawierające domenę RRM.
Otwórz stronę serwisu [InterProt](https://www.ebi.ac.uk/interpro/). W polu szybkiego wyszukiwania po prawej stronie wyszukaj domenę RRM (*RNA recognition motif domain*).

1. Podaj numer dostępu tej domeny.
2. Podaj liczbę białek zawierających domenę RRM u bakterii.


### Zad. 8 - UniProt: wszystkie białka zawierające domenę RRM
W bazie UniProt wyszukaj wszystkie białka zawierające domenę RRM u bakterii. Ile białek otrzymano?


## MEME - Identyfikacja nowych motywów/domen białkowych

### Zad. 9
W pliku [sequences.fasta](./data/sequences.fasta) znajduje się 6 sekwencji białkowych, które pełnią podobną funkcję. Celem tego zadania jest znalezienie motywów sekwencji wspólnych dla tych sekwencji.

Użyj serwisu [MEME](http://meme-suite.org) i wybierz `Motif Discvovery` > `MEME`. W formularzu, w sekcji `Select the site distribution` wybierz opcję `Any number of repetitions`. Wklej sekwencje lub załaduj je z pliku i rozpocznij analizę.

1. Ile motywów znaleziono?
2. Które motywy są obecne we wszystkich 6 sekwencjach?
3. Sprawdź w serwisie InterPro, czy zidentyfikowane motywy odpowiadają znanym już domenom białkowym.
4. Jaką funkcję pełnią te motywy?
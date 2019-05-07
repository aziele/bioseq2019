### Zad. 1 - blastp: identyfikacja sekwencji białka
Zidentyfikuj funkcję poniższego białka w bazie *SwissProt*. Sekwencja została wygenerowana w oparciu o translację 5 egzonu pewnego genu z jednego gatunku *Drosophila*.

```
MSQICKRGLLISNRLAPAALRCKSTWFSEVQMGPPDAILGVTEAFKKDTNPKKINLGAGAYRDDNTQPFV
LPSVREAEKRVVSRSLDKEYATIIGIPEFYNKAIELALGKGSKRLAAKHNVTAQSISGTGALRIGAAFLA
KFWQGNREIYIPSPSWGNHVAIFEHAGLPVNRYRYYDKDTCALDFGGLIEDLKKIPEKSIVLLHACAHNP
TGVDPTLEQWREISALVKKRNLYPFIDMAYQGFATGDIDRDAQAVRTFEADGHDFCLAQSFAKNMGLYGE
RAGAFTVLCSDEEEAARVMSQVKILIRGLYSNPPVHGARIAAEILNNEDLRAQWLKDVKLMADRIIDVRT
KLKDNLIKLGSSQNWDHIVNQIGMFCFTGLKPEQVQKLIKDHSVYLTNDGRVSMAGVTSKNVEYLAESIH
KVTK
```
<br/>

### Zad. 2 - blastp: powtórzony fragment sekwencji
Znajdź białko u *Arabidopsis thaliana* homologiczne do poniższej sekwencji białkowej wiążącej RNA u cyjanobakterii *Synechocystis sp.*.

```
>sp|Q57014|RBPA_SYNY3 Putative RNA-binding protein RbpA OS=Synechocystis sp.
MSIYVGNLSYDVSEADLTAVFAEYGSVKRVQLPTDRETGRMRGFGFVELEADAEETAAIEALDGAEWMGR
DLKVNKAKPRENRSGGGSFGGGRKSYGGSRY
```

Ile lokalnych przyrównań występuje między sekwencję zapytania a sekwencją najlepszego trafienia?
<br/><br/>

### Zad. 3 - blastn: identyfikacja polimorfizmów w genomach wirusów HIV
Ostatnio badano oporność lekową wirusa HIV u dzieci i dorosłych poddanych różnym terapiom leczenia. Wykorzystaj poniższą sekwencję zapytania wirusa HIV oraz program BLAST do identyfikacji polimorfizmu pojedynczego nukleotydu (SNP) w izolatach HIV od pacjentów (sekwencje w bazie danych). W wynikach programu BLAST ustaw `Formatting Options` > `Alignment view` > `Flat query-anchored with dots for identities`).

```
ATGACCTCAAATCACTCTTTGGCAACGACCCCTCGTCACAATAAAGATAGGGGGGCAACTAAAGGAAGCT
CTATTAGATACAGGAGCAGATGATACAGTATTAGAAGAAATGGAGTTGCCAGGAAGATGGAAACCAAAAA
TGATAGGGGGAATTGGAGGTTTTATCAAAGTAAGACAGTATGATCAGATACCCATAGAAATCTGTGGACA
TAGAGCTATAGGTACAGTATTAGTAGGACCTACACCTGTCAACATAATTGGAAGAAATCTGTTGACTCAG
CTTGGTTGCACTTTAAATTTTCCCATAAGTCCTATTGAAACTGTACCAGTAAAATTAAAGCCAGGAATGG
ATGGCCCAAAAGTTAAACAATGGCCATTGACAGAAGAAAAAATAAAAGCATTAGTAGAAATTTGTACAGA
AATGGAAAAGGAAGGGAAAATTTCAAAAATTGGGCCTGAAAATCCATACAATACTCCAGTATTTGCCATA
AAGAAAAAAGACAGTACTAAATGGAGAAAATTAGTAGATTTCAGAGAACTTAATAAGAAAACTCAAGACT
TCTGGGAAGTTCAATTAGGAATACCACATCCCGCAGGGTTAAAAAAGAAAAAATCAGTAACAGTACTGGA
TGTGGGTGATGCATATTTTTCAGTTCCCTTAGATAAAGACTTCAGGAAGTACACTGCATTTACCATACCT
AGTATAAACAATGAGACACCAGGGATTAGATATCAGTACAATGTGCTTCCACAGGGATGGAAAGGATCAC
CAGCAATATTCCAAAGTAGTATGACAAAAATTTTAGAGCCTTTTAGAGAACAAAATCCAGAAATAGTTAT
CTATCAATACATGGATGATTTGTATGTAGGATCTGACTTAGAACTAGGGCAGCATAGAGCAAAAATAGAG
GAACTGAGACGACATCTGTTGAGGTGGGGATTTACCACACCAGACAAAAAACATCAGAAAGAGCCTCCAT
TCCTTTGGA
```

Jakie SNP występują w pozycji 6 znalezionych trafień?
<br/><br/>

### Zad. 4 - blastn: ograniczanie bazy sekwencji BLAST przez zapytanie Entrez
Poniżej znajduje się sekwencja nukleotydowa tRNA. Przy pomocy programu `blastn` znajdź w bazie `nr` rekordy zawierające sekwencje do niej podobne, ale nie dłuższe niż `100` nukleotydów.  

```
GCATCCGTAGCTCAGCTGGAtAGAGTACTCGGCTACGAACCGAGCGGtCGGAGGTTCGAATCCTCCCGGA
TGCACCA
```

Podaj liczbę sekwencji przeszukiwanej bazy danych BLAST.
<br/><br/>

### Zad. 5 - blastx: identyfikacja przesunięcia ramki odczytu

Użyj programu **blastx** do znalezienia białka najbardziej podobnego do poniższej sekwencji nukleotydowej. 

```
AGAAGAAGACATAGTAATTAGATCTGAAAATTTTACGAACAATGCTAAAACCATAATAGT
ACAGCTGAAGGAATCTATAAAAATTAATTGTACAAGACCCAACAACAATACAAGAAAAAG
TATACCTATAGCAACGGGGGGAGCAATTTATGCAACAGGAGACATAATAGGAGATATAAG
ACAAGCACATTGTAACCTTAGTAGAGACCAATGGGATAACACTTTAAGCCAGCTAGTTAC
AAAACTAAGAGAACAATTTGGGAATAAACAATAGCCTTTAATCAATCCTCAGGAGGGGAC
CCAGAAATTGTAATGCACAGTTTTAATTGTGGAGGAGAATTTTTCTACTGTAATACAACA
CAGCTGTTTAATAGTACTTGGCCAACTAATAAAAAGTCTACTAACAAAACAGGAACTATC
ACACTCCCGTGCAGAATAAAACAAATTATAAACAGGTGGCAAGAAGTAGGAAAAGCAATG
TATGCCCCTCCCATCAAGGGACAAATTAGATGTTCATCAAATATTACAGGGATATTCTTA
ACAAGAGATGGTGGTAACGCAAGCGATGAGACCGAGACCTTCAGACCTGGAGGAGGAAAT
A
```

Sekwencja koduje białko, ale występuje w niej przesunięcie ramki odczytu (*frameshift*). W oparciu o wyniki programu BLAST zidentyfikuj miejsce przesunięcia ramki odczytu.
<br/><br/>

### Zad. 6 - blastp: identyfikacja ortologów
Główne białko moczu (*MUP*, *major urinary protein*) zwierząt bierze udział w wywoływanie strachu między różnymi gatunkami zwierząt. Na przykład, myszy wyczuwają i boją się zapachu białek MUP szczurów i kotów.

Celem zadania jest znalezienie sekwencji oposa ortologicznej do białka MUP3 myszy.

1. Znajdź w bazie RefSeq sekwencję białka MUP3 myszy i uruchom program **blastp** w celu przeszukania bazy `nr` sekwencji oposa (*Monodelphis domestica*). 
2. W wynikach programu BLAST, zidentyfikuj jedną lub więcej sekwencji oposa, które mogą być ortologami MUP3 myszy.
3. Uruchom program BLAST w odwrotnym kierunku: organizm `Mus musculus` i baza `RefSeq`.
4. Na postawie wyników programu BLAST, zidentyfikuj sekwencję ortologiczną.
<br/>

### Zad. 7 - blastp: wyszukiwanie krótkich peptydów
Czy którakolwiek z poniższych z sekwencji aminokwasowych występuje w sekwencjach białkowych bazy `nr`?

* `GANDALF`
* `GARFIELDTHECAT`
* `ELVISLIVES`
* `CAPTAINCRICK`

Jeżeli tak to, czy ich dopasowania są istotne statystycznie?
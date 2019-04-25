## Przyrównanie sekwencji - podstawowe informacje


### Zad. 1 - Format zapisu przyrównania sekwencji nukleotydowych
Wejściowe sekwencje DNA:

```
>dna1
GATACTAT
>dna2
GATTTCAAT
```

Przyrównanie pary sekwencji (dwie formy zapisu):

```
dna1   GA-TACTA-T                       dna1   GA-TACTA-T
       || |.| | |                       dna2   GATTTC-AAT
dna2   GATTTC-AAT
```

Odpowiedz na pytania:

1. Ile wynosi długość powyższego przyrówania?
2. Na ilu pozycjach przyrównania nukleotydy są:
   * zgodne (*match*)
   * niezgodne (*mismatch*)?
3. Ile wynosi procent *identyczności* przyrównanych sekwencji?
4. Ile wynosi wartość punktacji (*score*) przyrównania sekwencji? Przyjmij poniższy system punktacji:
   * elementy zgodne (*match*): `2`
   * elementy niezgodne (*mismatch*): `-1`
   * przerwa (*gap*): `-2`
<br/><br/>


### Zad. 2 - Format zapisu przyrównania sekwencji aminokwasowych
Poniżej znajduje się przyrównanie dwóch sekwencji białkowych.

```
s1   MSSE-                       s1   MSSE-
     ||.:                        s2   MSKQI
s2   MSKQI
```

Odpowiedz na pytania:

1. Ile wynosi procent *identyczności* przyrównywanych sekwencji?
2. Podaj wartość *score* całego przyrównania przy zastosowaniu macierzy <a href="ftp://ftp.ncbi.nlm.nih.gov/blast/matrices/BLOSUM62" target="_blank">BLOSUM62</a> i kary za przerwę: `-5`.
3. Ile wynosi procent *podobieństwa* przyrównywanych sekwencji?
<br/><br/>


## Programy Needle i Water

### Zad. 3 - Przyrównanie lokalne i semi-globalne sekwencji DNA
Poniżej znajduje się sekwencja genomowa genu insuliny ponocnicny trójpręgowej oraz sekwencja CDS tego genu. 

```
>J02989.1:DNA Owl monkey (A.trivirgatus) insulin gene, genomic
GGCCTAGCTAGGGCTGCTGTCCTGGGGTGGGCTGGGAATGGGCAGCCATCAGGCAGGGGCCCCCTCACTC
CCCTACCCCGACAACCTCGGCCCACCCATGGGGGCATCTCGGGCAACCAGAGATAGAGGGCAGGGGTCTG
GGGACAGCAGCGTGAAGAGCCCCGCCCTGCAGCCTCCCGCACTCCTGGTCTAATGTGGAAAGTGGCCCAG
ATGAGGGCTTTGCTCTCCTGGAGACATTTGCCCCCAGCTGTGAGCAGGGACAGGACTGGCCACCAGCGCC
TGGTTAAGACTCTAATGACCACCCCTCCCGGCCCTGAGGAAGAGGTGCTGACGACCAAGGAGATATTCCC
GCAGACCCAGCAGCCGGGAAATGATCTGGAAAGTGCAGCCTCAGCCCCCAGCCATCTGCCAGCCCCTGCA
CCTCAGGCCCTAATGGGCCAGGCGGCAAGGTTGGCAGGTAGGGGAGATGGGCTCTGGGCCTATAAAGCCA
GCAGGGACCCAGCAGCCCTCACGCCCGGGACCAGCTGCATCACAGGAGGCCAGCGAGCAGGTCTGTTCCA
AGGGCCTTCGAGCCAGTCTGGGCCCCAGGGCTGCCCCACTCGGGGTTCCAGAGCAGTTGGACCCCAGGTC
TCAGCGGGAGGGTGTGGCTGGGCTCTGAAGCATTTGGGTGAGCCCAGGGGCTCAGGGCAGGGCACCTGCC
TTCAGCGGCCTCAGCCTGCCTGTCTCCCAGGTCTCTGTCCTTCCACCATGGCCCTGTGGATGCACCTCCT
GCCCCTGCTGGCGCTGCTGGCCCTCTGGGGACCCGAGCCAGCCCCGGCCTTTGTGAACCAGCACCTGTGC
GGCCCCCACCTGGTGGAAGCCCTCTACCTGGTGTGCGGGGAGCGAGGTTTCTTCTACGCACCCAAGACCC
GCCGGGAGGCGGAGGACCTGCAGGGTGAGCCCCACCGCCCCTCCGTGCCCCCGCCGCCCCCAGCCACCCC
CACTCCCGCTGCTCCCACCCAGCCTGGGCAGAAGGGGACAGGAGGCTGCTACCAGTAGGGAGACAGGTGG
ACTTTTTAAAAAGAAATGAAGTTCTCTTGGTCACATCCTGAAAGTGACCAGCTCCCTGTGGCCCCGGCAG
AATCTCAGCCTGAGGACGGTATTGGCTTCGGCAGCTGAGCTCCGAGATACCTCGGAGGGCACGGCAGGGT
AGGGTCCTCCCTCCACGTGCCCCTCGAGCAAATGCCTCGCAGCCCACTTCTCCACCCTCACCTGAGGACC
GCAGCTTCCAGTGTTTTGTTGAGTACATCAAGTCCTGGGTGACCTGCGGTCACAGGGTGCCCCACGCTGC
CTGCCTGTGGCAAATGCCCCATGGCACCCTGAGGAAGGCATGGCTGCTGCCACGGTGGGCCAGACCCCTG
TCCCCGGGCTTCATGACAGCCTCCATAGTCAGGAAATGGGGCAGGCACTGGTGACAGGCCCTGGAAAGAC
GTACCGGGGGTACCCGTTCAGCCTCCTGCCATGGCACCACCCAGGGCATTGAAGTCCTGTATGTCCACAC
CCAGTGTGGGGCACCCTTCCTCAACCTGGGCCCAGCTCGGCTGAGGGGGTGAGGGCGTGACCTGGGGCTG
GCGGGCAGGCGGGCACCATCTCTCCCTGACTGTGCCATCCTGCGTGCCTCTTCCTCGCCGCTGTTCCGGA
CCTGCTCTGCGTGGCTCGCCCTGGCAGTGGGGCAGGTGGAGCTGGGTGGGGGCTCTATCACGGGCAGCCT
GCCACCCTTGGAGGGTCCCATGCAGAAGCGTGGCGTCGTGGATCAGTGCTGCACCAGCATCTGCTCCCTC
TACCAGCTGCAGAACTACTGCAACTAGACTGGGCCCACAGCGACCCCGTGCCCACTGCCACCTGCACCAG
CACCTGCTCCCTCTACCAGCTGGAGAACCACAGCTGGCTGCGGCCCACAGCAGGCCCAAATGCGGCCCTG
CACCCTCCTCACCTGCACATGAGTGATGGAATAAAGCCTTGAACCAGCTCTGCTGTGCTGTTTGCGTGTT
TGGGGGGCCCTGGGCAGACCCCGCCGTCCTGGCACTGTTATGAGCCCCTCCCAGCTCTCTCCAAGCTCTC
GCCCGGCCTGCAG

>J02989.1:CDS Owl monkey (A.trivirgatus) insulin gene, complete cds
ATGGCCCTGTGGATGCACCTCCTGCCCCTGCTGGCGCTGCTGGCCCTCTGGGGACCCGAGCCAGCCCCGG
CCTTTGTGAACCAGCACCTGTGCGGCCCCCACCTGGTGGAAGCCCTCTACCTGGTGTGCGGGGAGCGAGG
TTTCTTCTACGCACCCAAGACCCGCCGGGAGGCGGAGGACCTGCAGGTGGGGCAGGTGGAGCTGGGTGGG
GGCTCTATCACGGGCAGCCTGCCACCCTTGGAGGGTCCCATGCAGAAGCGTGGCGTCGTGGATCAGTGCT
GCACCAGCATCTGCTCCCTCTACCAGCTGCAGAACTACTGCAACTAG
```

Korzystając z internetowej wersji programów **Needle** i **Water** (<a href="http://www.ebi.ac.uk/Tools/psa/">http://www.ebi.ac.uk/Tools/psa/</a>) wykonaj - w dwóch kartach przeglądarki - przyrównanie powyższych sekwencji.

1. Z ilu egzonów składa się badany gen insuliny?
2. Podaj pozycję początku i końca egzonów na sekwencji genomowej.
3. Podaj procent identyczności dwóch przyrównań.
   * Dlaczego procent identyczności przyrównania w programie Needle jest niższy niż w water?
<br/><br/>


### Zad. 4 - Przyrównanie lokalne i semi-globalne sekwencji aminokwasowych
Poniżej znajdują się dwie sekwencje prokariotycznych proteaz serynowych pobrane z bazy UniProt.
Pierwsza jest termostabilną proteazą pochodzącą z *Bacillus lentus*, którą firma *Novozymes* dodaje do proszków do prania pod nazwą *Savinase*. Druga sekwencja jest również termostabilną proteazą serynową pochodzącą z inne gatunku *Bacillus halodurans*.

```
>P29600 SUBS_BACLE Subtilisin Savinase - Bacillus lentus
AQSVPWGISRVQAPAAHNRGLTGSGVKVAVLDTGISTHPDLNIRGGASFVPGEPSTQDGN
GHGTHVAGTIAALNNSIGVLGVAPSAELYAVKVLGASGSGSVSSIAQGLEWAGNNGMHVA
NLSLGSPSPSATLEQAVNSATSRGVLVVAASGNSGAGSISYPARYANAMAVGATDQNNNR
ASFSQYGAGLDIVAPGVNVQSTYPGSTYASLNGTSMATPHVAGAAALVKQKNPSWSNVQI
RNHLKNTATSLGSTNLYGSGLVNAEAATR

>P41363 ELYA_BACHD Thermostable alkaline protease precursor - Bacillus halodurans
MRQSLKVMVLSTVALLFMANPAAASEEKKEYLIVVEPEEVSAQSVEESYDVDVIHEFEEI
PVIHAELTKKELKKLKKDPNVKAIEKNAEVTISQTVPWGISFINTQQAHNRGIFGNGARV
AVLDTGIASHPDLRIAGGASFISSEPSYHDNNGHGTHVAGTIAALNNSIGVLGVAPSADL
YAVKVLDRNGSGSLASVAQGIEWAINNNMHIINMSLGSTSGSSTLELAVNRANNAGILLV
GAAGNTGRQGVNYPARYSGVMAVAAVDQNGQRASFSTYGPEIEISAPGVNVNSTYTGNRY
VSLSGTSMATPHVAGVAALVKSRYPSYTNNQIRQRINQTATYLGSPSLYGNGLVHAGRAT
Q
```

#### Przyrównanie semi-globalne (Needle)

Korzystając z programu *Needle* przeprowadź semi-globalne przyrównanie obu sekwencji.
1. Podaj wartość punktacji przyrównania (`Score`).
2. Podaj długość przyrównania.
3. Podaj procent identyczności sekwencji.
4. Podaj procent podobieństwa sekwencji.

#### Przyrównanie lokalne (Water)

W nowej karcie przeglądarki skorzystaj z programu *Water* w celu przyrównania obu sekwencji.

5. Czy któreś z dwóch przyrównań jest bardziej poprawnego od drugiego?

#### Interpretacja wyników

Odszukaj dwa rekordy w bazie UniProt.

6. W jaki sposób otrzymano te dwa rekordy?
7. Podaj subkomórkową lokalizację obu białek.
8. Czy oba białka różnią się pod względem post-translacyjnych modyfikacji (`PTM / Processing`)?
9. Czy białko (`P41363`) może posłużyć jako enzym stosowany w proszkach do prania?
<br/><br/>


### Zad. 5 - Przyrównanie daleko spokrewnionych sekwencji (wątpliwe przyrównania)
Poniżej znajduje się sekwencja peptydazy człowieka (tripeptydylo-peptydaza).

```
>P29144 TPP2_HUMAN Tripeptidyl-peptidase 2 
MATAATEEPFPFHGLLPKKETGAASFLCRYPEYDGRGVLIAVLDTGVDPGAPGMQVTTDG
KPKIVDIIDTTGSGDVNTATEVEPKDGEIVGLSGRVLKIPASWTNPSGKYHIGIKNGYDF
YPKALKERIQKERKEKIWDPVHRVALAEACRKQEEFDVANNGSSQANKLIKEELQSQVEL
LNSFEKKYSDPGPVYDCLVWHDGEVWRACIDSNEDGDLSKSTVLRNYKEAQEYGSFGTAE
MLNYSVNIYDDGNLLSIVTSGGAHGTHVASIAAGHFPEEPERNGVAPGAQILSIKIGDTR
LSTMETGTGLIRAMIEVINHKCDLVNYSYGEATHWPNSGRICEVINEAVWKHNIIYVSSA
GNNGPCLSTVGCPGGTTSSVIGVGAYVSPDMMVAEYSLREKLPANQYTWSSRGPSADGAL
GVSISAPGGAIASVPNWTLRGTQLMNGTSMSSPNACGGIALILSGLKANNIDYTVHSVRR
ALENTAVKADNIEVFAQGHGIIQVDKAYDYLVQNTSFANKLGFTVTVGNNRGIYLRDPVQ
VAAPSDHGVGIEPVFPENTENSEKISLQLHLALTSNSSWVQCPSHLELMNQCRHINIRVD
PRGLREGLHYTEVCGYDIASPNAGPLFRVPITAVIAAKVNESSHYDLAFTDVHFKPGQIR
RHFIEVPEGATWAEVTVCSCSSEVSAKFVLHAVQLVKQRAYRSHEFYKFCSLPEKGTLTE
AFPVLGGKAIEFCIARWWASLSDVNIDYTISFHGIVCTAPQLNIHASEGINRFDVQSSLK
YEDLAPCITLKNWVQTLRPVSAKTKPLGSRDVLPNNRQLYEMVLTYNFHQPKSGEVTPSC
PLLCELLYESEFDSQLWIIFDQNKRQMGSGDAYPHQYSLKLEKGDYTIRLQIRHEQISDL
ERLKDLPFIVSHRLSNTLSLDIHENHSFALLGKKKSSNLTLPPKYNQPFFVTSLPDDKIP
KGAGPGCYLAGSLTLSKTELGKKADVIPVHYYLIPPPTKTKNGSKDKEKDSEKEKDLKEE
FTEALRDLKIQWMTKLDSSDIYNELKETYPNYLPLYVARLHQLDAEKERMKRLNEIVDAA
NAVISHIDQTALAVYIAMKTDPRPDAATIKNDMDKQKSTLVDALCRKGCALADHLLHTQA
QDGAISTDAEGKEEEGESPLDSLAETFWETTKWTDLFDNKVLTFAYKHALVNKMYGRGLK
FATKLVEEKPTKENWKNCIQLMKLLGWTHCASFTENWLPIMYPPDYCVF
```

W trzech kartach przeglądarki internetowej porównaj powyższą sekwencję człowieka z sekwencją *Savinase* (`P29600`) stosując:

* Przyrównanie semi-globalne (*Needle*).
* Przyrównanie globalne (*Needle*)
  - W formularzu programu włącz karę za wprowadzenie przerw na końcu przyrównania: `More options` > `END GAP PENALTY` > `true`.
* Przyrównanie lokalne (*Water*)

1. Które z trzech przyrównań najlepiej przedstawia podobne fragmenty sekwencji `P29600` i `P29144`?
2. Czy można odpowiedzieć na pytanie, czy obie sekwencje są ze sobą spokrewnione?

#### Istotność przyrównania

* Otwórz program [ShuffleProtein](http://www.bioinformatics.org/sms2/shuffle_protein.html).
* Umieść w oknie tekstowym sekwencję tripeptydylo-peptydazę człowieka. 
* Wygeneruj losową sekwencję. 
* Przyrównaj wygenerowaną sekwencję z sekwencją *Savinase* korzystając z programu *Water*.
* Powtórz powyższą procedurę dwukrotnie.

3. Jaki zakres wartości punktacji, identyczności i podobieństwa przyjmują te trzy przyrównania?
4. Porównując te przyrównania z oryginalnym przyrównaniem - czy oba białka są spokrewnione?
<br/><br/>

## Wpływ parametrów na przyrównanie sekwencji

### Zad. 6 - Kara za stosowanie przerw
Używając programu *Water* przyrównaj sekwencję *Savinase* z sekwencją tripeptydylo-peptydazę człowieka: 

1. Zmniejszając karę za otwarcie przerwy = `1` i wydłużenie przerwy = `0.2`. 
   * W jaki sposób zmniejszenie kar za otwarcie przerw wpłynęło na to dopasowanie?
2. Zwiększając kary za stosowanie przerw: otwarcie przerwy = `20`, wydłużenie przerwy = `1`.
   * W jaki sposób zwiększenie kar za stosowanie przerw wpłynęło na to dopasowanie?
<br/><br/>

### Zad. 7 - Macierze substytucji
Używając programu Water wykonaj dwa przyrównania sekwencji *Savinase* z sekwencją tripeptydylo-peptydazę człowieka, stosując macierz substytucji `BLOSUM30` i `BLOSUM90`.

Jak zmienia się długość przyrównania i procent identyczności w zależności od macierzy BLOSUM?
<br/><br/>

## Porównane sekwencji: wykres Dot Plot

### Zad. 8
W pliku [dotplot.fasta](./day1/data/dotplot.fasta) znajduje się 10 sekwencji nukleotydowych. Przy wykorzystaniu programu *dotmatcher* (<a href="http://www.bioinformatics.nl/cgi-bin/emboss/dotmatcher">http://www.bioinformatics.nl/cgi-bin/emboss/dotmatcher</a>) wykonaj analizy dot-plot dla podanych poniżej par sekwencji. 
> W polu `Matrix file` wpisz nazwę macierzy `EDNASIMPLE` (`+1` dla par nukleotdów zgodnych, `0` dla niezgodnych). W panelu `Additional section` wpisz długość słowa i wartość graniczną odpowiednio `15` i `10`.

1. s1:s1
2. s1:s10
3. s2:s2
4. s4:s5
5. s7:s8
6. s4:s4
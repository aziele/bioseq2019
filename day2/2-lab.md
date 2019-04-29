## BLAST - zaawansowane zagadnienia

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
2. Spójrz na przyrównanie tych sekwencji. Jak brzmi ukryta wiadomość?
3. Co oznaczają fragmenty dopasowania oznaczone małymi szarymi literami?
<br/><br/>


### Zad. 2 - Złożone przeszukiwanie blastx
W bazie nukleotydowej NCBI wyszukaj rekord sekwencji *EST* węża koralowego o numerze dostępu `FL590802`. W panelu `Analyze this sequence` po prawej stronie rekordu naciśnij `Run BLAST`. Wybierz program `blastx`, bazę sekwencji `UniProtKB/Swiss-Prot(swissprot)` i rozpocznij przeszukiwanie.

1. Czy sekwencja zapytania została dopasowana na całej długości do sekwencji białek?
2. Jakiego typu sekwencje białkowe zostały przyrównane do sekwencji zapytania?

### Najwyżej punktowane przyrównanie

Z listy otrzymanych trafień zidentyfikuj sekwencję, która uzyskała najwyższą wartość punktacji (`Max score`). Odpowiedz na poniższe pytania dotyczące tej sekwencji:

3. W której ramce odczytu została przetłumaczona sekwencja zapytania?
4. Podaj długość pełnej sekwencji zapytania oraz jej początek i koniec w przyrównaniu.
5. Podaj długość pełnej sekwencji trafienia oraz jej początek i koniec w przyrównaniu.
6. Dlaczego aminokwasowa sekwencja trafienia nie została przyrównana przez program blastx w pozycji `1-18`?
7. Czy liczba reszt cysteiny w sekwencji zapytania odpowiada liczbie cystein w sekwencji trafienia?
<br/><br/>


### Zad. 3 - Identyfikacja ortologów (*Reciprocal BLAST*)
> Celem zadania jest znalezienie sekwencji białkowej rekina, ortologicznej do białka opsyny-5 człowieka (`NP_859528`).

Opsyny są światłoczułymi białkami występującymi u zwierząt i pełnią kluczowe funkcje w procesie widzenia. Białka te absorbują światła o różnej długości fali (np. czerwone, niebieskie, zielone); mutacje w genach kodujących opsyny wywołują ślepotę różnych kolorów. Rodzina białek opsynowych składa się z wielu białek o podobnych nazwach: u człowieka występuje pięć grup opsyn (1-5), rodopsyna i peropsyna. Nazwy tych białek niekoniecznie odpowiadają nazwom opsyn u innych gatunków. Dlatego identyfikacja ortologów tych genów u odgrywa kluczową rolę w ich klasyfikacji.

#### BLAST w jednym kierunku
W serwisie [NCBI BLAST](https://blast.ncbi.nlm.nih.gov/) przeszukaj wszystkie białkowe sekwencje rekina *Scyliorhinus canicula* stosując jako zapytanie numer dostępu opsyny-5 człowieka (`NP_859528`).

1. Czy zidentyfikowana sekwencja białkowa rekina jest opsyną-5?

#### BLAST w drugim kierunku
Przeprowadź wyszukiwania BLAST stosując jako zapytanie zidentyfikowaną sekwencję rekina i bazę danych sekwencji człowieka pochodzących z bazy *RefSeq*.

2. Czy zidentyfikowana sekwencja białkowa rekina jest opsyną-5?



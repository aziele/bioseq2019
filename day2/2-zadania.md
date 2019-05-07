### Zad. 1 - Identyfikacja przesunięcia ramki odczytu

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

### Zad. 2 - Identyfikacja ortologów
Główne białko moczu (*MUP*, *major urinary protein*) zwierząt bierze udział w wywoływanie strachu między różnymi gatunkami zwierząt. Na przykład, myszy wyczuwają i boją się zapachu białek MUP szczurów i kotów.

Celem zadania jest znalezienie sekwencji u oposa ortologicznej do białka MUP3 myszy.

1. Znajdź w bazie RefSeq sekwencję białka MUP3 myszy i uruchom program **blastp** w celu przeszukania bazy `nr` sekwencji oposa (*Monodelphis domestica*). 
2. W wynikach programu BLAST, zidentyfikuj jedną lub więcej sekwencji oposa, które mogą być ortologami MUP3 myszy.
3. Uruchom program BLAST w odwrotnym kierunku: organizm `Mus musculus` i baza `RefSeq`.
4. Na postawie wyników programu BLAST, zidentyfikuj sekwencję ortologiczną.

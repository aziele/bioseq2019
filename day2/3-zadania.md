### Zad. 1 - Przyrównanie rodziny białkowej
W pliku [x-protein.fasta](./data/x-protein.fasta) znajdują się sekwencje aminokwasowe białek należących do jednej rodziny. Wykonaj przyrównanie tych sekwencji korzystając z internetowych programów [ClustalOmega](https://www.ebi.ac.uk/Tools/msa/clustalo/) i [MAFFT](https://www.ebi.ac.uk/Tools/msa/mafft/). W formularzu obu programów zaznacz opcję, aby kolejność sekwencji w przyrównania odpowiadała kolejności sekwencji w pliku z sekwencjami FASTA (`MORE OPTIONS` > `ORDER` > `INPUT`).

1. Czy oba programy generują takie same przyrównania?
2. Podaj najdłuższy fragment sekwencji o nieprzerwanej 100% identyczności.
<br/><br/>

### Zad. 2 - Przyrównanie sekwencji CDS w oparciu o sekwencje białkowe
> Celem zadania jest wykorzystanie informacji zawartej w sekwencjach białkowych insuliny do utworzenia prawidłowego przyrównania odpowiadających sekwencji CDS.

W pliku [insulin.cds.clean.fasta](./data/insulin.cds.clean.fasta) znajdują się sekwencje CDS insuliny. Otwórz program [RevTrans](http://www.cbs.dtu.dk/services/RevTrans-2.0/web/). Umieść sekwencje CDS w polu `Paste in DNA sequences` i wykonaj przyrównanie.

1. Czy liczba przerw w przyrównaniu jest zawsze podzielna przez 3?
2. Czy wszystkie kodony zostały przyrównane? (pierwsza pozycja kodonu powinna być w tej samej kolumnie co pozostałe pierwsze pozycje kodonu w innych sekwencjach)
<br/><br/>

### Zad. 3 - Miejsca akceptorowe egzonu
W pliku [acceptor.fasta](./data/acceptor.fasta) znajduje się 100 sekwencji wyodrębnionych z genów człowieka w miejscu intron/egzon. Wykonaj logo tych sekwencji.



### Zad. 1
W pliku [insulin.cds.fasta](./data/insulin.cds.fasta) znajdują się sekwencje CDS insuliny różnych organizmów.

#### Przyrównanie na poziomie DNA
Wykonaj przyrównanie sekwencji CDS korzystając z programu [EMBOSS MAFFT](https://www.ebi.ac.uk/Tools/msa/).

1. Czy w przyrównaniu występują przerwy, których liczba nie jest podzielna przez trzy? Przerwy takie nie odpowiadają liczbie całych kodonów.

2. Która sekwencja wydaje się najmniej podobna do pozostałych sekwencji? (łatwe do zobaczenia w JalView)
   * Czy ma to sens taksonomiczny? (Wskazówka: czy wszystkie sekwencje należą do kręgowców?)

3. Zwróć uwagę na drzewo wiodące (`Guide Tree`) na stronie przyrównania programem MAFFT. Czy wśród sekwencji występują takie, które są identyczne?


#### Przyrównanie sekwencji białkowych
Przy użyciu programu [EMBOSS Transeq](https://www.ebi.ac.uk/Tools/st/emboss_transeq/) dokonaj translacji sekwencji CDS insuliny na sekwencje białkowe. Wykonaj przyrównanie otrzymanych sekwencji aminokwasowych.

4. Czy przyrównanie sekwencji białkowych odpowiada przyrównaniu sekwencji CDS?
5. Które sekwencje białkowe są identyczne?


## Zad. 2
W pliku [acceptor.fasta](./data/acceptor.fasta) znajduje się 100 sekwencji wyodrębnionych z genów człowieka w miejscu intron/egzon. Wykonaj logo tych sekwencji.



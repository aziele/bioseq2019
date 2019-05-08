### Zad. 1 - Badanie pokrewieństwa niedźwiedzi

W pliku [bears.fasta](http://www.combio.pl/files/bears.fasta) znajdują się sekwencje 12s rRNA (niekodujące białka) pochodzące z 7 gatunków niedźwiedzi i 4 gatunków innych kręgowców:

1. American Black bear
2. American Brown bear
3. Asiatic Black bear
4. Spectacled bear
5. Polar bear
6. Giant panda
7. Red panda
8. Dog
9. Racoon
10. Crocodile skink
11. Cow

Przeprowadź analizę filogenetyczną powyższych sekwencji.

1. Które niedźwiedzie są ze sobą bardziej spokrewnione: 
   * American Black - Asia Black Bear 
   * Spectacled Bear - Polar Bear?

2. Czy panda wielka jest bardziej spokrewniona z niedźwiedziami amerykańskimi czy azjatyckimi?

3. Czy `Red Panda` jest w ogóle niedźwiedziem?

4. Który z niedźwiedzi jest najstarszy?
<br/><br/>

### Zad. 2 - Wymarły niedźwiedź jaskiniowy
Sekwencje z poprzedniego zadania należą do żyjących gatunków niedźwiedzi. Niedźwiedź jaskiniowy (*Ursus spelaeus*) wymarł ok. 20 tys. lat temu. Użyj serwisu [NCBI BLAST](https://blast.ncbi.nlm.nih.gov/Blast.cgi) i znajdź sekwencję 12s rRNA niedźwiedzia jaskiniowego, dołącz ją do sekwencji pozostałych niedźwiedzi w pliku [bears.fasta](http://www.combio.pl/files/bears.fasta) i zbuduj drzewo filogenetyczne.

1. Który niedźwiedź jest najbliższym krewnym wymarłego niedźwiedzia jaskiniowego?
2. Czy uwzględnienie niedźwiedzia jaskiniowego na drzewie zmieniło układ pozostałych taksonów?
<br/><br/>

### Zad. 3 - Drzewo gatunków: analiza mitochondrialnego DNA
Plik [mito.fasta](http://www.combio.pl/files/mito.fasta) zawiera dopasowanie sekwencji mitochondrialnego DNA (niekodującego białko) pochodzące z człowiekokształtnych i innych naczelnych. Korzystając z programu MEGA utwórz drzewa filogenetyczne opisujące relacje między tymi sekwencjami używając 4 metod filogenetycznych z analizą bootstrap (`50` pseudoreplikacji):

1. Neighbor-Joining, 
2. Maximum Likelihood (potrwa ok. 3 min)
3. Minimum Evolution
4. Maximum Parsimony

---

1. Czy topologie drzew uzyskane czterema metodami znacznie się różnią?
2. Które węzły są najbardziej wiarygodne (100% bootstrap) we wszystkich drzewach?
3. Która para współczesnych ludzi jest ze sobą najbliżej spokrewniona?
4. Jaki gatunek naczelnych (inny niż neandertalczyk) jest najbliżej spokrewniony z współczesnym człowiekiem?
5. Jaki typ współczesnego człowieka jest najbliżej spokrewniony z korzeniem drzewa?
6. Czy topologia drzewa potwierdza teorię "Wyjścia z Afryki" (*Out of Africa Theory*)?

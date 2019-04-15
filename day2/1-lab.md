## Wyszukiwanie sekwencji podobnych (BLAST)

### Zad. 1 - Opis wyników programu BLAST
Poniżej znajduje się sekwencja mRNA insuliny gryzonia koszatniczki pospolitej (*Octodon degus*).

```
>M57671.1 Octodon degus insulin mRNA, complete cds
GCATTCTGAGGCATTCTCTAACAGGTTCTCGACCCTCCGCCATGGCCCCGTGGATGCATCTCCTCACCGT
GCTGGCCCTGCTGGCCCTCTGGGGACCCAACTCTGTTCAGGCCTATTCCAGCCAGCACCTGTGCGGCTCC
AACCTAGTGGAGGCACTGTACATGACATGTGGACGGAGTGGCTTCTATAGACCCCACGACCGCCGAGAGC
TGGAGGACCTCCAGGTGGAGCAGGCAGAACTGGGTCTGGAGGCAGGCGGCCTGCAGCCTTCGGCCCTGGA
GATGATTCTGCAGAAGCGCGGCATTGTGGATCAGTGCTGTAATAACATTTGCACATTTAACCAGCTGCAG
AACTACTGCAATGTCCCTTAGACACCTGCCTTGGGCCTGGCCTGCTGCTCTGCCCTGGCAACCAATAAAC
CCCTTGAATGAG
```

Ze strony serwisu [NCBI](https://www.ncbi.nlm.nih.gov) otwórz stronę programu `BLAST`. Wybierz program `Nucleotide BLAST`. W formularzu:

* W polu `Enter Query Sequence` umieść powyższą sekwencje w formacie FASTA
* W panelu  `Program Selection` wybierz `Somewhat similar sequences (blastn)`
* Uruchom program BLAST.

#### Odczytywanie wyników
Z listy otrzymanych trafień (panel *Descriptions*) zwróć uwagę na sekwencję, która uzyskała najwyższą wartość punktacji (`Max score`). Odpowiedz na poniższe pytania dotyczące tej sekwencji:

1. Jaki jest numer dostępu sekwencji?
2. Ile wynosi wartość punktacji `Max score`?
   * O czym informuje ten parametr?
3. Ile wynosi wartość punktacji `Total score`?
   * O czym informauje ten parametr?
4. Ile wynosi procent identyczności między sekwencją zapytania?
5. Ile wynosi wartość `Query cover`?
   * O czym informuje ten parametr?
6. Ile wynosi wartość `E-value`?
   * O czym informuje ten parametr?
7. Ile przerw wprowadzono w tym przyrównaniu?
8. Ile wynosi długość przyrównania?

Na liście otrzymanych trafień znajdź najwyżej punktowaną sekwencję insuliny człowieka (*Homo sapiens*), która nie jest syntetycznym konstruktem.

9. Odpowiedz na te same pytania 1-8 na temat przyrównania z sekwencją człowieka.

### Zad. 2 - Wielkość bazy danych i E-value
Przeprowadź ponowne przeszukiwanie programem BLAST stosując jako zapytanie mRNA insuliny koszatniczki pospolitej `M57671.1`. W formularzu:

* Ogranicz przeszukiwanie do organizmu człowieka
* W panelu  `Program Selection` wybierz `Somewhat similar sequences (blastn)`
* Uruchom program BLAST.

1. Czy w wynikach znalezione zostałe sekwencje człowieka z poprzedniego zadania?
2. Czy wartości parametrów punktacji, identyczności, E-value są takie same jak w poprzednim zadaniu?
3. Jaka jest wielkość (w liczbie nukleotydów) przeszukiwanej bazy danych użytej w tym i poprzednim zadaniu? 
   > `Search summary` > `Number of letters`
4. Ile wynosi stosunek wielkości obu baz danych?
5. Ile wynosi stosunek E-value uzyskanych w dwóch przeszukiwaniach?
6. Jaka jest zależność między wielkością bazy danych a wartością E-value dla przyrównań o takiej samej wartości punktacji?
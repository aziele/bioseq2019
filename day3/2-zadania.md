### Zad. 1 - PSI-BLAST: szukanie odległych sekwencji homologicznych
> Celem zadania jest sprawdzenie, czy białko człowieka (o numerze dostępu w bazie UniProt: `GPAA1_HUMAN`) ma sekwencje homologiczne w rodzaju *Trypansomoma*.

#### Standardowe przeszukiwanie BLAST
Przeprowadź standardowe przeszukiwanie programem `protein BLAST`, zawężając wyszukiwania do organizmu *Trypanosoma*.

1. Ile znaleziono sekwencji statystycznie istotnych (`E-value < 0.005`)?
   * Ile wynosi E-value najlepszego trafienia?

#### Wyszukiwanie PSI-BLAST
Przeprowadź wyszukiwanie programem PSI-BLAST we wszstkich organizmach w celu zbudowania profilu PSSM. Następnie używając profilu PSSM przeszukaj bazę danych `nr` z ograniczeniem do rodzaju *Trypanosoma*.

2. Ile znaleziono sekwencji statystycznie istotnych (`E-value < 0.005`)?
   * Ile wynosi E-value najlepszego trafienia?
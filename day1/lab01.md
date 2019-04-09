## Przeszukiwanie bazy Genbank i RefSeq

### Standardowe wyszukiwanie

W nukleotydowej bazie NCBI (`nucleotide`) wyszukaj wszystkie sekwencje insuliny.

```
Rozwiązanie:
Search details: insulin[All Fields]; 202 048 rekordów
```

Zawęź wyszukiwania do ogranizmu człowieka.

```
Rozwiązanie:
Filters > Homo sapiens (11078)
Search details: insulin[All Fields] AND "Homo sapiens"[porgn]
```

Zawęź wyszukiwania do sekwencji mRNA.

```
Rozwiązanie:
Filters > Molecule type > mRNA (6357)
insulin[All Fields] AND "Homo sapiens"[porgn] AND biomol_mrna[PROP]
```

### Zaawansowane wyszukiwanie
Korzystając z zaawansowanego wyszukiwania (`Advanced`) skonstruuj zapytanie do bazy danych pozwalające wyszukać wszystkie sekwencje insuliny człowieka.

```
Rozwiązanie:
insulin[All Fields] AND "Homo sapiens"[Organism] (11 193)
```

Zawęź wyszukiwania do sekwencji mRNA.

```
Rozwiązanie:
Advanced > History > Add previous query > Filter > mRN > Index preview > mRNA
(insulin[All Fields] AND "Homo sapiens"[Organism]) AND "mrna"[Filter] (6357)
```

Zawęź wyszukiwania, aby w rekordach nie występowały frazy `insulin-like` i `partial`

```
Rozwiązanie:
(((insulin[All Fields] AND "Homo sapiens"[Organism]) AND "mrna"[Filter]) NOT insulin-like[All Fields]) NOT partial[All Fields] (5047)
```
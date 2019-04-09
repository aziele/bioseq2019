## Przeszukiwanie bazy Genbank i RefSeq

### Klasyczne wyszukiwanie

1. W nukleotydowej bazie NCBI (`nucleotide`) wyszukaj wszystkie sekwencje insuliny.
2. Zawęź wyszukiwania do ogranizmu człowieka.
3. Zawęź wyszukiwania do sekwencji mRNA.

### Zaawansowane wyszukiwanie

Korzystając z zaawansowanego wyszukiwania (`Advanced`) skonstruuj zapytanie do bazy danych pozwalające wyszukać wszystkie sekwencje insuliny:

4. człowieka
5. człowieka uzwględniając tylko sekwencje mRNA
6. człowieka uwzględniając tylko sekwencje mRNA i wykluczając frazy `insulin-like` i `partial`



## Rozwiązania:

```
1. Search details: insulin[All Fields]; 202 048 rekordów

2. Filters > Homo sapiens (11078)
   Search details: insulin[All Fields] AND "Homo sapiens"[porgn]

3. Filters > Molecule type > mRNA (6357)
   insulin[All Fields] AND "Homo sapiens"[porgn] AND biomol_mrna[PROP]

4. insulin[All Fields] AND "Homo sapiens"[Organism] (11 193)

5. Advanced > History > Add previous query > Filter > mRN > Index preview > mRNA
   (insulin[All Fields] AND "Homo sapiens"[Organism]) AND "mrna"[Filter] (6357)

6. (((insulin[All Fields] AND "Homo sapiens"[Organism]) AND "mrna"[Filter]) NOT insulin-like[All Fields]) NOT partial[All Fields] (5047)
```
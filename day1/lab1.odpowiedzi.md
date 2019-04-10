### Zad. 1
1. 202 048 rekordów 
   *Search details:*

   ```
   insulin[All Fields]; 202 048 rekordów
   ```

2. Filters > *Homo sapiens* (11 078)
   *Search details:*

   ```
   insulin[All Fields] AND "Homo sapiens"[porgn]
   ```

3. Filters > Molecule type > mRNA (6 357 rekordów)
   *Search details:*

   ```
   insulin[All Fields] AND "Homo sapiens"[porgn] AND biomol_mrna[PROP]
   ```

4. Advanced search (11 193 rekordów).
   *Search details:*

   ```
   insulin[All Fields] AND "Homo sapiens"[Organism] (11 193 rekordów)
   ```

5. Advanced > History > Add previous query > Filter > mRN > Index preview > mRNA (6 357 rekordów)
   *Search details:*
   ```
   (insulin[All Fields] AND "Homo sapiens"[Organism]) AND "mrna"[Filter] 
   ```

6. Advanced search (5 047 rekordów)
   *Search details*

   ```
   insulin[All Fields] AND "Homo sapiens"[Organism] AND "mrna"[Filter] 
   NOT (insulin-like[All Fields] OR partial[All Fields])
   ```

   lub 

   ```
   insulin[All Fields] AND "Homo sapiens"[Organism] AND "mrna"[Filter] 
   NOT insulin-like[All Fields] NOT partial[All Fields]
   ```


### Zad. 2
Advanced search (1 rekord)

```
((BRCA2[Gene Name]) AND Homo sapiens[Organism]) AND "refseq"[Filter]
```

1. Długość białka: `3418` aa
2. Numer dostępu białka `NP_000050`
3. Numer dostępu z aktualną wersją: `NP_000050.2`.
   > Pokazać, że można przejść do poprzedniej wersji rekordu `NP_000050.1`.
4. Numer dostępu mRNA: `NM_000059.3`
5. Identyfikator genu (*Gene ID*): `675` [link](https://www.ncbi.nlm.nih.gov/gene/675)
   > Przejść do rekordu genu.
6. Synonimy genu BRCA2: `FAD`, `FACD`, `FAD1`, itd.
7. Liczba egzonów: `27`
8. Lokalizacja genu na genomie: chromosom 13 NC_000013.11 (32315480..32399672), nić plus
9. Udjąć 1000 od statu genu i dodać 1000 do końca genu.
10. Gen BRCA2 ma jeden wariant splicingowy.


### Zad. 3
Zadanie na podstawie: https://www.youtube.com/watch?v=zs46Ur0m0mc
Baza danych: `Gene`. Advanced search.

```
HFE[Gene Name] AND Homo sapiens[Organism]
```

1. GeneID: `3077` [link](https://www.ncbi.nlm.nih.gov/gene/3077)
2. Gen ma 11 wariantów splicingowych kodujących białka:
   * 10 ma numery NM/NP
   * 1 ma `XM/XP`
   Gen ma również RNA ([XR_002957972.1](https://www.ncbi.nlm.nih.gov/nucleotide/XR_002957972))
3. Spójrz na graficzną reprezentację wariantów splicingowych w części *Genomic regions, transcripts, and products*. Ustaw `Genomic Sequence` na `NG_008720.2 RefSeqGene`. Prawy przycisk myszy > Set New Marker at Position > 8671 i Lock marker. Pojawi się linia wyznaczająca miejsce w sekwencji genomowej genu, transkryptów i białek. Kliknij prawym przyciskiem na markerk i wybierz `Marker details`. Otworzy się okienko z dokładną lokalizacją markera względem genu, transkryptów, CDS i białek.


### Zad. 3
- Zadanie na podstawie: https://www.youtube.com/watch?v=sK3ykyInU8o
- Taxonomy > wpisać `mouse`. Wybrać *Mus musculus*. 
  - Subtree links = wszystkie dane wraz z podgatunkami,
  - Direct links = bezpośrednio podłączone pod taxonomy ID (Mus musculus bez jawnego podłączenia pod podgatunki.)

1. 6 194 struktur białkowych (`Structure`)
2. 1 genom (`Genome`)


### Zad. 4
Taxonomy > wpisać `rodentia` lub `rodents`.

1. 
2. `6` levels, przycisk `Display`.
3. using filter `has genome sequences`.
4. Zazaczyć `protein` i nacisnąć przycisk `Display`.
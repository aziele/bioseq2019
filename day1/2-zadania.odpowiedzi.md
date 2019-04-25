### Zad. 1
Otwórz stronę serwisu [UniProt](https://www.uniprot.org). Użyj zaawansowanego wyszukiwania i skonstruuj poniższe zapytanie:

```
organism:"Neisseria gonorrhoeae [485]"
```

1. W wyniku otrzymano **12 711** rekordów białek:
   * `137` rekordów należy do bazy *SwissProt*
   * `12 574` rekordów należy do bazy *trEMBL*

2. W wyniku uwzględnienia wszystkich niższych jednostek taksonomicznych (podgatunków) *N. gonorrhoeae* otrzymano **24 248** białek:
   * `807` rekordów należy do bazy *SwissProt*
   * `23 441` rekordów należy do bazy *trEMBL* 
<br/><br/>


### Zad. 2
Otwórz stronę serwisu [UniProt](https://www.uniprot.org). Użyj zaawansowanego wyszukiwania i skonstruuj poniższe zapytanie: 

```
existence:"Evidence at protein level [1]" length:[1 TO 10]
```

1. W wyniku otrzymano `1 144` białek z bazy *SwissProt* i `147` białek z bazy *trEMBL*.

2. Korzystając z zaawasnowanego wyszukiwania zmodyfikuj poprzednie zapytanie: 
   > `Advanced` > `Sequence` > `Fragment` > `Sequence complete`

   ```
   existence:"Evidence at protein level [1]" length:[1 TO 10] fragment:no
   ```
   W wyniku otrzymano `783` rekordów z bazy *SwissProt* i `65` rekordów z bazy *trEMBL*.

2. Korzystając z zaawansowanego wyszukiwania zmodyfikuj poprzednie zapytanie: 

   ```
   existence:"Evidence at protein level [1]" length:[1 TO 10] fragment:no 
   AND organism:"Homo sapiens (Human) [9606]"
   ```

   W wyniku otrzymano `6` białek człowieka z bazy *SwissProt*.


#### Zapis sekwencji w formacie FASTA
Naciśnij przycisk `Download` > `Download all` > `Uncompressed` > Przycisk `GO`.

```
>sp|P0DPR3|TRDD1_HUMAN T cell receptor delta diversity 1 OS=Homo sapiens OX=9606 GN=TRDD1 PE=1 SV=1
EI
>sp|P22103|PNEU_HUMAN Pneumadin OS=Homo sapiens OX=9606 PE=1 SV=1
AGEPKLDAGV
>sp|P02728|GLEM_HUMAN Erythrocyte membrane glycopeptide OS=Homo sapiens OX=9606 PE=1 SV=1
CEGHSHDHGA
>sp|P02729|GLUR_HUMAN Urine glycopeptide OS=Homo sapiens OX=9606 PE=1 SV=1
CEHSHDGA
>sp|P01358|GAJU_HUMAN Gastric juice peptide 1 OS=Homo sapiens OX=9606 PE=1 SV=1
LAAGKVEDSD
>sp|P01858|TUFT_HUMAN Phagocytosis-stimulating peptide OS=Homo sapiens OX=9606 PE=1 SV=1
TKPR
```
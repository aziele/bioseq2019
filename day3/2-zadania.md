### Zad. 1 - Identyfikacja domen w serwise InterPro
W serwisie [InterPro](https://www.ebi.ac.uk/interpro/) zidentyfikuj domeny występujące w poniższej sekwencji białkowej:

```
>NP_001157185.1 elongation factor Tu, mitochondrial isoform 2 [Mus musculus]
MAAATLLRATPRFSGLCASPTPFLQGRLRPLKAPASPFLCRGLAVEAKKTYVRDKPHVNVGTIGHVDHGK
TTLTAAITKILAEGGGAKFKKYEEIDNAPEERARGITINAAHVEYSTAARHYAHTDCPGHADYVKNMITG
TAPLDGCILVVAANDGPMPQTREHLLLAKQIGVEHVVVYVNKADAVQDSEMVELVELEIRELLTEFGYKG
EETPVIVGSALCALEQRDPELGVKSVQKLLDAVDTYIPVPTRDLDKPFLLPVESVYSIPGRGTVVTGTLE
RGILKKGDECELLGHNKNIRTVVTGIEMFHKSLERAEAGDNLGALVRGLKREDLRRGLVMVKPGSIQPHQ
KVEAQVRAPVLSGFPCLEAGLVAKPFHPYCFSPLGLYPQQGGRWPPQTLCISFHARHVLPDLGHGLSSHL
ASREGTCHAWRGLEA
```

1. Ile domen białkowych posiada ta sekwencja?
2. W ilu róznych układach domen (architektura domen) występuje domena `Elongation factor Tu (EF-Tu), GTP-binding domain`?
3. W ilu białkach człowieka występuje ta domena?
<br/><br/>

### Zad. 2 - Wyszukiwanie sekwencji wielodomenowych (kinazy WAK)
Kinazy WAK (*Wall associated kinase*) są łącznikami między ścianą komórkową a cytoplazmą i wykazują zdolnośc do wiązania składników ścian komórkowych roślin. Kinazy WAK składają się z domen:
* *GUB_WAK_bind* (`PF13947`) - zewnątrzkomórkowa część białka, która wiążę pektyny ściany komórkowej
* *EGF_CA* (`PF07645`) - epidermalny czynnik wzrostu wiążący jony wapnia
* *Pkinase_Tyr* (`PF07714`) - domena kinazowo

* W serwisie [UniProt](https://www.uniprot.org) wyszukaj wszystkie białka roślin, które posiadają powyższe trzy domeny.

1. Ile białek zidentyfikowano?

* Ogranicz listę zidentyfikowanych białek do rekordów wysokiej jakości (*Reviewed*).

2. Z jakiego organizmu pochodzą te białka?

* Zapisz sekwencje wysokiej jakości w formacie FASTA.
* Wykonaj przyrównanie pobranych sekwencji w programie [MAFFT](https://www.ebi.ac.uk/Tools/msa/mafft/).

3. Podaj najdłuższy fragment w tych sekwencji o nieprzerwanej 100% identyczności.
<br/><br/>

### Zad. 3 - Przyrównanie rodziny białkowej
W pliku [x-protein.fasta](./data/x-protein.fasta) znajdują się sekwencje aminokwasowe białek należących do jednej rodziny. Wykonaj przyrównanie tych sekwencji korzystając z programu [MAFFT](https://www.ebi.ac.uk/Tools/msa/mafft/).

Sekwencją jednego z białek sprawdź czy występuje w nim motyw zawarty w bazie [PROSITE](http://prosite.expasy.org).

1. Jaki to jest motyw? Podaj jego nazwę i identyfikator PROSITE.
2. Jaka jest długość i wzorzec tego motywu?
3. Czy w przyrównaniu sekwencji region tego motywu jest dobrze zachowany?
4. Ile białek pochodzących z *Archaea*, *Bacteria* i *Eukaryota* zawartych w bazie UniProtKB zawiera ten motyw?
<br/><br/>


### Zad. 4 - Białka z domeną rycyny
> Celem zadania jest wyszukanie wszystkich białek zawierających określony zestaw domen.

Białko rycyna (ricin) pochodzące z rącznika pospolitego (*Ricinus communis*) posiada silne
właściwości toksyczne. Dlatego niejednokrotnie wykorzystywane było one przez przestępców,
służby specjalne, a także terrorystów jako broń biologiczna. 

Odszukaj rekord tego białka w bazie [UniProt](https://www.uniprot.org) i wyświetl jego sekwencję w formacie FASTA. Znalezioną sekwencją przeszukaj serwis [Pfam](https://pfam.xfam.org) i zidentyfikuj zawarte w niej domeny. Następnie, skorzystaj z zaawansowanego wyszukiwania serwisu UniProt i wyszukaj w nim wszystkie białka zawierające wszystkie te domeny.


### Zad. 5 - PSI-BLAST: szukanie odległych sekwencji homologicznych
> Celem zadania jest sprawdzenie, czy białko człowieka (o numerze dostępu w bazie UniProt: `GPAA1_HUMAN`) ma sekwencje homologiczne w rodzaju *Trypansomoma*.

#### Standardowe przeszukiwanie BLAST
Przeprowadź standardowe przeszukiwanie programem `protein BLAST`, zawężając wyszukiwania do organizmu *Trypanosoma*.

1. Ile znaleziono sekwencji statystycznie istotnych (`E-value < 0.005`)?
   * Ile wynosi E-value najlepszego trafienia?

#### Wyszukiwanie PSI-BLAST
Przeprowadź wyszukiwanie programem PSI-BLAST we wszstkich organizmach w celu zbudowania profilu PSSM. Następnie używając profilu PSSM przeszukaj bazę danych `nr` z ograniczeniem do rodzaju *Trypanosoma*.

2. Ile znaleziono sekwencji statystycznie istotnych (`E-value < 0.005`)?
   * Ile wynosi E-value najlepszego trafienia?
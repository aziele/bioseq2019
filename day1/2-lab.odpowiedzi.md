## UniProt
Zadania na podstawie: [DTU Course](http://teaching.healthtech.dtu.dk/36611/index.php/Exercise:_The_protein_database_UniProt).

### Zad. 1
1. W wyniku Wpisania frazy `human insulin` znaleziono `1525` rekordów z bazy SwissProt i `3048` rekordów z bazy `trEMBL`.
   * SwissProt zawiera rekordy wysokiej jakości (zweryfikowane przez specjalistów, białka o potwierdzonej funkcji)
   * trEMBL zawiera rekordy o niskiej jakości (niezweryfikowane, białka o niepotwierdzomym występowaniu i funkcji)
2. Tak, na pierwszej stronie listy wyników jest szukane białko (`INS_HUMAN Insulin INS Homo sapiens (Human)`). Na liście znajdują się również białka pochodzące z innych organizmów nie będące insuliną.
3. Wybranie z panelu filtrów organizmu i nazwy białka spowodowało ograniczenie wyników do `199` rekordów człowieka, których nazwa zawiera wyraz `insulin`. Zapytanie do bazy znajduje się w oknie wyszukiwania (`organism:human name:insulin`).
   * Insulina człowieka znajduje się na 7 miejscu na liście znalezionych białek.
4. Dodanie do zapytania frazy `NOT name:protein-like` ograniczyło wyniki do 197 białek, które w nazwie nie mają frazy `protein-like`.
   * Insulina człowieka znajduje się na 7 miejscu na liście znalezionych białek.
5. Zapytanie `organism:human name:insulin NOT name:insulin-like NOT name:receptor` ograniczyło liczbę wyników do 47 białek. 
   * Insulina człowieka znajduje się teraz na pierwszym miejscu listy wyników.


### Zad. 2
Rekord insuliny człowieka: [P01308](https://www.uniprot.org/uniprot/P01308)

1. W lewym panelu (*Display*) wybierz `Publications`. W sumie dla tego białka dostępnych jest 1 050 publikacji. Z tego 1 014 oznaczonych jest jako *Computationally mapped* (są to publikacje automatycznie pobrane z innych baz danych i nie są zweryfikowane przez pracowników UniProt). Natomiast 36 publikacji na temat tego białka insuliny jest zweryfikowanych i dotyczy szczegółowych informacji dotyczących funkcji, sekwencji, struktury, interakcji tego białka.
2. Panelu rekordu `Subcellular location` informuje, że białko jest wydzialane poza komórkę (*Extracellular region or secreted*). Zakładka `GO - Cellular compoenent` podaje szczegółowe miejsce występowania białka, na przykład retikulum endocytoplazmatyczne, ale są to tymczasowe lokalizacje białka zanim zostanie ono wydzielone z komórki.
3. Panel rekordu `PTM / Processing` w części `Molecule processing` informuje, że insulina posiada dwa sygnałowe peptydy: *Signal peptide* na N-końcu w pozycji 1-24 oraz *Propeptide* na C-końcu w pozycji 57-97. Oba te peptydy zostają wycinane zanim białko zostanie wydzielone poza komórkę. Dojrzałe białko insuliny (łańcuchy A i B) są więc mniejsze niż sekwencja, która jest pokaza w panelu `Sequences`.
4. W panelu `Sequence`, części `Natural variant` zawierająca listę mutacji insuliny, które zostały opisane w literaturze. W kolumnie `Description` zawarta jest informacja na temat zmiany aminokwasu .w sekwenci - jeżeli wariant jest związany z chorobą oznaczone jest skrótem choroby (np. "R → C in IDDM2"). Panel `Under Pathol./Biotech` dostarcza informacji na temat choroby, której skrót jest w tabeli oraz powtarza informacje o wariantach sekwencji związanych z tą jednostką chorobową (np. IDDM2 to skrót od Cukrzycy typu 2).
5. U dołu rekordu insuliny, w panelu `Cross-references` podane są odnośniki do innych baz danych. W części `Sequence databases` tego panelu znajduje się odnośnik do sekwencji białkowej i mRNA insuliny w bazie RefSeq (`NP_000198.1﻿` i `NM_000207.2`).


### Zad. 3
1. W bazie UniProt znajduje się ponad 10 milionów białek zawierających peptydy sygnałowe. Z tego, 41 893 należy do bazy SwissProt a 10,787,160 do bazy trEMBL. Zapytanie do bazy: `annotation:(type:signal)`.
2. Lista znalezionych białek zawiera również białka, w których peptydy sygnałowe zostały przewidziane komputerowo i niekoniecznie wsparte są dowodami doświadczalnymi. Wyszukanie białek zawierających sygnałowe peptydy o doświadczalnie potwierdzonej funkcji: `annotation:(type:signal evidence:experimental)`. W wyniku otrzymano 3 650 białek z bazy SwissProt (oczywiście, nie ma takich białek w bazie trEMBL).
3. Wśród białek z poprzedniego zapytania, 723 należy do człowieka. Zapytanie: `annotation:(type:signal evidence:experimental) AND organism:"Homo sapiens (Human) [9606]"`. Warto zwrócić uwagę na identyfikator taksonomiczny z bazy NCBI. Jeżeli wpisalibyśmy tylko `human` bez identyfikatora taksonomicznego w wyniku moglibyśmy otrzymać również białka pochodzące na przykład z *Human immunodeficiency virus*. 

### Zad. 4
Wejdź na stronę serwisu [UniProt](https://www.uniprot.org). U góry na stronie, kliknij na link `Retrieve/ID mapping`.

* W polu tekstowym `Provide your identifiers` umieść identyfikatory NCBI.
* W polu `Select options` ustaw `from` na `UniProtKB AC/ID` a opcję `to` na `Refseq Protein`.
  
<img src="./images/uniprot-mapping.png" alt="uniprot-mapping" width="500px">

* Uruchom zamianę.

<img src="./images/uniprot-mapping-results.png" alt="uniprot-mapping-results" width="500px">

1. Zamiany identyfikatorów dokonano dla 4 z 5 numerów dostępu.
   * Numer dostępu UniProt `B8XQC5_TETTH` nie został zamieniony.
2. Aby pobrać tabelę w formie tekstowej naciśnij przycisk `Download` i wybierz `Mapping table`.

  ```
  From  To
  TNR6A_HUMAN NP_055309.2
  TNR6A_HUMAN XP_005255314.1
  TNR6A_HUMAN XP_016878642.1
  TNR6A_HUMAN NP_001317449.1
  Q9UPQ9  NP_001020014.1
  Q9UPQ9  NP_001155973.1
  Q9UPQ9  NP_055903.2
  Q9HCJ0  NP_001136112.1
  Q9HCJ0  NP_061869.2
  Q5D869  NP_181532.2
  ```

## Ontologia genów (Gene Ontology)

### Zad. 5
Wejdź na stronę [NCBI](https://www.ncbi.nlm.nih.gov). Wybierz bazę `Gene` i korzystając z zaawansowanego wyszukiwania utwórz zapytania:

```
CASP6[Gene Name] AND human[Organism] 
```

Zostanie wyświetlony rekord o identyfikatorze genu (`Gene ID`): [839](https://www.ncbi.nlm.nih.gov/gene/839).

1. W panelu po prawej stronie pod nagłówkiem `General Gene Information` wybierz `Gene Ontology`.
   * Funkcja komórkowa:
      - aktywność endopeptydazy zaangażowana w proces apoptozy
      - wiązanie białek
   * Proces biologiczny:
      - apoptoza
      - odpowiedź komórkowa na staurosporynę 
   * Kompartment komórkowy:
      - cytoplazma
      - cytozol
      - nukleoplazma

<img src="./images/go-casp6.png" alt="go-casp6" width="400px">

2. Trzyliterowy kody obok opisu terminu ontologii (np. `IBA`, `TAS`) informują o metodzie, według której przypisano dany terminu ontologii do tego genu. Skierowanie kursora myszy na dany skrót wyświetli jego opis. Na przykład:
   * skrót `IBA` (*Inferred from Biological aspect of Ancestor*) oznacza, że dany termin GO został przypisany do tego genu na podstawie organizmu przkodka.
   * skrót `IMP` (*Inferred from Mutant Phenotype*) - termin GO został przypisany do tego genu na podstawie fenotypu mutanta tego genu.
3. W panelu `Related sequences` znajduje się numer dostępu kodowanego przez ten gen białka w bazie UniProt: [UniProtKB/Swiss-Prot:P55212](https://www.uniprot.org/uniprot/P55212). Tak, informacja na temat terminów GO znajduje się w rekordzie UniProt - informacja na temat funkcji i procesu znajduje się w panelu `Function`, a informacja o przedziale komórkowym znajduje się w panelu `Subcellular location`, w zakładce `GO - Cellular component`.


### Zad. 6
Wejdź na stronę serwisu [Gene Ontology](http://amigo.geneontology.org/amigo/). Wpisz nazwę proces `programmed cell death` i wybierz ją z listy autouzupełnień.

<img src="./images/amigo-quicksearch.png" alt="amigo-quicksearch" width="500px">

1. Numer dostępu procesu PCD w bazie Gene Ontology to [GO:0012501](http://amigo.geneontology.org/amigo/term/GO:0012501).
2. Proces PCD nie jest tym samym co apoptoza. Według klasyfikacji GO, proces PCD ma szerszy zakres, a apoptoza jest składową procesu PCD.

<img src="./images/go-pcd-inferred_tree.png" alt="go-pcd-inferred_tree" width="500px">

3. Trzy przykładowe procesy wchodzące w skład PCD to:
   * autofagowa degradacja
   * autoliza
   * apoptoza

4. Procesem nadrzędnym dla PCD jest śmierć komórkowa `GO:0008219 cell death`.

5. Serwis kataloguje `35523` genów/białek zaangażowanych w proces PCD.

6. Po prawej stronie tabeli zawierającej listę białek, w panelu `Filter results`, naciśnij na opcję `Organism`. Z rozwiniętej listy organizmów, naciśnij na zielony przycisk `+` w celu zawężenia listy białek/genu do organizmu człowieka. W wyniku otrzymano `4525` genów/białek człowieka.

7. W panelu `Filter results`, rozwiń opcję `Evidence` i wybierz `Experimental evidence`. Lista obejmuje `1755` genów/białek.

8. W panelu `Filter results` rozwiń opcję `Type` i wybierz `protein`. Następnie rozwiń opcję `Contributor` i wybierz `UniProt`. Lista obejmuje `1098` genów kodujących białko.

9. Wybierz dowolne białko z listy (np. [ACVR1C](http://amigo.geneontology.org/amigo/gene_product/UniProtKB:Q8NER5)). Ze strony Gene Ontology poświęconej temu białku, naciśnij na numer dostępu tego białka w UniProt ([Q8NER5](https://www.uniprot.org/uniprot/Q8NER5)). W rekordzie UniProt, w części `Function` znajduje się lista wszystkich funkcji oraz procesów biologicznych, w które zaangażowane jest białko `Q8NER5`. Przykładowymi procesami - innymi niż PCD - w które zaangażowane jest to białko to odpowiedź na insulinę lub glukozę.


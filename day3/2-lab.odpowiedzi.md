## Motywy i domeny białkowe

## Zad. 1
Otwórz stronę serwisu [Pfam](https://pfam.xfam.org). Z menu wybierz `SEARCH`. Z menu po prawej stronie wybierz `Sequence`. Wklej sekwencję w oknie tekstowym `Sequence` i naciśnij przycisk `Submit`.

<img src="./images/pfam-sequence.png" alt="pfam-sequence">

1. W sekwencji zidentyfikowano:
   * dwie domeny (`Dice_dimer` i `PAZ`)
   * trzy rodziny domen (`Helicase_C`, dwie domeny `Ribonuclease_3`)
2. Domena Dicer (`Helicase_C`) znajduje się w pozyjach `229`-`318`.
   > Serwis Pfam przedstawia dwa typy koordynatów `start` i `end`. Pozycje start i end w kolumnie **Alignment** oznaczają region przyrównania sekwencji zapytania z modelem HMM reprezentującym domenę. Z kolei, koordynaty **Envelope** wyznaczają region w sekwencji, który został dodatkowo probabilistycznie wyznaczony jako region występowania domeny. Koordynaty **Envelope** są zwykle kilka aminokwasów większe niż koordynaty w kolumnie **Alignment**.
3. Wartość E-value przyrównania domeny `Dicer_dimer` z modelem HMM wynosi `4.8e-24`. Przyrównanie jest zatem statystycznie istotne.
4. Numer dostępu domeny `Dicer_dimer` to [PF03368](https://pfam.xfam.org/family/PF03368.14).
5. Domena bierze udział w interferencji RNA (RNAi), procesie wyciszania genów za pomocą cząsteczek dwuniciowego RNA (dsRNA). Domena wiążę dsRNA.
6. 843 gatunki mają białka z domeną `Dicer_dimer`.
7. Według bazy Pfam domena `Dicer_dimer` nie występuje u organizmów prokariotycznych. Proces RNAi występuje u eukariontów.
8. 71 gatunków owadów (*Insecta*) posiada domenę `Dicer_dimer`.
9. Na widoku drzewa gatunków (`Tree`) wskazuje na 1 białko człowieka z domeną `Dicer_dimer`. 
10. 4 sekwencje *Hominidae* posiada domenę `Dicer_dimer`. Aby wyświetlić numery dostępu tych białek, zaznacz na drzewie grupę *Hominidae* i w prawym panelu wybierz `Download` > `Sequence accessions`. Numery dostępu tych białek w UniProt to: 
   ```
   Q9UPY3
   H2NM60
   H2R458
   A0A2I3SVT1
   ```
11. Logo domeny `Dicer_dimer` utworzone na podstawie modelu HMM składa się z `92` aminokwasów.
12. W pozycji 8 modelu HMM najbardziej zachowanymi aminokwasami są `Y` (tyrozyna) i `F` (fenyloalanina)
13. Domena `Dicer_dimer` występuje najczęściej w białkach (w 397 sekwencjach) w sąsiedztwie domeny `Helicase_C` i dwóch domen `Ribonuclease_3`.
14. Sekwencja zapytania to endorybonukelaza Dicer człowieka ([NP_085124.2](https://www.ncbi.nlm.nih.gov/protein/NP_085124)).
